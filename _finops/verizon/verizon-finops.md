---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: verizon-thingspace-connectivity-openapi.yml
  format: yaml
  label: Verizon ThingSpace
  slug: thingspace
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/verizon/refs/heads/main/openapi/verizon-thingspace-connectivity-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for Verizon.
focus_columns:
  BillingCurrency: USD
  ProviderName: Verizon
  PublisherName: Verizon
  ServiceCategory: Telecommunications
  ServiceName: Verizon
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
name: Verizon Finops
provider_name: Verizon
provider_slug: verizon
publisher_name: Verizon
service_category: Telecommunications
slug: verizon-finops
source_filename: verizon-finops.yml
source_heading: FinOps Profile
source_url: https://thingspace.verizon.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Verizon\nproviderId: verizon\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Telecommunications\ndescription: FOCUS-aligned FinOps for Verizon.\nsources:\n  - https://thingspace.verizon.com/\n  - https://www.verizon.com/business/products/internet-of-things/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Verizon\nserviceCategory: Telecommunications\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Verizon\n  ServiceCategory: Telecommunications\n  ProviderName: Verizon\n  PublisherName: Verizon\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n\
  \    unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Verizon consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/verizon/refs/heads/main/finops/verizon-finops.yml
sources:
- https://thingspace.verizon.com/
- https://www.verizon.com/business/products/internet-of-things/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Telecommunications
---
