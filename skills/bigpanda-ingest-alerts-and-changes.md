---
name: ingest-alerts-and-changes
description: Push monitoring alerts and deployment/config changes into BigPanda so correlation can link a spike to what caused it.
api: bigpanda:bigpanda-alerts-api
generated: '2026-09-04'
method: generated
source: openapi/bigpanda-alerts-api-openapi.yml, openapi/bigpanda-changes-api-openapi.yml
operations:
  - alerts
  - oim-send-alert
  - resolve-alerts
  - create-or-update-a-change
  - retrieve-all-changes
  - retrieve-a-change
  - create-related-change-rcc
  - retrieve-rcc-relations
---

# Ingest alerts and changes into BigPanda

Base URL `https://api.bigpanda.io`. Ingestion is the one surface where an **Org Token** is still
accepted; everything else needs a User API Key. Prefer a User API Key for new integrations.

## Send alerts

- `alerts` — `POST /data/v2/alerts` (the classic inbound Alerts API).
- `oim-send-alert` — `POST /oim/api/alerts` (the Open Integration Hub path).

Alerts are append-only. There is no un-ingest. The inverse of an alert is a **resolution**, not a delete.

- `resolve-alerts` — `POST /resources/v2.0/environments/{environment_id}/batch-resolve/alerts`.
  **Rate limit: 1 call per second, maximum 500 alerts per request.** This is the strictest published
  limit in the API — batch deliberately, do not fan out.

## Send changes

- `create-or-update-a-change` — `POST /data/changes`. This is an **upsert** keyed on the identifier you
  supply, which is the only replay protection anywhere in the BigPanda API: re-sending the same change
  updates it rather than creating a duplicate. It is not a general idempotency key and it does not apply
  to any other endpoint.
- `retrieve-all-changes` — `GET /resources/v2.0/changes`; `retrieve-a-change` — `GET /resources/v2.0/changes/{change_id}`.

**Rate limit on the whole Changes surface: 400 changes per minute and 50,000 per week.** BigPanda marks
the weekly cap `(contractual)` — it is a commercial term, not just a throttle. Budget it: a busy CI
pipeline can exhaust 50,000 change records in days.

## Link a change to an incident (Root Cause Changes)

- `create-related-change-rcc` — `POST /resources/v2.0/rcc`
- `retrieve-rcc-relations` — `GET /resources/v2.0/rcc`
- `update-related-change-rcc` / `retrieve-an-rcc-change` — `/resources/v2.0/rcc/{related_change_id}`

## Rules that matter

- **No idempotency key.** Outside `create-or-update-a-change`, a retried ingest is a second alert.
  Include a stable identifier in the alert payload so BigPanda's own dedupe can do the work instead.
- **Region matters.** Send to your organization's region. `https://api.bigpanda.io` is US. The EU value
  BigPanda publishes, `https://api.eu.bigpanda.io`, did not resolve in DNS on 2026-09-04; the live EU
  host observed was `https://eu-api.bigpanda.io`. Confirm your EU base URL with BigPanda before wiring
  an ingest pipeline to it.
- **429** means the endpoint limit was hit. Back off exponentially; no retry header is documented.

## Sources
- https://api-docs.bigpanda.io/alert-ingestion
- https://api-docs.bigpanda.io/changes-and-root-cause
- https://api-docs.bigpanda.io/regions
