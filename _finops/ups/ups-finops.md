---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ups-shipping-openapi.yml
  format: yaml
  label: UPS Shipping API
  slug: ups-shipping
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ups/refs/heads/main/openapi/ups-shipping-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for UPS.
focus_columns:
  BillingCurrency: USD
  ProviderName: UPS
  PublisherName: UPS
  ServiceCategory: Logistics / Shipping
  ServiceName: UPS
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  name: transactions
  unit: transaction
- aggregation: sum
  name: api_calls
  unit: call
- aggregation: max
  name: annual_contract
  unit: year
name: Ups Finops
provider_name: UPS
provider_slug: ups
publisher_name: UPS
service_category: Logistics / Shipping
slug: ups-finops
source_filename: ups-finops.yml
source_heading: FinOps Profile
source_url: https://developer.ups.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: UPS\nproviderId: ups\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Logistics / Shipping\ndescription: FOCUS-aligned FinOps for UPS.\nsources:\n  - https://developer.ups.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: UPS\nserviceCategory: Logistics / Shipping\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: UPS\n  ServiceCategory: Logistics / Shipping\n  ProviderName: UPS\n  PublisherName: UPS\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n  -\
  \ name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track UPS consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ups/refs/heads/main/finops/ups-finops.yml
sources:
- https://developer.ups.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Logistics / Shipping
---
