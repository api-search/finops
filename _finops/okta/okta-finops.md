---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: okta-openapi-original.yml
  format: yaml
  label: Okta API
  slug: okta-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/okta/refs/heads/main/openapi/okta-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription
description: FOCUS-aligned FinOps for Okta.
focus_columns:
  BillingCurrency: USD
  ProviderName: Okta
  PublisherName: Okta
  ServiceCategory: Identity
  ServiceName: Okta
layout: finops
meters:
- aggregation: max
  dimensions:
  - sku
  name: user_licenses
  unit: license-month
- aggregation: sum
  name: workflow_executions
  unit: execution
- aggregation: max
  name: device_licenses
  unit: device-month
- aggregation: sum
  name: api_requests
  unit: request
name: Okta Finops
provider_name: Okta
provider_slug: okta
publisher_name: Okta
service_category: Identity
slug: okta-finops
source_filename: okta-finops.yml
source_heading: FinOps Profile
source_url: https://www.okta.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Okta\nproviderId: okta\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Identity\ndescription: FOCUS-aligned FinOps for Okta.\nsources:\n  - https://www.okta.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Okta\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Per-User Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Okta\n  ServiceCategory: Identity\n  ProviderName: Okta\n  PublisherName: Okta\n  BillingCurrency: USD\nmeters:\n  - name: user_licenses\n    unit: license-month\n    aggregation: max\n    dimensions:\n      - sku\n  - name: workflow_executions\n\
  \    unit: execution\n    aggregation: sum\n  - name: device_licenses\n    unit: device-month\n    aggregation: max\n  - name: api_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Okta consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/okta/refs/heads/main/finops/okta-finops.yml
sources:
- https://www.okta.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Identity
---
