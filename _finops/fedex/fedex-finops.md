---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom B2B Contract
description: FOCUS-aligned FinOps for FedEx.
focus_columns:
  BillingCurrency: USD
  ProviderName: FedEx
  PublisherName: FedEx
  ServiceCategory: Logistics / Shipping
  ServiceName: FedEx
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
name: Fedex Finops
provider_name: FedEx
provider_slug: fedex
publisher_name: FedEx
service_category: Logistics / Shipping
slug: fedex-finops
source_filename: fedex-finops.yml
source_heading: FinOps Profile
source_url: https://developer.fedex.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: FedEx\nproviderId: fedex\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Logistics / Shipping\ndescription: FOCUS-aligned FinOps for FedEx.\nsources:\n  - https://developer.fedex.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: FedEx\nserviceCategory: Logistics / Shipping\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: FedEx\n  ServiceCategory: Logistics / Shipping\n  ProviderName: FedEx\n  PublisherName: FedEx\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n   \
  \   - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track FedEx consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fedex/refs/heads/main/finops/fedex-finops.yml
sources:
- https://developer.fedex.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Logistics / Shipping
---
