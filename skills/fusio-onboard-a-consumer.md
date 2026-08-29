---
name: fusio-onboard-a-consumer
description: >-
  Onboard a third-party developer onto a Fusio-managed API - create the user, grant scopes, create
  the OAuth2 app, issue and later revoke tokens.
api: Fusio Backend API
version: 1
generated: '2026-08-29'
method: generated
source: openapi/fusio-backend.json, openapi/fusio-consumer.json, openapi/fusio-authorization.json
operations:
  - backend.scope.getAll
  - backend.user.create
  - backend.user.resend
  - backend.app.create
  - backend.token.getAll
  - consumer.token.create
  - consumer.token.delete
  - backend.app.deleteToken
  - authorization.revoke
  - authorization.getWhoami
---

# Onboard an API consumer on Fusio

## Steps

1. **Read the scope catalogue.** `backend.scope.getAll` (`GET /backend/scope`) - grant only what
   the consumer needs. `backend.scope.getCategories` shows how scopes group.

2. **Create the user.** `backend.user.create` (`POST /backend/user`) with name, email, password
   and the scopes to grant. If the activation mail is missed, `backend.user.resend`
   (`POST /backend/user/{user_id}/resend`) sends it again.

3. **Create the OAuth2 app.** `backend.app.create` (`POST /backend/app`) returns a client id and
   client secret. The app URL matters: every redirect URI the consumer uses must share that base
   URL.

4. **Issue a token.** Three routes, pick deliberately:
   - `POST /authorization/token` - full OAuth2. Grants: `authorization_code`,
     `client_credentials`, `password`, `refresh_token`.
   - `POST /consumer/login` - username and password, returns a JWT. The simple path.
   - `consumer.token.create` (`POST /consumer/token`) - a personal access token the consumer
     creates themselves, with a chosen subset of scopes. Prefer this for machine use.

5. **Confirm.** `authorization.getWhoami` (`GET /authorization/whoami`) returns the identity the
   token actually resolves to. Call it once before handing the token over.

## Reversibility

This flow is reversible and the windows are clear.

- `authorization.revoke` (`POST /authorization/revoke`) kills the current token immediately.
- `backend.app.deleteToken` (`DELETE /backend/app/{app_id}/token/{token_id}`) kills a specific
  issued token.
- `consumer.token.delete` (`DELETE /consumer/token/{token_id}`) lets the consumer kill their own.
- Every token carries an expiry from the instance configuration, so an un-revoked token dies on
  its own.
- `backend.user.delete` and `backend.app.delete` are soft deletes recoverable through
  `backend.trash.restore` - with **no published retention window**.

## Notes

- Token expiry is instance-configurable; refresh with the `refresh_token` grant or
  `PUT /consumer/login` rather than re-authenticating the user.
- External identity providers (Keycloak, Entra ID, Okta) can be bound per app through
  `backend.identity.create`; consumers then list them at `GET /consumer/identity`.
