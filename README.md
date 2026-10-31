# Reevo

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

Reevo is an AI-native revenue platform ("revenue operating system") that consolidates the sales workflow into one system across four products: Find (lead sourcing, enrichment, routing and scoring), Engage (email sequences, dialing, inbox and meeting prep), Win (deal monitoring, smart task logging and coaching) and Foundation (a native CRM with an AI copilot, reporting, workflows and integrations). It helps GTM teams eliminate tool sprawl and automate repetitive sales work. Backed by Kleiner Perkins and Khosla Ventures. Reevo ships two callable surfaces: a permission-scoped public REST API at https://api.reevo.ai/api/v1/public authenticated with an x-api-key header (accounts, contacts, opportunities, tasks, manual activities, users, mailboxes and sequence enrollments), and a remote Model Context Protocol server at https://mcp.reevo.ai/mcp that exposes roughly 30 CRM tools over streamable-HTTP with OAuth 2.0 and granular read/create/update scopes. Neither surface publishes an OpenAPI or AsyncAPI definition — the contract is documented in prose in the Reevo Knowledge Base.

**Areas:** Company · Artificial Intelligence · Sales · CRM · Revenue Operations · Sales Automation · Lead Generation · Agents · MCP · Sales Engagement · A2A

## Reevo on APIs.io

Everything profiled for Reevo is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/reevo/](https://apis.io/providers/reevo/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [Reevo Public REST API](https://apis.io/apis/reevo/reevo-public-rest-api/) — Reevo's permission-scoped public REST API. Endpoints cover account and contact upsert, accounts (create/update/get/search-by-domain), contacts (get/search),…
- [Reevo MCP Server](https://apis.io/apis/reevo/reevo-mcp-server/) — Reevo's remote Model Context Protocol server. An MCP client POSTs to https://mcp.reevo.ai/mcp over MCP streamable-HTTP transport with OAuth 2.0…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Reevo Webhooks](https://apis.io/asyncapis/reevo/reevo-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Reevo MCP](https://apis.io/servers/reevo/reevo-mcp/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Reevo Authentication](https://apis.io/security/reevo/reevo-authentication/)
- [Reevo Domain Security](https://apis.io/security/reevo/reevo-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Reevo Scopes](https://apis.io/scopes/reevo/reevo-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Reevo Plans Pricing](https://apis.io/plans/reevo/reevo-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Reevo Rate Limits](https://apis.io/rate-limits/reevo/reevo-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.reevo.ai)
- [Documentation](https://help.reevo.ai)
- [Getting started](https://help.reevo.ai/Getting-started/Onboarding)
- [API reference](https://help.reevo.ai/Data-management-and-migration/Integrations-With-Other-Tools)
- [Pricing](https://www.reevo.ai/pricing)
- [Support](https://help.reevo.ai)
- [Changelog](https://www.reevo.ai/release-notes)
- [Blog](https://www.reevo.ai/blog)
- [Compliance](https://www.reevo.ai/pricing)
- [Terms of service](https://www.reevo.ai/terms)
- [Privacy policy](https://www.reevo.ai/privacy)
- [GitHub](https://github.com/ReevoAI)

## API Evangelist rating

**Kin Score 52.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 75.0 |
| Contract quality | 39.0 |
| Contract governance | 18.2 |
| Operational transparency | 26.3 |
| Developer ergonomics | 54.8 |
| Access clarity | 77.6 |

**Agent readiness 56.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | yes |
| Well Known Catalog | yes |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | na |

**Regulatory alignment 36.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/reevo/](https://apis.io/providers/reevo/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Reevo: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/reevo/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
