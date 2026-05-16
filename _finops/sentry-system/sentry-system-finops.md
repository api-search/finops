---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi-derefed.json
  format: json
  label: Sentry API
  slug: sentry-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Events and Issues API
  slug: sentry-events-and-issues-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Organizations API
  slug: sentry-organizations-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Projects API
  slug: sentry-projects-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Teams API
  slug: sentry-teams-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Releases API
  slug: sentry-releases-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Alerts API
  slug: sentry-alerts-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Crons API
  slug: sentry-crons-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Dashboards API
  slug: sentry-dashboards-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Discover API
  slug: sentry-discover-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Environments API
  slug: sentry-environments-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Explore API
  slug: sentry-explore-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Integration Platform API
  slug: sentry-integration-platform-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Integrations API
  slug: sentry-integrations-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Mobile Builds API
  slug: sentry-mobile-builds-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Monitors API
  slug: sentry-monitors-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Prevent API
  slug: sentry-prevent-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Replays API
  slug: sentry-replays-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry SCIM API
  slug: sentry-scim-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Seer API
  slug: sentry-seer-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
- filename: openapi-derefed.json
  format: json
  label: Sentry Users API
  slug: sentry-users-api
  spec_type: OpenAPI
  url: https://github.com/getsentry/sentry-api-schema/blob/main/openapi-derefed.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription + Pay-As-You-Go
description: FOCUS-aligned FinOps shape for Sentry — tiered SaaS subscription with multiple consumption meters (errors, logs/metrics, spans, replays, uptime monitors, cron monitors). Team and Business plans publish per-unit overage prices ($0.50/GB logs, $1.00/uptime alert, $0.78/cron monitor); Developer hard-caps on free quota; Enterprise is custom.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Functional Software, Inc.
  ProviderName: Sentry
  PublisherName: Functional Software, Inc.
  ServiceCategory: Observability / APM
  ServiceName: Sentry
layout: finops
meters:
- aggregation: sum
  description: Captured error events
  dimensions:
  - organization
  - project
  - environment
  name: errors
  unit: error
- aggregation: sum
  description: Logs and metrics ingested in GB (overage billed at $0.50/GB on Team/Business)
  dimensions:
  - organization
  - project
  name: logs_metrics
  unit: GB
- aggregation: sum
  description: Tracing spans ingested
  dimensions:
  - organization
  - project
  name: spans
  unit: span
- aggregation: sum
  description: Session Replay recordings ingested
  dimensions:
  - organization
  - project
  name: session_replays
  unit: replay
- aggregation: sum
  description: Active uptime monitors / alerts (overage at $1.00/alert on Team/Business)
  dimensions:
  - organization
  name: uptime_monitors
  unit: alert
- aggregation: sum
  description: Active cron monitors (overage at $0.78/monitor on Team/Business)
  dimensions:
  - organization
  name: cron_monitors
  unit: monitor
- aggregation: sum
  description: Recurring monthly plan fee (Team $26/mo, Business $80/mo, Enterprise custom)
  dimensions:
  - plan
  name: subscription_fee
  unit: month
name: Sentry System Finops
provider_name: Sentry
provider_slug: sentry-system
publisher_name: Functional Software, Inc. (Sentry)
service_category: Observability / APM
slug: sentry-system-finops
source_filename: sentry-system-finops.yml
source_heading: FinOps Profile
source_url: https://sentry.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sentry\nproviderId: sentry-system\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Error Tracking\n  - Observability\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Sentry — tiered SaaS subscription with multiple consumption\n  meters (errors, logs/metrics, spans, replays, uptime monitors, cron monitors). Team and Business plans\n  publish per-unit overage prices ($0.50/GB logs, $1.00/uptime alert, $0.78/cron monitor); Developer hard-caps\n  on free quota; Enterprise is custom.\nsources:\n  - https://sentry.io/pricing/\n  - https://docs.sentry.io/api/ratelimits/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Functional Software,\
  \ Inc. (Sentry)\nserviceCategory: Observability / APM\nbillingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Sentry\n  ServiceCategory: Observability / APM\n  ProviderName: Sentry\n  PublisherName: Functional Software, Inc.\n  InvoiceIssuerName: Functional Software, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: errors\n    description: Captured error events\n    unit: error\n    aggregation: sum\n    dimensions:\n      - organization\n      - project\n      - environment\n  - name: logs_metrics\n    description: Logs and metrics ingested in GB (overage billed at $0.50/GB on Team/Business)\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - organization\n      - project\n  - name: spans\n    description: Tracing spans ingested\n    unit: span\n    aggregation: sum\n    dimensions:\n      - organization\n      - project\n  - name:\
  \ session_replays\n    description: Session Replay recordings ingested\n    unit: replay\n    aggregation: sum\n    dimensions:\n      - organization\n      - project\n  - name: uptime_monitors\n    description: Active uptime monitors / alerts (overage at $1.00/alert on Team/Business)\n    unit: alert\n    aggregation: sum\n    dimensions:\n      - organization\n  - name: cron_monitors\n    description: Active cron monitors (overage at $0.78/monitor on Team/Business)\n    unit: monitor\n    aggregation: sum\n    dimensions:\n      - organization\n  - name: subscription_fee\n    description: Recurring monthly plan fee (Team $26/mo, Business $80/mo, Enterprise custom)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\nprinciples:\n  - name: Visibility\n    description: Use the Stats / Usage page in the Sentry UI plus the /api/0/organizations/{org}/stats_v2/\n      endpoint to break consumption down by project, category (error/transaction/replay/log), and time\n      bucket.\
  \ Spending alerts can be configured from the same screen.\n  - name: Allocation\n    description: Sentry organizations and projects are the natural allocation units. Tag events with\n      release, environment, and team metadata to attribute consumption to product squads.\n  - name: Optimization\n    description: Use server-side and client-side sampling to control transaction/span volume; configure\n      inbound filters to drop noisy / non-actionable errors; tune session replay sample rate per project.\n      Advanced Quota Management on Business lets you cap per-project spend to prevent runaway billing.\n  - name: Accountability\n    description: Engineering owners of each project are accountable for their event volume. Platform\n      / SRE owns the org-level subscription and overage budget; finance reviews monthly Sentry invoice\n      against the plan.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sentry-system/refs/heads/main/finops/sentry-system-finops.yml
sources:
- https://sentry.io/pricing/
- https://docs.sentry.io/api/ratelimits/
specification: FinOps Framework
tags:
- Error Tracking
- Observability
- FinOps
- FOCUS
---
