---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Quarterly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for AMG: investor-fee structures (management + performance) charged at the fund/account level by Affiliates.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AMG Affiliate (per fund)
  ProviderName: Affiliated Managers Group
  PublisherName: Affiliated Managers Group, Inc.
  ServiceCategory: Investment Management
  ServiceName: AMG Affiliate Funds
layout: finops
meters:
- aggregation: avg
  dimensions:
  - affiliate
  - fund
  name: assets_under_management
  unit: USD
- aggregation: sum
  dimensions:
  - affiliate
  - fund
  name: management_fee
  unit: USD
- aggregation: sum
  dimensions:
  - affiliate
  - fund
  name: performance_fee
  unit: USD
name: Affiliated Managers Group Finops
provider_name: Affiliated Managers Group
provider_slug: affiliated-managers-group
publisher_name: Affiliated Managers Group, Inc.
service_category: Investment Management
slug: affiliated-managers-group-finops
source_filename: affiliated-managers-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.amg.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Affiliated Managers Group\nproviderId: affiliated-managers-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AMG operates as a holding company for autonomous investment Affiliates. Costs to LPs\n  are fund-level management and performance fees, not API consumption.\ntags:\n  - FinOps\n  - FOCUS\n  - Asset Management\n  - Financial Services\ndescription: 'FOCUS-aligned FinOps for AMG: investor-fee structures (management + performance)\n  charged at the fund/account level by Affiliates.'\nsources:\n  - https://www.amg.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Affiliated Managers Group, Inc.\nserviceCategory: Investment Management\nbillingModel:\n\
  \  pricingCategory: Subscription\n  billingFrequency: Quarterly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: AMG Affiliate Funds\n  ServiceCategory: Investment Management\n  ProviderName: Affiliated Managers Group\n  PublisherName: Affiliated Managers Group, Inc.\n  InvoiceIssuerName: AMG Affiliate (per fund)\n  BillingCurrency: USD\nmeters:\n  - name: assets_under_management\n    unit: USD\n    aggregation: avg\n    dimensions:\n      - affiliate\n      - fund\n  - name: management_fee\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - affiliate\n      - fund\n  - name: performance_fee\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - affiliate\n      - fund\nprinciples:\n  - name: Visibility\n    description: Reconcile fund statements against custodial AUM data; track management/performance\n      fee accruals quarterly.\n  - name: Allocation\n    description: Attribute fees by mandate, account,\
  \ and affiliate.\n  - name: Optimization\n    description: Negotiate fee breakpoints at scale; consolidate share classes; review benchmark\n      alignment.\n  - name: Accountability\n    description: Assign investment-committee owner; quarterly fee variance review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/affiliated-managers-group/refs/heads/main/finops/affiliated-managers-group-finops.yml
sources:
- https://www.amg.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Asset Management
- Financial Services
---
