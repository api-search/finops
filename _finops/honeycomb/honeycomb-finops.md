---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: honeycomb-api-openapi.yml
  format: yaml
  label: Honeycomb API
  slug: api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-api-openapi.yml
- filename: honeycomb-events-api-openapi.yml
  format: yaml
  label: Honeycomb Events API
  slug: events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-events-api-openapi.yml
- filename: honeycomb-queries-api-openapi.yml
  format: yaml
  label: Honeycomb Queries API
  slug: queries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-queries-api-openapi.yml
- filename: honeycomb-slos-api-openapi.yml
  format: yaml
  label: Honeycomb SLOs API
  slug: slos-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-slos-api-openapi.yml
- filename: honeycomb-datasets-api-openapi.yml
  format: yaml
  label: Honeycomb Datasets API
  slug: datasets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-datasets-api-openapi.yml
- filename: honeycomb-boards-api-openapi.yml
  format: yaml
  label: Honeycomb Boards API
  slug: boards-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-boards-api-openapi.yml
- filename: honeycomb-markers-api-openapi.yml
  format: yaml
  label: Honeycomb Markers API
  slug: markers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-markers-api-openapi.yml
- filename: honeycomb-triggers-api-openapi.yml
  format: yaml
  label: Honeycomb Triggers API
  slug: triggers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-triggers-api-openapi.yml
- filename: honeycomb-environments-api-openapi.yml
  format: yaml
  label: Honeycomb Environments API
  slug: environments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/openapi/honeycomb-environments-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Event Tiered Subscription
description: FOCUS-aligned FinOps for Honeycomb.
focus_columns:
  BillingCurrency: USD
  ProviderName: Honeycomb
  PublisherName: Honeycomb
  ServiceCategory: Observability
  ServiceName: Honeycomb
layout: finops
meters:
- aggregation: sum
  dimensions:
  - environment
  - dataset
  name: events_ingested
  unit: event
- aggregation: sum
  name: metrics_data_points
  unit: datapoint
- aggregation: max
  name: triggers_active
  unit: trigger-month
- aggregation: max
  name: slos_active
  unit: slo-month
name: Honeycomb Finops
provider_name: honeycomb
provider_slug: honeycomb
publisher_name: Honeycomb
service_category: Observability
slug: honeycomb-finops
source_filename: honeycomb-finops.yml
source_heading: FinOps Profile
source_url: https://www.honeycomb.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Honeycomb\nproviderId: honeycomb\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Observability\ndescription: FOCUS-aligned FinOps for Honeycomb.\nsources:\n  - https://www.honeycomb.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Honeycomb\nserviceCategory: Observability\nbillingModel:\n  pricingCategory: Per-Event Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Honeycomb\n  ServiceCategory: Observability\n  ProviderName: Honeycomb\n  PublisherName: Honeycomb\n  BillingCurrency: USD\nmeters:\n  - name: events_ingested\n    unit: event\n    aggregation: sum\n  \
  \  dimensions:\n      - environment\n      - dataset\n  - name: metrics_data_points\n    unit: datapoint\n    aggregation: sum\n  - name: triggers_active\n    unit: trigger-month\n    aggregation: max\n  - name: slos_active\n    unit: slo-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Honeycomb consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/honeycomb/refs/heads/main/finops/honeycomb-finops.yml
sources:
- https://www.honeycomb.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Observability
---
