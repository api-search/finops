---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: synctera-openapi.json
  format: json
  label: Synctera Platform API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/synctera/refs/heads/main/openapi/synctera-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'Synctera bills under contract: monthly platform fee, per-transaction, per-card, ACH/wire, plus interest revenue share.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Synctera
  ProviderName: Synctera
  PublisherName: Synctera
  ServiceCategory: BaaS
  ServiceName: Synctera
layout: finops
meters:
- aggregation: sum
  description: Account transactions processed.
  dimensions:
  - program
  - account_type
  name: transactions
  unit: transaction
- aggregation: max
  description: Active cards.
  dimensions:
  - program
  - card_product
  name: active_cards
  unit: card
- aggregation: sum
  description: KYC/KYB verification calls.
  dimensions:
  - program
  name: kyc_verifications
  unit: verification
name: Synctera Finops
provider_name: Synctera
provider_slug: synctera
publisher_name: Synctera, Inc.
service_category: FinTech
slug: synctera-finops
source_filename: synctera-finops.yml
source_heading: FinOps Profile
source_url: https://synctera.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Synctera\nproviderId: synctera\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- FinTech\n- BaaS\n- Banking\n- Payments\n- Card Issuing\n- KYC\n- FinOps\n- FOCUS\ndescription: 'Synctera bills under contract: monthly platform fee, per-transaction,\n  per-card, ACH/wire, plus interest revenue share.'\nnotes: Invoiced via Synctera.\nsources:\n- https://synctera.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Synctera, Inc.\nserviceCategory: FinTech\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n\
  \  - Adjustment\nfocusColumns:\n  ServiceName: Synctera\n  ServiceCategory: BaaS\n  ProviderName: Synctera\n  PublisherName: Synctera\n  InvoiceIssuerName: Synctera\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: transactions\n  description: Account transactions processed.\n  unit: transaction\n  aggregation: sum\n  dimensions:\n  - program\n  - account_type\n- name: active_cards\n  description: Active cards.\n  unit: card\n  aggregation: max\n  dimensions:\n  - program\n  - card_product\n- name: kyc_verifications\n  description: KYC/KYB verification calls.\n  unit: verification\n  aggregation: sum\n  dimensions:\n  - program\nprinciples:\n- name: Visibility\n  description: Use Synctera Console reporting and the API to track costs.\n- name: Allocation\n  description: Tag resources by business unit.\n- name: Optimization\n  description: Right-size card products; choose internal transfers over ACH where\n    possible.\n- name: Accountability\n  description: Program owners\
  \ review monthly contract minimums.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/synctera/refs/heads/main/finops/synctera-finops.yml
sources:
- https://synctera.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinTech
- BaaS
- Banking
- Payments
- Card Issuing
- KYC
- FinOps
- FOCUS
---
