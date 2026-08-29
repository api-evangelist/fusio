---
name: fusio-publish-an-operation
description: >-
  Publish a new REST operation on a Fusio instance end to end - define the response schema, create
  the action that produces it, bind both to an HTTP method and path, scope it, rehearse it, and
  promote it to stable.
api: Fusio Backend API
version: 1
generated: '2026-08-29'
method: generated
source: openapi/fusio-backend.json
operations:
  - backend.schema.create
  - backend.schema.getPreview
  - backend.action.getClasses
  - backend.action.getForm
  - backend.action.create
  - backend.action.execute
  - backend.operation.create
  - backend.scope.create
  - backend.operation.update
  - backend.operation.getAll
---

# Publish an operation on Fusio

An operation is Fusio's unit of publication: one HTTP method and path, bound to an action that
produces the response and a schema that describes it. Nothing is live until the operation exists.

## Before you start

- Authenticate. Every call below needs a bearer token with the matching `backend.*` scope
  (`backend.schema`, `backend.action`, `backend.operation`, `backend.scope`). Get one from
  `POST /authorization/token` or use a personal access token.
- Read `authentication/fusio-authentication.yml` and `scopes/fusio-scopes.yml` for the full model.

## Steps

1. **Define the response shape.** `backend.schema.create` (`POST /backend/schema`) with a
   TypeSchema source. Rehearse it first with `backend.schema.getPreview`
   (`POST /backend/schema/preview/{schema_id}`), which renders the schema without committing it.

2. **Pick an action class.** `backend.action.getClasses` (`GET /backend/action/list`) lists every
   action class installed on this instance. `backend.action.getForm`
   (`GET /backend/action/form`) returns the config form for the class you chose, so you know which
   config fields are required rather than guessing.

3. **Create the action.** `backend.action.create` (`POST /backend/action`) with the class and its
   config.

4. **Rehearse the action.** `backend.action.execute`
   (`POST /backend/action/execute/{action_id}`) runs it against test input. The provider documents
   this operation as being for exactly this purpose. Do this before wiring anything to a URL.

5. **Create the scope** if the operation should be protected.
   `backend.scope.create` (`POST /backend/scope`).

6. **Create the operation.** `backend.operation.create` (`POST /backend/operation`) binding
   `httpMethod`, `httpPath`, the action, the outgoing schema, the scopes and `public`.

7. **Verify.** `backend.operation.getAll` (`GET /backend/operation`) and then call the new path.
   Every Fusio response carries `X-Operation-Id`, so you can confirm you hit the operation you
   just created rather than inferring it from the path.

## Promoting to stable — read this before you do it

`backend.operation.update` can move the operation's stability from Experimental to Stable. **That
transition is not reversible.** Fusio freezes the action and schema version on the transition and
the provider states that afterwards "it is also no longer possible to make any changes to the
operation". Stay Experimental while anything is still moving. See
`lifecycle/fusio-lifecycle.yml`.

## Reversibility

Deletes here are soft. `backend.operation.delete`, `backend.action.delete` and
`backend.schema.delete` mark the record deleted rather than removing it, and
`backend.trash.restore` (`POST /backend/trash/{type}`) brings it back. **Fusio publishes no
retention window**, so do not assume a restore will still be possible later.

## Errors and retries

- Failures return `{"success": false, "title": "...", "message": "...", "id": "..."}` as
  `application/json`. This is not RFC 9457. See `errors/fusio-problem-types.yml`.
- **There is no idempotency key.** A retried `POST /backend/schema` or `POST /backend/operation`
  creates a second record. Read back with `getAll` before retrying a create that may have
  succeeded.
- On `429`, back off; `Retry-After` is 900 seconds. `RateLimit-Limit` and `RateLimit-Remaining`
  are on successful responses when a rate allocation applies.
