---
name: schedule-a-maintenance-window
description: Suppress expected alerts during planned work by creating, listing, stopping and deleting BigPanda maintenance plans.
api: bigpanda:bigpanda-maintenance-plans-api
generated: '2026-09-04'
method: generated
source: openapi/bigpanda-maintenance-plans-api-openapi.yml
operations:
  - maintenance-plan-v2-create-plan
  - retrieve-all-plans-v2
  - maintenance-plan-v2-retrieve-plan
  - maintenance-plan-v2-update-plan
  - maintenance-plan-v2-stop-plan
  - maintenance-plan-v2-delete-plan
---

# Schedule a BigPanda maintenance window

Base URL `https://api.bigpanda.io`. `Authorization: Bearer <User API Key>`.

## Steps

1. **Create the plan.** `maintenance-plan-v2-create-plan` — `POST /resources/v2.0/maintenance-plans`.
   The plan carries a time range and a condition describing which alerts it suppresses.
2. **Confirm it landed.** `retrieve-all-plans-v2` — `GET /resources/v2.0/ordered-maintenance-plans`, or
   `maintenance-plan-v2-retrieve-plan` — `GET /resources/v2.0/maintenance-plans/{maintenance_id}`.
3. **Adjust it** if the work slips. `maintenance-plan-v2-update-plan` —
   `PUT /resources/v2.0/maintenance-plans/{maintenance_id}`.
4. **End it early** when the work finishes ahead of schedule. `maintenance-plan-v2-stop-plan` —
   `POST /resources/v2.0/maintenance-plans/{maintenance_id}/stop`. This is the reversal path: it works
   **while the plan is running**, and it stops suppression without deleting the record.
5. **Remove it** only if it should never have existed. `maintenance-plan-v2-delete-plan` —
   `DELETE /resources/v2.0/maintenance-plans/{maintenance_id}`.

## Rules that matter

- **Stop, do not delete, to end a live window.** Stopping preserves the record for the audit trail;
  deleting removes it.
- **A maintenance plan suppresses, it does not un-fire.** Alerts that arrived before the plan started
  are already incidents. Create the window before the work begins.
- **No idempotency key.** Creating the same plan twice creates two plans. List before you create if you
  are retrying after a timeout.
- **Rate limit: 5 requests per second** on every operation here.

## Sources
- https://api-docs.bigpanda.io/maintenance-plans
