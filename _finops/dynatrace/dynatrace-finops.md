---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dynatrace-metrics-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Metrics API v2
  slug: dynatrace-metrics-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-metrics-api-v2-openapi.yml
- filename: dynatrace-log-monitoring-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Log Monitoring API v2
  slug: dynatrace-log-monitoring-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-log-monitoring-api-v2-openapi.yml
- filename: dynatrace-account-management-api-openapi.yml
  format: yaml
  label: Dynatrace Account Management API
  slug: dynatrace-account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-account-management-api-openapi.yml
- filename: dynatrace-events-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Events API v2
  slug: dynatrace-events-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-events-api-v2-openapi.yml
- filename: dynatrace-problems-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Problems API v2
  slug: dynatrace-problems-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-problems-api-v2-openapi.yml
- filename: dynatrace-entities-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Entities API v2
  slug: dynatrace-entities-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-entities-api-v2-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Dynatrace: per-host/pod/container subscriptions plus consumption meters (GiB ingest/retain/query, sessions, synthetic actions) on the Grail platform.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Dynatrace LLC
  PricingUnit: GiB-hour / pod-hour / container-hour / session / GiB
  ProviderName: Dynatrace
  PublisherName: Dynatrace LLC
  ServiceCategory: Observability
  ServiceName: Dynatrace
layout: finops
meters:
- aggregation: sum
  dimensions:
  - capability
  - host_size
  - environment
  name: host_hours
  unit: host-hour
- aggregation: sum
  dimensions:
  - host
  - environment
  name: full_stack_gib_hours
  unit: GiB-hour
- aggregation: sum
  dimensions:
  - cluster
  - namespace
  name: pod_hours
  unit: pod-hour
- aggregation: sum
  dimensions:
  - cluster
  - workload
  name: container_hours
  unit: container-hour
- aggregation: sum
  dimensions:
  - bucket
  - source
  name: log_ingest
  unit: GiB
- aggregation: avg
  dimensions:
  - bucket
  name: log_retain
  unit: GiB-day
- aggregation: sum
  dimensions:
  - app
  name: log_query_scanned
  unit: GiB
- aggregation: sum
  dimensions:
  - source
  - dimension_count
  name: metric_datapoints
  unit: datapoint
- aggregation: sum
  dimensions:
  - app
  - replay
  name: rum_sessions
  unit: session
- aggregation: sum
  dimensions:
  - monitor_type
  - location
  name: synthetic_executions
  unit: action
- aggregation: sum
  dimensions:
  - capability
  name: appsec_host_months
  unit: host-month
name: Dynatrace Finops
provider_name: Dynatrace
provider_slug: dynatrace
publisher_name: Dynatrace LLC
service_category: Observability
slug: dynatrace-finops
source_filename: dynatrace-finops.yml
source_heading: FinOps Profile
source_url: https://www.dynatrace.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Dynatrace\nproviderId: dynatrace\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\n  - APM\ndescription: 'FOCUS-aligned FinOps for Dynatrace: per-host/pod/container subscriptions plus consumption\n  meters (GiB ingest/retain/query, sessions, synthetic actions) on the Grail platform.'\nsources:\n  - https://www.dynatrace.com/pricing/\n  - https://docs.dynatrace.com/docs/manage/subscription\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dynatrace LLC\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Dynatrace\n  ServiceCategory: Observability\n  ProviderName: Dynatrace\n  PublisherName: Dynatrace LLC\n  InvoiceIssuerName: Dynatrace LLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: GiB-hour / pod-hour / container-hour / session / GiB\nmeters:\n  - name: host_hours\n    unit: host-hour\n    aggregation: sum\n    dimensions:\n      - capability\n      - host_size\n      - environment\n  - name: full_stack_gib_hours\n    unit: GiB-hour\n    aggregation: sum\n    dimensions:\n      - host\n      - environment\n  - name: pod_hours\n    unit: pod-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - namespace\n  - name: container_hours\n    unit: container-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - workload\n  - name: log_ingest\n    unit: GiB\n    aggregation: sum\n    dimensions:\n\
  \      - bucket\n      - source\n  - name: log_retain\n    unit: GiB-day\n    aggregation: avg\n    dimensions:\n      - bucket\n  - name: log_query_scanned\n    unit: GiB\n    aggregation: sum\n    dimensions:\n      - app\n  - name: metric_datapoints\n    unit: datapoint\n    aggregation: sum\n    dimensions:\n      - source\n      - dimension_count\n  - name: rum_sessions\n    unit: session\n    aggregation: sum\n    dimensions:\n      - app\n      - replay\n  - name: synthetic_executions\n    unit: action\n    aggregation: sum\n    dimensions:\n      - monitor_type\n      - location\n  - name: appsec_host_months\n    unit: host-month\n    aggregation: sum\n    dimensions:\n      - capability\nprinciples:\n  - name: Visibility\n    description: Use the Account Management API and Subscription page to track DDU/DPS consumption and\n      per-capability usage; export usage reports to your data lake for FOCUS mapping.\n  - name: Allocation\n    description: Tag hosts, services, and Grail\
  \ buckets with management-zone, team, environment, and\n      cost-center metadata; use Dynatrace Cost Allocation app for chargeback.\n  - name: Optimization\n    description: Tune log ingest with OpenPipeline filters, set retention policies per Grail bucket, downsample\n      metrics, and prefer Infrastructure Monitoring over Full-Stack on non-app hosts.\n  - name: Accountability\n    description: Set DPS budget thresholds and Davis anomaly alerts; review monthly subscription consumption\n      against forecast and chargeback to product teams.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/finops/dynatrace-finops.yml
sources:
- https://www.dynatrace.com/pricing/
- https://docs.dynatrace.com/docs/manage/subscription
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
- APM
---
