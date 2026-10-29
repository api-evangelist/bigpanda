# BigPanda

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

BigPanda is an agentic IT operations (AIOps) platform that ingests alerts from monitoring and observability tools, correlates them into a small number of actionable incidents, links those incidents to the deployment and configuration changes that caused them, and increasingly acts on them through AI agents. Its public API is large and current: 263 operations across 165 paths, published as OpenAPI 3.0.1 on BigPanda's own API reference, covering alert ingestion and enrichment, correlation patterns, incidents, environments, changes and root cause, maintenance plans, topology, outbound webhooks, SCIM 2.0 user provisioning, SSO, roles and API keys, plus a Biggy assistant surface with a remote Model Context Protocol server and an A2A agent endpoint.

**Areas:** Incidents · Monitoring · Platform · AIOps · IT Operations · Alerts · Incident Management · Observability · Agents · MCP

## BigPanda on APIs.io

Everything profiled for BigPanda is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/bigpanda/](https://apis.io/providers/bigpanda/)** — or go straight to one of the APIs or properties below.

### APIs (29)

- [BigPanda AI Settings API](https://apis.io/apis/bigpanda/bigpanda-ai-settings-api/) — AI analysis configurations and on-demand AI analysis generation.
- [BigPanda Alert Filters API](https://apis.io/apis/bigpanda/bigpanda-alert-filters-api/) — Alert filters and filter schedules, in current and v1 routes, for suppressing alerts before correlation.
- [BigPanda Alert Ingestion (OIM) API](https://apis.io/apis/bigpanda/bigpanda-alert-ingestion-oim-api/) — Open Integration Hub ingestion — send raw tool payloads for normalization and processing, with 23 documented tool reference payloads.
- [BigPanda Alerts API](https://apis.io/apis/bigpanda/bigpanda-alerts-api/) — Inbound alert ingestion and batch alert resolution — the write path monitoring tools use to push events into BigPanda.
- [BigPanda API Keys API](https://apis.io/apis/bigpanda/bigpanda-api-keys-api/) — Create, read, update and revoke the User API Keys that authenticate every other call.
- [BigPanda Audit API](https://apis.io/apis/bigpanda/bigpanda-audit-api/) — Search the organization audit log.
- [BigPanda Biggy Query API](https://apis.io/apis/bigpanda/bigpanda-biggy-query-api/) — Send a natural-language question to Biggy and retrieve the response, synchronously or as an async job.
- [BigPanda Change Risk API](https://apis.io/apis/bigpanda/bigpanda-change-risk-api/) — Request and retrieve AI-powered risk ratings for ServiceNow change requests.
- [BigPanda Changes & Root Cause API](https://apis.io/apis/bigpanda/bigpanda-changes-api/) — Ingest deployment and configuration changes and link them to incidents as Root Cause Changes.
- [BigPanda Correlation Patterns API](https://apis.io/apis/bigpanda/bigpanda-correlation-patterns-api/) — The rules that turn alerts into incidents, including their evaluation order.
- [BigPanda Data Connectors API](https://apis.io/apis/bigpanda/bigpanda-data-connectors-api/) — Data connectors and their authentication.
- [BigPanda Email Parser Configuration API](https://apis.io/apis/bigpanda/bigpanda-email-parser-configuration-api/) — Versioned email-parser integration configuration, mirroring the OIM configuration lifecycle.
- [BigPanda Environments API](https://apis.io/apis/bigpanda/bigpanda-environments-api/) — BPQL-defined environments and environment groups that scope every incident operation.
- [BigPanda Incidents API](https://apis.io/apis/bigpanda/bigpanda-incidents-api/) — Search, read, assign, comment, tag, snooze, merge, split and resolve correlated incidents.
- [BigPanda Maintenance Plans API](https://apis.io/apis/bigpanda/bigpanda-maintenance-plans-api/) — Schedule maintenance windows to suppress alerts during planned work, and stop a running window early.
- [BigPanda Meetings & Transcripts API](https://apis.io/apis/bigpanda/bigpanda-meetings-transcripts-api/) — Add the Biggy transcription bot to a call, then list transcripts, read raw text and generate AI summaries.
- [BigPanda Notifications & Webhooks API](https://apis.io/apis/bigpanda/bigpanda-notifications-api/) — Configure Notifications Webhook v2 destinations and discover the dynamic variables a webhook template can interpolate.
- [BigPanda OIM Configuration API](https://apis.io/apis/bigpanda/bigpanda-oim-configuration-api/) — Versioned Open Integration Hub configuration with list, retrieve, diff and restore — the only versioned object in the BigPanda surface.
- [BigPanda Reporting API](https://apis.io/apis/bigpanda/bigpanda-reporting-api/) — Troubleshooting logs and multi-context report generation.
- [BigPanda Roles & Permissions API](https://apis.io/apis/bigpanda/bigpanda-roles-permissions-api/) — Roles, role membership and the permission catalog that decides what a User API Key can do.
- [BigPanda Service Accounts API](https://apis.io/apis/bigpanda/bigpanda-service-accounts-api/) — Machine identities and the API keys attached to them.
- [BigPanda Topology API](https://apis.io/apis/bigpanda/bigpanda-topology-api/) — Service and infrastructure topology used to relate alerts across systems.
- [BigPanda Users & SCIM API](https://apis.io/apis/bigpanda/bigpanda-users-api/) — User management plus a standards-based SCIM 2.0 provisioning surface for Users and Groups.
- [BigPanda Agents (MCP & A2A) API](https://apis.io/apis/bigpanda/bigpanda-agents-mcp-a2a-api/) — The Agents (MCP & A2A) API from BigPanda — 3 operation(s) for agents (mcp & a2a).
- [BigPanda Alert Tags & Enrichment API](https://apis.io/apis/bigpanda/bigpanda-alert-tags-enrichment-api/) — The Alert Tags & Enrichment API from BigPanda — 22 operation(s) for alert tags & enrichment.
- [BigPanda Audit Log API](https://apis.io/apis/bigpanda/bigpanda-audit-log-api/) — The Audit Log API from BigPanda — 2 operation(s) for audit log.
- [BigPanda Changes & Root Cause API](https://apis.io/apis/bigpanda/bigpanda-changes-root-cause-api/) — The Changes & Root Cause API from BigPanda — 4 operation(s) for changes & root cause.
- [BigPanda Major Incident Management API](https://apis.io/apis/bigpanda/bigpanda-major-incident-management-api/) — The Major Incident Management API from BigPanda — 7 operation(s) for major incident management.
- [BigPanda SSO & JIT Provisioning API](https://apis.io/apis/bigpanda/bigpanda-sso-jit-provisioning-api/) — The SSO & JIT Provisioning API from BigPanda — 7 operation(s) for sso & jit provisioning.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Bigpanda Webhooks](https://apis.io/asyncapis/bigpanda/bigpanda-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [bigpanda-mcp.yml](https://apis.io/servers/bigpanda/bigpanda-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Bigpanda Agentic Access](https://apis.io/agentic-access/bigpanda/bigpanda-agentic-access/)

#### JSON Schema (14)

The data models the API reads and writes.

- [AlertRequest](https://apis.io/schemas/bigpanda/bigpanda-alert-request/)
- [AlertResponse](https://apis.io/schemas/bigpanda/bigpanda-alert-response/)
- [AuditLogEntry](https://apis.io/schemas/bigpanda/bigpanda-audit-log-entry/)
- [AuditLogsResponse](https://apis.io/schemas/bigpanda/bigpanda-audit-logs-response/)
- [ChangeRequest](https://apis.io/schemas/bigpanda/bigpanda-change-request/)
- [ChangeResponse](https://apis.io/schemas/bigpanda/bigpanda-change-response/)
- [Environment](https://apis.io/schemas/bigpanda/bigpanda-environment/)
- [EnvironmentRequest](https://apis.io/schemas/bigpanda/bigpanda-environment-request/)
- [EnvironmentsResponse](https://apis.io/schemas/bigpanda/bigpanda-environments-response/)
- [Incident](https://apis.io/schemas/bigpanda/bigpanda-incident/)
- [IncidentsResponse](https://apis.io/schemas/bigpanda/bigpanda-incidents-response/)
- [MaintenancePlan](https://apis.io/schemas/bigpanda/bigpanda-maintenance-plan/)
- [MaintenancePlanRequest](https://apis.io/schemas/bigpanda/bigpanda-maintenance-plan-request/)
- [MaintenancePlansResponse](https://apis.io/schemas/bigpanda/bigpanda-maintenance-plans-response/)

#### JSON Structure (14)

Data models expressed in JSON Structure.

- [Bigpanda Alert Request Structure](https://apis.io/json-structure/bigpanda/bigpanda-alert-request-structure/)
- [Bigpanda Alert Response Structure](https://apis.io/json-structure/bigpanda/bigpanda-alert-response-structure/)
- [Bigpanda Audit Log Entry Structure](https://apis.io/json-structure/bigpanda/bigpanda-audit-log-entry-structure/)
- [Bigpanda Audit Logs Response Structure](https://apis.io/json-structure/bigpanda/bigpanda-audit-logs-response-structure/)
- [Bigpanda Change Request Structure](https://apis.io/json-structure/bigpanda/bigpanda-change-request-structure/)
- [Bigpanda Change Response Structure](https://apis.io/json-structure/bigpanda/bigpanda-change-response-structure/)
- [Bigpanda Environment Request Structure](https://apis.io/json-structure/bigpanda/bigpanda-environment-request-structure/)
- [Bigpanda Environment Structure](https://apis.io/json-structure/bigpanda/bigpanda-environment-structure/)
- [Bigpanda Environments Response Structure](https://apis.io/json-structure/bigpanda/bigpanda-environments-response-structure/)
- [Bigpanda Incident Structure](https://apis.io/json-structure/bigpanda/bigpanda-incident-structure/)
- [Bigpanda Incidents Response Structure](https://apis.io/json-structure/bigpanda/bigpanda-incidents-response-structure/)
- [Bigpanda Maintenance Plan Request Structure](https://apis.io/json-structure/bigpanda/bigpanda-maintenance-plan-request-structure/)
- [Bigpanda Maintenance Plan Structure](https://apis.io/json-structure/bigpanda/bigpanda-maintenance-plan-structure/)
- [Bigpanda Maintenance Plans Response Structure](https://apis.io/json-structure/bigpanda/bigpanda-maintenance-plans-response-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Bigpanda Context](https://apis.io/jsonld/bigpanda/bigpanda-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Bigpanda Vocabulary](https://apis.io/vocabularies/bigpanda/bigpanda-vocabulary/)

#### Examples (14)

Example requests and responses.

- [Bigpanda Alert Request Example](https://apis.io/examples/bigpanda/bigpanda-alert-request-example/)
- [Bigpanda Alert Response Example](https://apis.io/examples/bigpanda/bigpanda-alert-response-example/)
- [Bigpanda Audit Log Entry Example](https://apis.io/examples/bigpanda/bigpanda-audit-log-entry-example/)
- [Bigpanda Audit Logs Response Example](https://apis.io/examples/bigpanda/bigpanda-audit-logs-response-example/)
- [Bigpanda Change Request Example](https://apis.io/examples/bigpanda/bigpanda-change-request-example/)
- [Bigpanda Change Response Example](https://apis.io/examples/bigpanda/bigpanda-change-response-example/)
- [Bigpanda Environment Example](https://apis.io/examples/bigpanda/bigpanda-environment-example/)
- [Bigpanda Environment Request Example](https://apis.io/examples/bigpanda/bigpanda-environment-request-example/)
- [Bigpanda Environments Response Example](https://apis.io/examples/bigpanda/bigpanda-environments-response-example/)
- [Bigpanda Incident Example](https://apis.io/examples/bigpanda/bigpanda-incident-example/)
- [Bigpanda Incidents Response Example](https://apis.io/examples/bigpanda/bigpanda-incidents-response-example/)
- [Bigpanda Maintenance Plan Example](https://apis.io/examples/bigpanda/bigpanda-maintenance-plan-example/)
- [Bigpanda Maintenance Plan Request Example](https://apis.io/examples/bigpanda/bigpanda-maintenance-plan-request-example/)
- [Bigpanda Maintenance Plans Response Example](https://apis.io/examples/bigpanda/bigpanda-maintenance-plans-response-example/)

#### Collections (13)

Postman and Open Collection request collections.

- [BigPanda API](https://apis.io/collections/bigpanda/open-bigpanda/)
- [BigPanda Alerts API](https://apis.io/collections/bigpanda/open-bigpanda-alerts-api/)
- [BigPanda Alerts Audit API](https://apis.io/collections/bigpanda/open-bigpanda-audit-api/)
- [BigPanda Alerts Changes API](https://apis.io/collections/bigpanda/open-bigpanda-changes-api/)
- [BigPanda Alerts Environments API](https://apis.io/collections/bigpanda/open-bigpanda-environments-api/)
- [BigPanda Alerts Incidents API](https://apis.io/collections/bigpanda/open-bigpanda-incidents-api/)
- [BigPanda Alerts Maintenance Plans API](https://apis.io/collections/bigpanda/open-bigpanda-maintenance-plans-api/)
- [BigPanda Alerts API](https://apis.io/collections/bigpanda/postman-bigpanda-alerts-api/)
- [BigPanda Alerts Audit API](https://apis.io/collections/bigpanda/postman-bigpanda-audit-api/)
- [BigPanda Alerts Changes API](https://apis.io/collections/bigpanda/postman-bigpanda-changes-api/)
- [BigPanda Alerts Environments API](https://apis.io/collections/bigpanda/postman-bigpanda-environments-api/)
- [BigPanda Alerts Incidents API](https://apis.io/collections/bigpanda/postman-bigpanda-incidents-api/)
- [BigPanda Alerts Maintenance Plans API](https://apis.io/collections/bigpanda/postman-bigpanda-maintenance-plans-api/)

#### Overlays (56)

OpenAPI overlays, including conversational phrasing for each operation.

- [Bigpanda Agents Mcp A2A Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-agents-mcp-a2a-api-phrasing-overlay/)
- [Bigpanda Agents Overlay](https://apis.io/overlays/bigpanda/bigpanda-agents-overlay/)
- [Bigpanda Ai Settings Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-ai-settings-api-phrasing-overlay/)
- [Bigpanda Ai Settings Overlay](https://apis.io/overlays/bigpanda/bigpanda-ai-settings-overlay/)
- [Bigpanda Alert Enrichment Overlay](https://apis.io/overlays/bigpanda/bigpanda-alert-enrichment-overlay/)
- [Bigpanda Alert Filters Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-alert-filters-api-phrasing-overlay/)
- [Bigpanda Alert Filters Overlay](https://apis.io/overlays/bigpanda/bigpanda-alert-filters-overlay/)
- [Bigpanda Alert Ingestion Oim Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-alert-ingestion-oim-api-phrasing-overlay/)
- [Bigpanda Alert Ingestion Oim Overlay](https://apis.io/overlays/bigpanda/bigpanda-alert-ingestion-oim-overlay/)
- [Bigpanda Alert Tags Enrichment Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-alert-tags-enrichment-api-phrasing-overlay/)
- [Bigpanda Alerts Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-alerts-api-phrasing-overlay/)
- [Bigpanda Alerts Overlay](https://apis.io/overlays/bigpanda/bigpanda-alerts-overlay/)
- [Bigpanda Api Keys Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-api-keys-api-phrasing-overlay/)
- [Bigpanda Api Keys Overlay](https://apis.io/overlays/bigpanda/bigpanda-api-keys-overlay/)
- [Bigpanda Audit Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-audit-api-phrasing-overlay/)
- [Bigpanda Audit Log Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-audit-log-api-phrasing-overlay/)
- [Bigpanda Audit Overlay](https://apis.io/overlays/bigpanda/bigpanda-audit-overlay/)
- [Bigpanda Biggy Query Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-biggy-query-api-phrasing-overlay/)
- [Bigpanda Biggy Query Overlay](https://apis.io/overlays/bigpanda/bigpanda-biggy-query-overlay/)
- [Bigpanda Change Risk Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-change-risk-api-phrasing-overlay/)
- [Bigpanda Change Risk Overlay](https://apis.io/overlays/bigpanda/bigpanda-change-risk-overlay/)
- [Bigpanda Changes Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-changes-api-phrasing-overlay/)
- [Bigpanda Changes Overlay](https://apis.io/overlays/bigpanda/bigpanda-changes-overlay/)
- [Bigpanda Changes Root Cause Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-changes-root-cause-api-phrasing-overlay/)
- [Bigpanda Correlation Patterns Api Phrasing Overlay](https://apis.io/overlays/bigpanda/bigpanda-correlation-patterns-api-phrasing-overlay/)
- …and 31 more published on APIs.io

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [BigPanda — jsonschema rules](https://apis.io/rules/bigpanda/bigpanda-jsonschema-spectral-rules/)
- [BigPanda API Rules](https://apis.io/rules/bigpanda/bigpanda-spectral-rules/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Bigpanda Authentication](https://apis.io/security/bigpanda/bigpanda-authentication/)
- [Bigpanda Domain Security](https://apis.io/security/bigpanda/bigpanda-domain-security/)
- [Bigpanda Trust Center](https://apis.io/security/bigpanda/bigpanda-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Bigpanda Scopes](https://apis.io/scopes/bigpanda/bigpanda-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Bigpanda Plans Pricing](https://apis.io/plans/bigpanda/bigpanda-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Bigpanda Rate Limits](https://apis.io/rate-limits/bigpanda/bigpanda-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Bigpanda Finops](https://apis.io/finops/bigpanda/bigpanda-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.bigpanda.io/)
- [Documentation](https://docs.bigpanda.io/docs/get-started)
- [Getting started](https://api-docs.bigpanda.io/get-started)
- [API reference](https://api-docs.bigpanda.io/)
- [Pricing](https://www.bigpanda.io/pricing/)
- [Sign up](https://www.bigpanda.io/demo/)
- [Support](https://support.bigpanda.io/)
- [Changelog](https://docs.bigpanda.io/docs/release-notes)
- [Blog](https://www.bigpanda.io/blog/)
- [Terms of service](https://www.bigpanda.io/terms-of-service/)
- [Privacy policy](https://www.bigpanda.io/privacy-notice/)
- [GitHub](https://github.com/bigpandaio)
- [Status](https://status.bigpanda.io/)

## API Evangelist rating

**Kin Score 71.6** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 80.0 |
| Contract quality | 67.1 |
| Contract governance | 45.5 |
| Operational transparency | 92.1 |
| Developer ergonomics | 55.4 |
| Access clarity | 60.5 |

**Agent readiness 50.0** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | — |

**Regulatory alignment 39.2** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/bigpanda/](https://apis.io/providers/bigpanda/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for BigPanda: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/bigpanda/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
