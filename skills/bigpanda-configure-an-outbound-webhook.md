---
name: configure-an-outbound-webhook
description: Register and manage a BigPanda Notifications Webhook v2 destination so incident events reach a system with no native integration.
api: bigpanda:bigpanda-notifications-api
generated: '2026-09-04'
method: generated
source: openapi/bigpanda-notifications-api-openapi.yml
operations:
  - retrieve-available-dynamic-variables
  - create-a-new-webhook-v2-workflow-integration
  - retrieve-all-existing-webhook-v2-configurations
  - retrieve-an-existing-webhook-v2-configuration
  - update-an-existing-webhook-v2-workflow-integration
  - deleteResourcesV21IntegrationsByAppKey
---

# Configure a BigPanda outbound webhook

Base URL `https://api.bigpanda.io`. `Authorization: Bearer <User API Key>`.

Webhook v2 is BigPanda's preferred mechanism for pushing incidents to ticketing, messaging and
automation platforms that have no native integration. It supports custom headers, custom URL paths and
dynamic variables interpolated from the incident.

## Steps

1. **Discover the payload vocabulary first.** `retrieve-available-dynamic-variables` —
   `GET /resources/v2.1/fields-resolver/workflows`. This enumerates the variables you can interpolate.
   It is the closest thing BigPanda publishes to an event schema — there is no published catalog of
   webhook event types and no schema for the delivered body, because the body is whatever your template
   composes.
2. **Create the destination.** `create-a-new-webhook-v2-workflow-integration` —
   `POST /resources/v2.1/integrations`.
3. **Verify.** `retrieve-all-existing-webhook-v2-configurations` — `GET /resources/v2.1/integrations`,
   then `retrieve-an-existing-webhook-v2-configuration` —
   `GET /resources/v2.1/integrations/{integration_id}`.
4. **Change it in place.** `update-an-existing-webhook-v2-workflow-integration` —
   `PUT /resources/v2.1/integrations/{integration_id}`.
5. **Remove it** by app key. `deleteResourcesV21IntegrationsByAppKey` —
   `DELETE /resources/v2.1/integrations/{app_key}`.

## Rules that matter

- **Two different identifiers.** Read and update take `integration_id`; delete takes `app_key`. They are
  not interchangeable — fetch the configuration and read both off it before deleting.
- **Deletion is not versioned.** Integration *configuration* is versioned and restorable
  (`list-configuration-versions`, `diff-configuration-versions`, `restore-configuration-version` in
  `openapi/bigpanda-oim-configuration-api-openapi.yml`), but deleting the integration itself is not
  covered by that. Export the configuration before you delete.
- **No idempotency key.** Creating twice creates two destinations, and both will fire.
- **For async results, prefer a callback over polling.** Callback notification configuration endpoints
  push a completion instead of requiring you to poll the Job resource.

## Sources
- https://api-docs.bigpanda.io/webhooks
- https://api-docs.bigpanda.io/asynchronous-operations
- https://docs.bigpanda.io/en/notifications-webhook.html
