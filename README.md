# Fusio (fusio)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Fusio is an open source API management platform which helps to build and manage REST APIs. It provides capabilities for creating, managing, and documenting APIs with a built-in developer portal, marketplace, and support for multiple programming languages through worker processes.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/fusio/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags:

 - API Management, Open Source, REST API

## Timestamps

- **Created:** 2026-03-16
- **Modified:** 2026-04-18

## APIs

### Fusio Backend API
The Fusio Backend API provides a REST interface to configure and manage all aspects of a Fusio API management instance. It covers operations, routes, schemas, actions, connections, apps, users, and marketplace resources used by the Fusio backend application.

**Human URL:** [https://docs.fusio-project.org/docs/use_cases/api_product/](https://docs.fusio-project.org/docs/use_cases/api_product/)

#### Tags:

 - Backend, Configuration, Management, REST API

#### Properties

- [Documentation](https://docs.fusio-project.org/docs/use_cases/api_product/)
- [GitHubRepository](https://github.com/apioo/fusio)

### Fusio Consumer API
The Fusio Consumer API is used by the developer portal application and enables third-party developers to request access tokens, manage their apps, and interact with protected API endpoints. It provides the authentication and user management layer for API consumers.

**Human URL:** [https://docs.fusio-project.org/docs/backend/consumer/user/](https://docs.fusio-project.org/docs/backend/consumer/user/)

#### Tags:

 - Authentication, Consumer, Developer Portal, REST API

#### Properties

- [Documentation](https://docs.fusio-project.org/docs/backend/consumer/user/)
- [APIReference](https://docs.fusio-project.org/docs/backend/consumer/app)
- [GitHubRepository](https://github.com/apioo/fusio)

### Fusio Worker API
The Fusio Worker API enables executing API action logic in multiple programming languages by forwarding requests to external worker processes. Workers are implemented in the target language (JavaScript, Python, Java, PHP, etc.) and communicate with the Fusio core via a simple REST interface, enabling serverless deployments.

**Human URL:** [https://docs.fusio-project.org/docs/concepts/worker_api](https://docs.fusio-project.org/docs/concepts/worker_api)

#### Tags:

 - Multi-Language, REST API, Serverless, Worker

#### Properties

- [Documentation](https://docs.fusio-project.org/docs/concepts/worker_api)
- [GitHubRepository](https://github.com/apioo/fusio-worker-php)

## Common Properties

- [Documentation](https://docs.fusio-project.org/)
- [GettingStarted](https://docs.fusio-project.org/docs/bootstrap)
- [Blog](https://www.fusio-project.org/blog)
- [ChangeLog](https://github.com/apioo/fusio/blob/master/CHANGELOG.md)
- [GitHubOrganization](https://github.com/apioo)
- [GitHubRepository](https://github.com/apioo/fusio)
- [Support](https://discord.com/invite/eMrMgwsc6e)
- [Marketplace](https://www.fusio-project.org/marketplace)
- [SDK](https://docs.fusio-project.org/docs/backend/development/sdk)

## Features

| Name | Description |
|------|-------------|
| API Gateway | Route and manage incoming API requests with built-in rate limiting and authentication. |
| Developer Portal | Self-service developer portal for API consumers to register, browse APIs, and manage access tokens. |
| Multi-Language Workers | Execute API action logic in JavaScript, Python, Java, PHP, and other languages through worker processes. |
| Marketplace | Browse and install pre-built API actions and adapters from the Fusio marketplace. |
| Schema Management | Define and manage API request and response schemas using TypeSchema format. |
| OAuth2 Authentication | Built-in OAuth2 server for securing APIs with token-based authentication. |
| Rate Limiting | Configure per-app and per-user rate limits to protect API resources. |
| Webhook Support | Define webhook subscriptions to notify consumers of events. |

## Use Cases

| Name | Description |
|------|-------------|
| API Product Building | Build and publish API products with documentation, authentication, and developer onboarding. |
| Microservices Gateway | Use Fusio as an API gateway in front of microservices for unified access control. |
| Data Integration | Connect to databases and external APIs to build data integration endpoints. |
| Serverless API Backend | Build API backends that execute logic in multiple languages without managing servers. |

## Integrations

| Name | Description |
|------|-------------|
| MySQL and PostgreSQL | Connect to MySQL and PostgreSQL databases as data sources for API endpoints. |
| MongoDB | Use MongoDB as a NoSQL data source for API endpoints. |
| Elasticsearch | Integrate with Elasticsearch for search-powered API endpoints. |
| RabbitMQ | Use RabbitMQ for asynchronous message processing in API workflows. |
| Docker | Deploy Fusio and worker containers using Docker and Docker Compose. |

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
