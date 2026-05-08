---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Rollbar REST API
  slug: rollbar-rest-api
  spec_type: OpenAPI
  url: https://explorer.docs.rollbar.com/
- filename: rollbar-deployment-api-openapi.yml
  format: yaml
  label: Rollbar Deployment API
  slug: rollbar-deployment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rollbar/refs/heads/main/openapi/rollbar-deployment-api-openapi.yml
- filename: rollbar-metrics-api-openapi.yml
  format: yaml
  label: Rollbar Metrics API
  slug: rollbar-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rollbar/refs/heads/main/openapi/rollbar-metrics-api-openapi.yml
- filename: rollbar-rql-api-openapi.yml
  format: yaml
  label: Rollbar RQL API
  slug: rollbar-rql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rollbar/refs/heads/main/openapi/rollbar-rql-api-openapi.yml
- filename: rollbar-webhooks-asyncapi.yml
  format: yaml
  label: Rollbar Webhooks
  slug: rollbar-webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/rollbar/refs/heads/main/asyncapi/rollbar-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Tiered Subscription by Volume
description: FOCUS-aligned FinOps for Rollbar.
focus_columns:
  BillingCurrency: USD
  ProviderName: Rollbar
  PublisherName: Rollbar
  ServiceCategory: Error Monitoring
  ServiceName: Rollbar
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - environment
  name: occurrences
  unit: occurrence
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: sum
  name: credits_used
  unit: credit
- aggregation: max
  name: user_seats
  unit: seat-month
name: Rollbar Finops
provider_name: Rollbar
provider_slug: rollbar
publisher_name: Rollbar
service_category: Error Monitoring
slug: rollbar-finops
source_filename: rollbar-finops.yml
source_heading: FinOps Profile
source_url: https://rollbar.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Rollbar\nproviderId: rollbar\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Error Monitoring\ndescription: FOCUS-aligned FinOps for Rollbar.\nsources:\n  - https://rollbar.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Rollbar\nserviceCategory: Error Monitoring\nbillingModel:\n  pricingCategory: Tiered Subscription by Volume\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Rollbar\n  ServiceCategory: Error Monitoring\n  ProviderName: Rollbar\n  PublisherName: Rollbar\n  BillingCurrency: USD\nmeters:\n  - name: occurrences\n    unit: occurrence\n    aggregation: sum\n    dimensions:\n\
  \      - project\n      - environment\n  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: credits_used\n    unit: credit\n    aggregation: sum\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Rollbar consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rollbar/refs/heads/main/finops/rollbar-finops.yml
sources:
- https://rollbar.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Error Monitoring
---
