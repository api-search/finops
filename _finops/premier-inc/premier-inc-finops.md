---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Contract / Custom
description: FOCUS-aligned FinOps placeholder for Premier Inc. The provider does not publish a public API pricing surface, so there are no documented meters or unit prices to align to FOCUS. Any cost allocation lives inside the bilateral partner / member contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Premier, Inc.
  ProviderName: Premier Inc
  PublisherName: Premier, Inc.
  ServiceCategory: Healthcare
  ServiceName: Premier Inc
  ServiceSubcategory: Group Purchasing and Healthcare Analytics
layout: finops
meters:
- aggregation: sum
  description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.
  dimensions:
  - contract
  - department
  name: contract_fee
  unit: varies
name: Premier Inc Finops
provider_name: Premier Inc
provider_slug: premier-inc
publisher_name: Premier, Inc.
service_category: Healthcare
slug: premier-inc-finops
source_filename: premier-inc-finops.yml
source_heading: FinOps Profile
source_url: https://premierinc.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Premier Inc\nproviderId: premier-inc\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Group Purchasing\n  - Analytics\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps placeholder for Premier Inc. The provider does not publish\n  a public API pricing surface, so there are no documented meters or unit\n  prices to align to FOCUS. Any cost allocation lives inside the bilateral\n  partner / member contract.\nsources:\n  - https://premierinc.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Premier, Inc.\nserviceCategory: Healthcare\nbillingModel:\n  pricingCategory: Contract / Custom\n  billingFrequency: Per-Contract\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Premier Inc\n  ServiceCategory: Healthcare\n  ServiceSubcategory: Group Purchasing and Healthcare Analytics\n  ProviderName: Premier Inc\n  PublisherName: Premier, Inc.\n  InvoiceIssuerName: Premier, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contract_fee\n    description: Negotiated contract fee or member dues; the actual unit (per-month, per-transaction, percent-of-spend) is defined in the executed agreement.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - department\nprinciples:\n  - name: Visibility\n    description: Cost visibility for Premier Inc comes from the negotiated contract artifacts and the consuming organization's AP / procurement system rather than from a provider usage API.\n  - name: Allocation\n    description: Allocate by the cost center or business unit listed on the contract; there is no\
  \ provider-side tag surface.\n  - name: Optimization\n    description: Renegotiate at renewal; consolidate purchasing through procurement; benchmark against peer organizations where possible.\n  - name: Accountability\n    description: The contract owner / category manager is accountable for spend; review at the contract renewal cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\nnotes: >-\n  No public pricing or billing documentation exists. Reconciled=false\n  because there is nothing publicly published to align to FOCUS columns or\n  meters.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/premier-inc/refs/heads/main/finops/premier-inc-finops.yml
sources:
- https://premierinc.com/
specification: FinOps Framework
tags:
- Healthcare
- Group Purchasing
- Analytics
- FinOps
- FOCUS
---
