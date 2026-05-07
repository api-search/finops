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
description: FOCUS-aligned FinOps for Mastercard.
focus_columns:
  BillingCurrency: USD
  ProviderName: Mastercard
  PublisherName: Mastercard
  ServiceCategory: Payment Network
  ServiceName: Mastercard
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
name: Mastercard Finops
provider_name: Mastercard
provider_slug: mastercard
publisher_name: Mastercard
service_category: Payment Network
slug: mastercard-finops
source_filename: mastercard-finops.yml
source_heading: FinOps Profile
source_url: https://developer.mastercard.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mastercard\nproviderId: mastercard\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Payment Network\ndescription: FOCUS-aligned FinOps for Mastercard.\nsources:\n  - https://developer.mastercard.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mastercard\nserviceCategory: Payment Network\nbillingModel:\n  pricingCategory: Custom B2B Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Mastercard\n  ServiceCategory: Payment Network\n  ProviderName: Mastercard\n  PublisherName: Mastercard\n  BillingCurrency: USD\nmeters:\n  - name: transactions\n    unit: transaction\n    aggregation: sum\n\
  \    dimensions:\n      - product\n  - name: api_calls\n    unit: call\n    aggregation: sum\n  - name: annual_contract\n    unit: year\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Mastercard consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers for chargeback.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mastercard/refs/heads/main/finops/mastercard-finops.yml
sources:
- https://developer.mastercard.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payment Network
---
