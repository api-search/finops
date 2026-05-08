---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for AES/Fluence: enterprise software subscription with per-asset pricing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Fluence Energy, Inc.
  ProviderName: AES Corporation / Fluence
  PublisherName: Fluence Energy, Inc.
  ServiceCategory: Energy Asset Management
  ServiceName: Fluence (AES)
layout: finops
meters:
- aggregation: max
  dimensions:
  - asset_type
  - region
  name: managed_assets_mw
  unit: MW
- aggregation: sum
  dimensions:
  - tenant
  - environment
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - product
  name: subscription_fees
  unit: year
name: Aes Finops
provider_name: AES Corporation
provider_slug: aes
publisher_name: Fluence Energy, Inc.
service_category: Energy / Asset Management Software
slug: aes-finops
source_filename: aes-finops.yml
source_heading: FinOps Profile
source_url: https://fluenceenergy.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AES Corporation\nproviderId: aes\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AES sells power; Fluence sells software under enterprise contracts. FinOps mapping reflects\n  Fluence enterprise software subscription billing.\ntags:\n  - FinOps\n  - FOCUS\n  - Energy\n  - Battery Storage\ndescription: 'FOCUS-aligned FinOps for AES/Fluence: enterprise software subscription with\n  per-asset pricing.'\nsources:\n  - https://fluenceenergy.com/\n  - https://www.aes.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fluence Energy, Inc.\nserviceCategory: Energy / Asset Management Software\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency:\
  \ Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Fluence (AES)\n  ServiceCategory: Energy Asset Management\n  ProviderName: AES Corporation / Fluence\n  PublisherName: Fluence Energy, Inc.\n  InvoiceIssuerName: Fluence Energy, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: managed_assets_mw\n    unit: MW\n    aggregation: max\n    dimensions:\n      - asset_type\n      - region\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tenant\n      - environment\n  - name: subscription_fees\n    unit: year\n    aggregation: sum\n    dimensions:\n      - product\nprinciples:\n  - name: Visibility\n    description: Reconcile annual Fluence invoices against managed-asset MW figures and the SOW\n      schedule.\n  - name: Allocation\n    description: Tag spend per asset portfolio and operating company.\n  - name: Optimization\n    description: Right-size Mosaic vs Nispera coverage to active\
  \ assets; renegotiate at renewal\n      based on portfolio size.\n  - name: Accountability\n    description: Assign portfolio-software owner; review annual renewal exposure.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aes/refs/heads/main/finops/aes-finops.yml
sources:
- https://fluenceenergy.com/
- https://www.aes.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy
- Battery Storage
---
