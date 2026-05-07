---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: datadog-api-openapi.yml
  format: yaml
  label: Datadog API
  slug: datadog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-api-openapi.yml
- filename: datadog-metrics-openapi.yml
  format: yaml
  label: Datadog Metrics API
  slug: datadog-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-metrics-openapi.yml
- filename: datadog-logs-openapi.yml
  format: yaml
  label: Datadog Logs API
  slug: datadog-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-logs-openapi.yml
- filename: datadog-events-openapi.yml
  format: yaml
  label: Datadog Events API
  slug: datadog-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-events-openapi.yml
- filename: datadog-monitors-openapi.yml
  format: yaml
  label: Datadog Monitors API
  slug: datadog-monitors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-monitors-openapi.yml
- filename: datadog-incidents-openapi.yml
  format: yaml
  label: Datadog Incidents API
  slug: datadog-incidents-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/openapi/datadog-incidents-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Subscription + Usage-Based
description: 'FOCUS-aligned FinOps for Datadog: per-host subscriptions plus metered usage for logs, custom metrics, traces, and synthetics.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Datadog, Inc.
  ProviderName: Datadog
  PublisherName: Datadog, Inc.
  ServiceCategory: Observability
  ServiceName: Datadog
layout: finops
meters:
- aggregation: sum
  dimensions:
  - org
  - tag
  - host_type
  name: infra_hosts
  unit: host-hour
- aggregation: sum
  name: apm_hosts
  unit: host-hour
- aggregation: sum
  dimensions:
  - org
  - service
  - source
  name: log_ingest_gb
  unit: GB
- aggregation: sum
  dimensions:
  - index
  - retention
  name: log_indexed_events
  unit: million_events
- aggregation: max
  dimensions:
  - org
  - namespace
  name: custom_metrics
  unit: metric
- aggregation: sum
  dimensions:
  - test_type
  - location
  name: synthetic_test_runs
  unit: test_run
- aggregation: sum
  name: rum_sessions
  unit: session
- aggregation: max
  name: ci_pipeline_committers
  unit: committer
name: Datadog Finops
provider_name: Datadog
provider_slug: datadog
publisher_name: Datadog, Inc.
service_category: Observability
slug: datadog-finops
source_filename: datadog-finops.yml
source_heading: FinOps Profile
source_url: https://www.datadoghq.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Datadog\nproviderId: datadog\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\n  - Observability\ndescription: 'FOCUS-aligned FinOps for Datadog: per-host subscriptions plus metered usage for logs, custom\n  metrics, traces, and synthetics.'\nsources:\n  - https://www.datadoghq.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Datadog, Inc.\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName:\
  \ Datadog\n  ServiceCategory: Observability\n  ProviderName: Datadog\n  PublisherName: Datadog, Inc.\n  InvoiceIssuerName: Datadog, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: infra_hosts\n    unit: host-hour\n    aggregation: sum\n    dimensions:\n      - org\n      - tag\n      - host_type\n  - name: apm_hosts\n    unit: host-hour\n    aggregation: sum\n  - name: log_ingest_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - org\n      - service\n      - source\n  - name: log_indexed_events\n    unit: million_events\n    aggregation: sum\n    dimensions:\n      - index\n      - retention\n  - name: custom_metrics\n    unit: metric\n    aggregation: max\n    dimensions:\n      - org\n      - namespace\n  - name: synthetic_test_runs\n    unit: test_run\n    aggregation: sum\n    dimensions:\n      - test_type\n      - location\n  - name: rum_sessions\n    unit: session\n    aggregation: sum\n  - name: ci_pipeline_committers\n    unit: committer\n    aggregation: max\n\
  principles:\n  - name: Visibility\n    description: Use Usage Metering and Cost Management for granular spend by team/service.\n  - name: Allocation\n    description: Apply consistent host tags (env, team, service) to enable team-level chargeback.\n  - name: Optimization\n    description: Drop unneeded log fields at ingest, use Flex storage for cold logs, prune high-cardinality\n      custom metrics.\n  - name: Accountability\n    description: Set per-team usage budgets and weekly reviews of Cost Management dashboard.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datadog/refs/heads/main/finops/datadog-finops.yml
sources:
- https://www.datadoghq.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
- Observability
---
