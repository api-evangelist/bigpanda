---
name: triage-and-resolve-an-incident
description: Find a correlated BigPanda incident, read its context, take ownership, and close it out — the core L1 flow.
api: bigpanda:bigpanda-incidents-api
generated: '2026-09-04'
method: generated
source: openapi/bigpanda-incidents-api-openapi.yml
operations:
  - search-incidents
  - retrieve-incident-by-id
  - get-incident-activities
  - assign-incident
  - comment-on-incident
  - create-an-incident-tag
  - snooze-incident
  - unsnooze-incident
  - resolve-incident-1
  - unassign-incident
---

# Triage and resolve a BigPanda incident

Base URL `https://api.bigpanda.io` (US region). Every request needs
`Authorization: Bearer <User API Key>` and `Accept: application/json`.
An organization lives in exactly ONE region — a request to the wrong region returns 404, not a redirect.

## Before you start

Incidents are addressed **through their environment**. You need an `environment_id` as well as an
`incident_id` for almost every operation. Get environments from `retrieve-all-environments`
(`GET /resources/v2.0/environments`).

## Steps

1. **Find the incident.** `search-incidents` —
   `GET /resources/v2.0/environments/{environment_id}/incidents`.
   Filter with BPQL object syntax before paging; paging parameters differ per endpoint, so read the
   response shape rather than assuming a cursor.
2. **Read it.** `retrieve-incident-by-id` —
   `GET /resources/v2.0/environments/{environment_id}/incidents/{incident_id}`.
3. **Read what already happened.** `get-incident-activities` —
   `GET /resources/v2.0/incidents/{incident_id}/activities`. Do this before acting: another operator or
   agent may already own the incident.
4. **Take ownership.** `assign-incident` —
   `POST /resources/v2.0/environments/{environment_id}/incidents/{incident_id}/assignment`.
   Reversible at any time with `unassign-incident`.
5. **Record what you did.** `comment-on-incident` —
   `POST .../comments`. Comments are the audit trail a human will read.
6. **Tag it if it needs classification.** `create-an-incident-tag` —
   `POST .../tags/{incidenttag_id}`. The tag must already exist as a definition
   (`create-an-incident-tag-definition`).
7. **If it is not actionable yet**, `snooze-incident` — `POST .../snooze`. Reverse with
   `unsnooze-incident`.
8. **Close it.** `resolve-incident-1` — `POST .../resolve`.

## Rules that matter

- **Resolve is one-way.** There is no un-resolve operation. Resolving an already-resolved incident
  returns `409 Conflict`. Confirm before you call it.
- **Merge is reversible, but only by splitting.** `merge-incidents-1` folds incidents together;
  `split-incident` is the documented inverse. No window is stated for how long a merge can be split.
- **There is no idempotency key.** BigPanda documents no `Idempotency-Key` header anywhere. A retried
  `POST` is a second write — a second comment, a second tag, a second assignment. On a timeout, GET the
  incident and check state before retrying.
- **Rate limit: 5 requests per second** on every operation in this flow. On `429`, back off
  exponentially. No `Retry-After` or `X-RateLimit-*` header is documented, so you must choose the
  interval yourself.
- **Errors** are conventional HTTP status codes with a JSON body shaped
  `{"status": <int>, "errors": ["<message>"]}`. `403` means the key's role lacks the permission, not
  that the key is bad.

## Sources
- https://api-docs.bigpanda.io/incidents
- https://api-docs.bigpanda.io/errors-and-troubleshooting
- https://api-docs.bigpanda.io/rate-limits
