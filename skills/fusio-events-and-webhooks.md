---
name: fusio-events-and-webhooks
description: >-
  Register an event on a Fusio instance, let consumers subscribe webhooks to it, dispatch it, and
  read back delivery outcomes.
api: Fusio Backend API
version: 1
generated: '2026-08-29'
method: generated
source: openapi/fusio-backend.json, openapi/fusio-consumer.json, https://docs.fusio-project.org/docs/backend/api/event
operations:
  - backend.event.create
  - backend.event.getAll
  - backend.trigger.create
  - consumer.event.getAll
  - consumer.webhook.create
  - consumer.webhook.getAll
  - consumer.webhook.get
  - backend.webhook.getAll
  - consumer.webhook.delete
---

# Events and webhooks on Fusio

## Register the event (operator)

`backend.event.create` (`POST /backend/event`) with a name, description and a schema describing
the payload the event will carry. The schema is the contract subscribers rely on, so define it
before anyone subscribes.

## Subscribe (consumer)

`consumer.webhook.create` (`POST /consumer/webhook`):

```json
{"event": "my_event", "endpoint": "http://my-app.com/callback"}
```

`consumer.event.getAll` (`GET /consumer/event`) lists which events this consumer may subscribe to.

## Dispatch (operator)

From inside an action: `$this->dispatcher->dispatch('my_event', ['foo' => 'bar'])`. Or configure
the built-in `Util-Dispatch-Event` action to dispatch a payload without writing code.

## What the subscriber receives

```
POST /callback HTTP/1.1
Host: my-app.com
Content-Type: application/json
User-Agent: Fusio/<version>@<commit>

{"foo": "bar"}
```

**There is no signature.** Fusio sends no HMAC, no timestamp header and no shared secret, so a
subscriber cannot verify a delivery came from the instance. If authenticity matters, put the
callback behind a secret path or an allowlist of the instance's egress IP, and treat the payload
as untrusted.

## Retries

If the endpoint returns a non-successful status code, Fusio retries up to **3** times. No backoff
schedule is published. Make the callback idempotent on your side.

## Read back deliveries

`consumer.webhook.get` (`GET /consumer/webhook/{webhook_id}`) returns a `responses` array with
`status`, `code`, `attempts` and `executeDate` per delivery - so a subscriber can audit their own
delivery history without asking the operator.

## Triggers - the inbound direction

`backend.trigger.create` (`POST /backend/trigger`) binds an event to an **action**, so an event can
drive internal work instead of (or as well as) an outbound webhook.

## Reversibility

`consumer.webhook.delete` and `backend.webhook.delete` are soft deletes, restorable through
`backend.trash.restore` with no published retention window. Deleting a subscription stops future
deliveries; it does not recall deliveries already sent.
