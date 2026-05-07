---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: the-racing-api-openapi.yml
  format: yaml
  label: The Racing API
  slug: the-racing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/the-racing-api/refs/heads/main/openapi/the-racing-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Free / Donation-Funded
description: FOCUS-aligned FinOps for The Racing API.
focus_columns:
  BillingCurrency: USD
  ProviderName: The Racing API
  PublisherName: The Racing API
  ServiceCategory: Sports Data
  ServiceName: The Racing API
layout: finops
meters:
- aggregation: sum
  name: api_calls
  unit: call
name: The Racing Api Finops
provider_name: The Racing API
provider_slug: the-racing-api
publisher_name: The Racing API
service_category: Sports Data
slug: the-racing-api-finops
source_filename: the-racing-api-finops.yml
source_heading: FinOps Profile
source_url: https://theracingapi.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: The Racing API\nproviderId: the-racing-api\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Sports Data\ndescription: FOCUS-aligned FinOps for The Racing API.\nsources:\n  - https://theracingapi.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Racing API\nserviceCategory: Sports Data\nbillingModel:\n  pricingCategory: Free / Donation-Funded\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: The Racing API\n  ServiceCategory: Sports Data\n  ProviderName: The Racing API\n  PublisherName: The Racing API\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: call\n    aggregation:\
  \ sum\nprinciples:\n  - name: Visibility\n    description: Track The Racing API consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/the-racing-api/refs/heads/main/finops/the-racing-api-finops.yml
sources:
- https://theracingapi.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Sports Data
---
