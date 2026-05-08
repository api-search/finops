---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: new-relic-openapi.yml
  format: yaml
  label: New Relic REST API v2
  slug: new-relic-rest-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-openapi.yml
- filename: new-relic-metric-api-openapi.yml
  format: yaml
  label: New Relic Metric API
  slug: new-relic-metric-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-metric-api-openapi.yml
- filename: new-relic-event-api-openapi.yml
  format: yaml
  label: New Relic Event API
  slug: new-relic-event-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-event-api-openapi.yml
- filename: new-relic-log-api-openapi.yml
  format: yaml
  label: New Relic Log API
  slug: new-relic-log-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-log-api-openapi.yml
- filename: new-relic-trace-api-openapi.yml
  format: yaml
  label: New Relic Trace API
  slug: new-relic-trace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/openapi/new-relic-trace-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User + Per-GB Ingest
description: FOCUS-aligned FinOps for New Relic.
focus_columns:
  BillingCurrency: USD
  ProviderName: New Relic
  PublisherName: New Relic
  ServiceCategory: Observability
  ServiceName: New Relic
layout: finops
meters:
- aggregation: sum
  dimensions:
  - data_type
  - account
  name: data_ingest
  unit: GB
- aggregation: max
  dimensions:
  - edition
  name: full_platform_users
  unit: user-month
- aggregation: max
  name: basic_users
  unit: user-month
- aggregation: sum
  name: synthetics_checks
  unit: check
name: New Relic Finops
provider_name: New Relic
provider_slug: new-relic
publisher_name: New Relic
service_category: Observability
slug: new-relic-finops
source_filename: new-relic-finops.yml
source_heading: FinOps Profile
source_url: https://newrelic.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: New Relic\nproviderId: new-relic\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\ndescription: FOCUS-aligned FinOps for New Relic.\nsources:\n  - https://newrelic.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: New Relic\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Per-User + Per-GB Ingest\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: New Relic\n  ServiceCategory: Observability\n  ProviderName: New Relic\n  PublisherName: New Relic\n  BillingCurrency: USD\nmeters:\n  - name: data_ingest\n    unit: GB\n    aggregation: sum\n    dimensions:\n \
  \     - data_type\n      - account\n  - name: full_platform_users\n    unit: user-month\n    aggregation: max\n    dimensions:\n      - edition\n  - name: basic_users\n    unit: user-month\n    aggregation: max\n  - name: synthetics_checks\n    unit: check\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track New Relic consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/new-relic/refs/heads/main/finops/new-relic-finops.yml
sources:
- https://newrelic.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
---
