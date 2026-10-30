# Fusio

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Fusio is Apache-2.0, self-hosted API management from apioo (Christoph Kappestein, Germany). An operator installs it and builds APIs inside it: an operation binds an HTTP method and path to an action (SQL, HTTP, MongoDB, Elasticsearch, an LLM agent, or code running in a JavaScript, Python, Java or PHP worker) and a TypeSchema-defined request and response shape. Every instance then generates its own machine-readable contract live - OpenAPI 3.0.3, OpenRPC 1.3.0 and TypeAPI - and serves an RFC 9727 api-catalog, RFC 8414 and RFC 9728 OAuth metadata, OpenID Connect discovery and an RFC 9116 security.txt out of the box. It ships its own OAuth2 authorization server, an Angular developer portal, a rate-limiting and monetization layer, a webhook and trigger system, and an MCP server that turns every published operation into an agent tool. There is no vendor-hosted tier and no pricing: the software is the product.

**Areas:** API Management · Open Source · REST API · API Gateway · Developer Portal · OpenAPI · Self-Hosted · MCP

## Fusio on APIs.io

Everything profiled for Fusio is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/fusio/](https://apis.io/providers/fusio/)** — or go straight to one of the APIs or properties below.

### APIs (43)

- [Fusio Worker API](https://apis.io/apis/fusio/fusio-worker-api/) — The Fusio Worker API enables executing API action logic in multiple programming languages by forwarding requests to external worker processes. Workers are…
- [Fusio Account API](https://apis.io/apis/fusio/fusio-account-api/) — The account API from Fusio — 9 operation(s) for account.
- [Fusio Action API](https://apis.io/apis/fusio/fusio-action-api/) — The action API from Fusio — 6 operation(s) for action.
- [Fusio Agent API](https://apis.io/apis/fusio/fusio-agent-api/) — The agent API from Fusio — 7 operation(s) for agent.
- [Fusio App API](https://apis.io/apis/fusio/fusio-app-api/) — The app API from Fusio — 5 operation(s) for app.
- [Fusio Audit API](https://apis.io/apis/fusio/fusio-audit-api/) — The audit API from Fusio — 2 operation(s) for audit.
- [Fusio Authorization API](https://apis.io/apis/fusio/fusio-authorization-api/) — The authorization API from Fusio — 2 operation(s) for authorization.
- [Fusio Backup API](https://apis.io/apis/fusio/fusio-backup-api/) — The backup API from Fusio — 2 operation(s) for backup.
- [Fusio Bundle API](https://apis.io/apis/fusio/fusio-bundle-api/) — The bundle API from Fusio — 3 operation(s) for bundle.
- [Fusio Category API](https://apis.io/apis/fusio/fusio-category-api/) — The category API from Fusio — 2 operation(s) for category.
- [Fusio Config API](https://apis.io/apis/fusio/fusio-config-api/) — The config API from Fusio — 2 operation(s) for config.
- [Fusio Connection API](https://apis.io/apis/fusio/fusio-connection-api/) — The connection API from Fusio — 14 operation(s) for connection.
- [Fusio Cronjob API](https://apis.io/apis/fusio/fusio-cronjob-api/) — The cronjob API from Fusio — 2 operation(s) for cronjob.
- [Fusio Dashboard API](https://apis.io/apis/fusio/fusio-dashboard-api/) — The dashboard API from Fusio — 1 operation(s) for dashboard.
- [Fusio Event API](https://apis.io/apis/fusio/fusio-event-api/) — The event API from Fusio — 4 operation(s) for event.
- [Fusio Firewall API](https://apis.io/apis/fusio/fusio-firewall-api/) — The firewall API from Fusio — 2 operation(s) for firewall.
- [Fusio Form API](https://apis.io/apis/fusio/fusio-form-api/) — The form API from Fusio — 4 operation(s) for form.
- [Fusio Generator API](https://apis.io/apis/fusio/fusio-generator-api/) — The generator API from Fusio — 2 operation(s) for generator.
- [Fusio Grant API](https://apis.io/apis/fusio/fusio-grant-api/) — The grant API from Fusio — 2 operation(s) for grant.
- [Fusio Identity API](https://apis.io/apis/fusio/fusio-identity-api/) — The identity API from Fusio — 7 operation(s) for identity.
- [Fusio Log API](https://apis.io/apis/fusio/fusio-log-api/) — The log API from Fusio — 6 operation(s) for log.
- [Fusio Marketplace API](https://apis.io/apis/fusio/fusio-marketplace-api/) — The marketplace API from Fusio — 6 operation(s) for marketplace.
- [Fusio Operation API](https://apis.io/apis/fusio/fusio-operation-api/) — The operation API from Fusio — 2 operation(s) for operation.
- [Fusio Page API](https://apis.io/apis/fusio/fusio-page-api/) — The page API from Fusio — 4 operation(s) for page.
- [Fusio Payment API](https://apis.io/apis/fusio/fusio-payment-api/) — The payment API from Fusio — 2 operation(s) for payment.
- [Fusio Plan API](https://apis.io/apis/fusio/fusio-plan-api/) — The plan API from Fusio — 4 operation(s) for plan.
- [Fusio Rate API](https://apis.io/apis/fusio/fusio-rate-api/) — The rate API from Fusio — 2 operation(s) for rate.
- [Fusio Role API](https://apis.io/apis/fusio/fusio-role-api/) — The role API from Fusio — 2 operation(s) for role.
- [Fusio Schema API](https://apis.io/apis/fusio/fusio-schema-api/) — The schema API from Fusio — 4 operation(s) for schema.
- [Fusio Scope API](https://apis.io/apis/fusio/fusio-scope-api/) — The scope API from Fusio — 5 operation(s) for scope.
- [Fusio SDK API](https://apis.io/apis/fusio/fusio-sdk-api/) — The sdk API from Fusio — 1 operation(s) for sdk.
- [Fusio Specification API](https://apis.io/apis/fusio/fusio-specification-api/) — The specification API from Fusio — 3 operation(s) for specification.
- [Fusio Statistic API](https://apis.io/apis/fusio/fusio-statistic-api/) — The statistic API from Fusio — 17 operation(s) for statistic.
- [Fusio System API](https://apis.io/apis/fusio/fusio-system-api/) — The System API from Fusio — 7 operation(s) for system.
- [Fusio Taxonomy API](https://apis.io/apis/fusio/fusio-taxonomy-api/) — The taxonomy API from Fusio — 2 operation(s) for taxonomy.
- [Fusio Tenant API](https://apis.io/apis/fusio/fusio-tenant-api/) — The tenant API from Fusio — 1 operation(s) for tenant.
- [Fusio Test API](https://apis.io/apis/fusio/fusio-test-api/) — The test API from Fusio — 2 operation(s) for test.
- [Fusio Token API](https://apis.io/apis/fusio/fusio-token-api/) — The token API from Fusio — 4 operation(s) for token.
- [Fusio Transaction API](https://apis.io/apis/fusio/fusio-transaction-api/) — The transaction API from Fusio — 4 operation(s) for transaction.
- [Fusio Trash API](https://apis.io/apis/fusio/fusio-trash-api/) — The trash API from Fusio — 2 operation(s) for trash.
- [Fusio Trigger API](https://apis.io/apis/fusio/fusio-trigger-api/) — The trigger API from Fusio — 2 operation(s) for trigger.
- [Fusio User API](https://apis.io/apis/fusio/fusio-user-api/) — The user API from Fusio — 3 operation(s) for user.
- [Fusio Webhook API](https://apis.io/apis/fusio/fusio-webhook-api/) — The webhook API from Fusio — 4 operation(s) for webhook.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Fusio Webhooks](https://apis.io/asyncapis/fusio/fusio-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Fusio MCP Server](https://apis.io/servers/fusio/fusio-mcp-server/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Fusio Agentic Access](https://apis.io/agentic-access/fusio/fusio-agentic-access/)

#### JSON Schema (164)

The data models the API reads and writes.

- [Backend_AccountChangePassword](https://apis.io/schemas/fusio/fusio-backend-account-change-password/)
- [Backend_Action](https://apis.io/schemas/fusio/fusio-backend-action/)
- [Backend_ActionCollection](https://apis.io/schemas/fusio/fusio-backend-action-collection/)
- [Backend_ActionCommitCollection](https://apis.io/schemas/fusio/fusio-backend-action-commit-collection/)
- [Backend_ActionExecuteRequest](https://apis.io/schemas/fusio/fusio-backend-action-execute-request/)
- [Backend_ActionExecuteResponse](https://apis.io/schemas/fusio/fusio-backend-action-execute-response/)
- [Backend_ActionIndex](https://apis.io/schemas/fusio/fusio-backend-action-index/)
- [Backend_Agent](https://apis.io/schemas/fusio/fusio-backend-agent/)
- [Backend_AgentCollection](https://apis.io/schemas/fusio/fusio-backend-agent-collection/)
- [Backend_AgentMessageCollection](https://apis.io/schemas/fusio/fusio-backend-agent-message-collection/)
- [Backend_App](https://apis.io/schemas/fusio/fusio-backend-app/)
- [Backend_AppCollection](https://apis.io/schemas/fusio/fusio-backend-app-collection/)
- [Backend_Audit](https://apis.io/schemas/fusio/fusio-backend-audit/)
- [Backend_AuditCollection](https://apis.io/schemas/fusio/fusio-backend-audit-collection/)
- [Backend_BackupExport](https://apis.io/schemas/fusio/fusio-backend-backup-export/)
- [Backend_BackupImport](https://apis.io/schemas/fusio/fusio-backend-backup-import/)
- [Backend_BackupImportResult](https://apis.io/schemas/fusio/fusio-backend-backup-import-result/)
- [Backend_Bundle](https://apis.io/schemas/fusio/fusio-backend-bundle/)
- [Backend_BundleCollection](https://apis.io/schemas/fusio/fusio-backend-bundle-collection/)
- [Backend_BundleCreate](https://apis.io/schemas/fusio/fusio-backend-bundle-create/)
- [Backend_BundleUpdate](https://apis.io/schemas/fusio/fusio-backend-bundle-update/)
- [Backend_Category](https://apis.io/schemas/fusio/fusio-backend-category/)
- [Backend_CategoryCollection](https://apis.io/schemas/fusio/fusio-backend-category-collection/)
- [Backend_CategoryCreate](https://apis.io/schemas/fusio/fusio-backend-category-create/)
- [Backend_CategoryUpdate](https://apis.io/schemas/fusio/fusio-backend-category-update/)
- …and 139 more published on APIs.io

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Fusio Context](https://apis.io/jsonld/fusio/fusio-context/)

#### Overlays (4)

OpenAPI overlays, including conversational phrasing for each operation.

- [Fusio Authorization Overlay](https://apis.io/overlays/fusio/fusio-authorization-overlay/)
- [Fusio Backend Overlay](https://apis.io/overlays/fusio/fusio-backend-overlay/)
- [Fusio Consumer Overlay](https://apis.io/overlays/fusio/fusio-consumer-overlay/)
- [Fusio System Overlay](https://apis.io/overlays/fusio/fusio-system-overlay/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Fusio API Rules](https://apis.io/rules/fusio/fusio-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Fusio Authentication](https://apis.io/security/fusio/fusio-authentication/)
- [Fusio Domain Security](https://apis.io/security/fusio/fusio-domain-security/)
- [Fusio Vulnerability Disclosure](https://apis.io/security/fusio/fusio-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Fusio Scopes](https://apis.io/scopes/fusio/fusio-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Fusio Plans Pricing](https://apis.io/plans/fusio/fusio-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Fusio Rate Limits](https://apis.io/rate-limits/fusio/fusio-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Fusio Finops](https://apis.io/finops/fusio/fusio-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.fusio-project.org/)
- [Documentation](https://docs.fusio-project.org/)
- [Getting started](https://docs.fusio-project.org/docs/bootstrap)
- [API reference](https://demo.fusio-project.org/apps/redoc)
- [Support](https://discord.com/invite/eMrMgwsc6e)
- [Changelog](https://github.com/apioo/fusio/blob/master/CHANGELOG.md)
- [Blog](https://www.fusio-project.org/blog)
- [GitHub](https://github.com/apioo)

## API Evangelist rating

**Kin Score 59.4** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.3 |
| Contract quality | 73.5 |
| Contract governance | 35.6 |
| Operational transparency | 71.1 |
| Developer ergonomics | 80.4 |
| Access clarity | 0.0 |

**Agent readiness 53.4** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | templated |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 32.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/fusio/](https://apis.io/providers/fusio/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Fusio: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/fusio/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
