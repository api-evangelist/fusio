---
name: fusio-restore-a-deleted-record
description: >-
  Undo a delete on a Fusio instance. Fusio never hard-deletes on a DELETE call - it soft-deletes,
  and this is how you find and restore the record.
api: Fusio Backend API
version: 1
generated: '2026-08-29'
method: generated
source: openapi/fusio-backend.json, https://docs.fusio-project.org/docs/backend/system/trash
operations:
  - backend.trash.getTypes
  - backend.trash.getAllByType
  - backend.trash.restore
---

# Restore a deleted record on Fusio

## The rule

Fusio does not hard-delete. The provider states it directly: "in Fusio it is not possible to
directly delete an entry, instead it is only marked as deleted." Every one of the 23
`DELETE /backend/{entity}/{id}` operations - actions, agents, apps, bundles, categories,
connections, cronjobs, events, firewall rules, forms, identities, operations, pages, plans, rates,
roles, schemas, scopes, taxonomies, triggers, users, webhooks - is a soft delete.

This means a `DELETE` here is a lower-consequence action than it looks. It also means the instance
accumulates deleted records until someone purges them.

## Steps

1. `backend.trash.getTypes` (`GET /backend/trash`) - which entity types currently hold recoverable
   records.
2. `backend.trash.getAllByType` (`GET /backend/trash/{type}`) - the deleted records of one type.
   Paginate with `startIndex` and `count`; narrow with `search`.
3. `backend.trash.restore` (`POST /backend/trash/{type}`) - bring one back.

## The window

**Fusio publishes no retention window.** The documentation states that entries can be restored or
finally deleted, but never says how long a restore stays possible, and none of the three trash
operations declares one. Do not tell a user "you can undo this later" on Fusio's behalf. Restore
now if you need it restored, and if you are automating deletes, capture enough of the record to
recreate it rather than relying on the trash.

## What this does NOT cover

- Promoting an operation from Experimental to **Stable** is not a delete and is not reversible.
  Fusio freezes the action and schema version on that transition.
- Plan purchases are settled by the external payment provider; Fusio publishes no refund or void
  operation of its own.
- Webhook deliveries already sent cannot be recalled.
