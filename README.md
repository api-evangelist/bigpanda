# BigPanda (bigpanda)
BigPanda is an AIOps platform that uses artificial intelligence to help IT operations teams automate incident management by correlating alerts from 200+ monitoring systems, identifying root causes, and streamlining incident resolution. BigPanda moves teams from reactive to proactive incident response with ML-powered alert correlation.

**URL:** [https://docs.bigpanda.io](https://docs.bigpanda.io)

## Tags:

 - Incidents, Monitoring, Platform, AIOps, Alert Correlation, IT Operations

## Timestamps

- **Created:** 2025-01-08
- **Modified:** 2026-04-19

## APIs

### BigPanda API
The BigPanda API enables programmatic management of incidents, alerts, environments, maintenance plans, correlation patterns, and enrichments.

**Human URL:** [https://docs.bigpanda.io/reference/environments-api](https://docs.bigpanda.io/reference/environments-api)

#### Tags:

 - Alerts, Incidents, Environments, Maintenance Plans, Changes, Audit

#### Properties

- [Documentation](https://docs.bigpanda.io/reference)
- [OpenAPI](openapi/bigpanda-openapi.yml)

## Common Properties

- [Portal](https://docs.bigpanda.io)
- [GettingStarted](https://docs.bigpanda.io/docs/get-started)
- [Documentation](https://docs.bigpanda.io/reference)
- [ChangeLog](https://docs.bigpanda.io/docs/release-notes)
- [PostmanWorkspace](https://www.postman.com/bigpandaio/bigpanda-api-staging/overview)
- [Status](https://status.bigpanda.io/)

## Features

| Name | Description |
|------|-------------|
| AI Alert Correlation | ML-powered correlation of alerts from 200+ monitoring tools into actionable incidents. |
| Incident Management | Triage, acknowledge, and resolve correlated incidents with full audit trail. |
| Root Cause Analysis | Automatically identify root causes by correlating alerts with change events. |
| Maintenance Plans | Schedule maintenance windows to suppress expected alerts during planned work. |
| Change Correlation | Ingest deployment and config changes to correlate with alert spikes. |
| Environments | Define DSL-based environments to group incidents by source, severity, or host. |
| Enrichments | Enrich alerts with contextual tags from CMDB and other data sources. |
| AIOps Automation | Automate incident response workflows with AI-driven insights and routing. |

## Use Cases

| Name | Description |
|------|-------------|
| Alert Noise Reduction | Reduce alert fatigue by correlating thousands of alerts into a handful of incidents. |
| Change Impact Analysis | Automatically link deployment changes to alert spikes for faster root cause identification. |
| On-Call Automation | Route correlated incidents to the right on-call team with full context. |
| Maintenance Scheduling | Suppress alerts during planned maintenance to prevent false incident creation. |
| ITSM Integration | Automatically create and update tickets in ServiceNow or Jira from correlated incidents. |

## Integrations

| Name | Description |
|------|-------------|
| PagerDuty | Route correlated incidents to PagerDuty for on-call alerting. |
| ServiceNow | Create and update ServiceNow incidents automatically from BigPanda. |
| Datadog | Ingest Datadog alerts into BigPanda for cross-tool correlation. |
| Nagios | Ingest Nagios monitoring alerts via BigPanda integration. |
| Prometheus | Correlate Prometheus/Alertmanager alerts in BigPanda. |
| Jira | Create Jira issues from BigPanda incidents for engineering tracking. |

## Artifacts

### OpenAPI

- [BigPanda API](openapi/bigpanda-openapi.yml)

### JSON Schema

- [bigpanda-alert-request-schema.json](json-schema/bigpanda-alert-request-schema.json)
- [bigpanda-alert-response-schema.json](json-schema/bigpanda-alert-response-schema.json)
- [bigpanda-environment-schema.json](json-schema/bigpanda-environment-schema.json)
- [bigpanda-incident-schema.json](json-schema/bigpanda-incident-schema.json)
- [bigpanda-maintenance-plan-schema.json](json-schema/bigpanda-maintenance-plan-schema.json)
- [bigpanda-change-request-schema.json](json-schema/bigpanda-change-request-schema.json)
- [bigpanda-audit-log-entry-schema.json](json-schema/bigpanda-audit-log-entry-schema.json)

## Capabilities

### Shared Per-API Definitions

- [BigPanda API](capabilities/shared/bigpanda.yaml) — 10 operations for alerts, incidents, environments, maintenance, changes, and audit

### Workflow Capabilities

| Workflow | APIs Combined | Tools | Persona |
|----------|--------------|-------|---------|
| [Incident Management](capabilities/incident-management.yaml) | BigPanda | 9 | SRE Engineer, IT Ops Manager |

## Vocabulary

- [BigPanda Vocabulary](vocabulary/bigpanda-vocabulary.yaml) — Unified taxonomy mapping 6 resources, 5 actions, 1 workflow, and 2 personas

## Rules

- [BigPanda Spectral Rules](rules/bigpanda-spectral-rules.yml) — 24 rules across 9 categories enforcing BigPanda API conventions

## Maintainers

**FN:** Kin Lane

**Email:** kin@apievangelist.com
