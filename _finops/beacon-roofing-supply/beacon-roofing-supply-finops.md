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
  label: Beacon PRO+ API
  slug: beacon-pro-plus
  spec_type: OpenAPI
  url: https://beaconproplus.com/swagger/all_api/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Account-Based Material Spend
description: 'FOCUS-aligned FinOps shape for Beacon PRO+: API access bundled with the contractor account, with the dominant cost category being underlying material purchases and delivery fees rather than API consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Beacon Roofing Supply, Inc.
  PricingCategory: Account-Based Material Spend
  PricingUnit: order
  ProviderName: Beacon Roofing Supply
  PublisherName: Beacon Roofing Supply, Inc.
  ServiceCategory: Construction Distribution / E-Commerce APIs
  ServiceName: Beacon PRO+
layout: finops
meters:
- aggregation: sum
  description: Orders placed through the PRO+ API
  dimensions:
  - account
  - job
  - branch
  name: orders
  unit: order
- aggregation: sum
  description: Material spend value via the PRO+ API
  dimensions:
  - account
  - job
  - product_category
  name: order_volume
  unit: USD
- aggregation: sum
  description: Delivery events tracked via the API
  dimensions:
  - account
  - branch
  name: deliveries
  unit: delivery
- aggregation: sum
  description: Manufacturer rebates accrued / surfaced through the API
  dimensions:
  - manufacturer
  - product_category
  name: rebates
  unit: USD
name: Beacon Roofing Supply Finops
provider_name: Beacon Roofing Supply
provider_slug: beacon-roofing-supply
publisher_name: Beacon Roofing Supply, Inc. (a QXO company)
service_category: Construction Distribution / E-Commerce APIs
slug: beacon-roofing-supply-finops
source_filename: beacon-roofing-supply-finops.yml
source_heading: FinOps Profile
source_url: https://beaconproplus.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Beacon Roofing Supply\nproviderId: beacon-roofing-supply\npublisherName: Beacon Roofing Supply, Inc. (a QXO company)\nserviceCategory: Construction Distribution / E-Commerce APIs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Construction\n  - Roofing\n  - Distribution\n  - E-Commerce\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Beacon PRO+: API access bundled with the contractor account,\n  with the dominant cost category being underlying material purchases and delivery fees rather than API\n  consumption.'\nnotes: No public rate card. Replace meter values with the contractor's negotiated Beacon account terms\n  and ISV integration scope\
  \ once available.\nsources:\n  - https://beaconproplus.com\n  - https://beaconproplus.com/swagger/all_api/\nprinciples:\n  - name: Visibility\n    description: Use the PRO+ API to surface order, delivery, and rebate data to the contractor's job-cost\n      ledger so material spend can be attributed per job.\n  - name: Allocation\n    description: Allocate material orders to jobs / projects via contractor PO and job-number metadata\n      passed through the API.\n  - name: Optimization\n    description: Optimize delivery scheduling and consolidate orders to minimize delivery fees; track\n      manufacturer rebates through the API to capture the full earned value.\n  - name: Accountability\n    description: Designate a project manager or operations lead as the Beacon account owner who reviews\n      monthly statements and rebate accruals.\nbillingModel:\n  pricingCategory: Account-Based Material Spend\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Beacon PRO+\n  ServiceCategory: Construction Distribution / E-Commerce APIs\n  ProviderName: Beacon Roofing Supply\n  PublisherName: Beacon Roofing Supply, Inc.\n  InvoiceIssuerName: Beacon Roofing Supply, Inc.\n  PricingCategory: Account-Based Material Spend\n  PricingUnit: order\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: orders\n    description: Orders placed through the PRO+ API\n    unit: order\n    aggregation: sum\n    dimensions:\n      - account\n      - job\n      - branch\n  - name: order_volume\n    description: Material spend value via the PRO+ API\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account\n      - job\n      - product_category\n  - name: deliveries\n    description: Delivery events tracked via the API\n    unit: delivery\n    aggregation: sum\n    dimensions:\n      - account\n      - branch\n  - name:\
  \ rebates\n    description: Manufacturer rebates accrued / surfaced through the API\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - manufacturer\n      - product_category\napis:\n  - name: Beacon PRO+ API\n    baseURL: ''\n    tags:\n      - Construction\n      - Roofing\n      - Distribution\n      - E-Commerce\n    serviceName: Beacon PRO+ API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Job\n    metric: order_volume / active_jobs\n    target: align to job estimate\n  - name: Rebate Capture Rate\n    metric: rebates / order_volume\n    target: maximize per manufacturer program\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/beacon-roofing-supply/refs/heads/main/finops/beacon-roofing-supply-finops.yml
sources:
- https://beaconproplus.com
- https://beaconproplus.com/swagger/all_api/
specification: FinOps Framework
tags:
- Construction
- Roofing
- Distribution
- E-Commerce
- FinOps
- FOCUS
---
