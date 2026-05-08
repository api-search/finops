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
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'Unit bills under contract: monthly platform fee, per-transaction, per-card, ACH/wire, plus interest revenue share. SDKs and OpenAPI available for cost attribution.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Unit
  ProviderName: Unit
  PublisherName: Unit
  ServiceCategory: BaaS
  ServiceName: Unit
layout: finops
meters:
- aggregation: sum
  description: Account transactions processed.
  dimensions:
  - org
  - account_type
  name: transactions
  unit: transaction
- aggregation: max
  description: Active cards.
  dimensions:
  - org
  - card_product
  name: active_cards
  unit: card
- aggregation: sum
  description: ACH transfers.
  dimensions:
  - org
  name: ach_transfers
  unit: transfer
name: Unit Finops
provider_name: Unit
provider_slug: unit
publisher_name: Unit Finance, Inc.
service_category: FinTech
slug: unit-finops
source_filename: unit-finops.yml
source_heading: FinOps Profile
source_url: https://www.unit.co/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Unit\nproviderId: unit\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- FinTech\n- BaaS\n- Banking\n- Payments\n- Card Issuing\n- ACH\n- FinOps\n- FOCUS\ndescription: 'Unit bills under contract: monthly platform fee, per-transaction, per-card,\n  ACH/wire, plus interest revenue share. SDKs and OpenAPI available for cost attribution.'\nnotes: Invoiced via Unit.\nsources:\n- https://www.unit.co/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Unit Finance, Inc.\nserviceCategory: FinTech\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Unit\n  ServiceCategory: BaaS\n  ProviderName: Unit\n  PublisherName: Unit\n  InvoiceIssuerName: Unit\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: transactions\n  description: Account transactions processed.\n  unit: transaction\n  aggregation: sum\n  dimensions:\n  - org\n  - account_type\n- name: active_cards\n  description: Active cards.\n  unit: card\n  aggregation: max\n  dimensions:\n  - org\n  - card_product\n- name: ach_transfers\n  description: ACH transfers.\n  unit: transfer\n  aggregation: sum\n  dimensions:\n  - org\nprinciples:\n- name: Visibility\n  description: Pull Unit transaction and statements APIs to attribute costs to customers.\n- name: Allocation\n  description: Use Unit tags on resources to attribute by business unit.\n- name: Optimization\n  description: Right-size card programs; book transfers when possible.\n- name: Accountability\n  description: Org owners review monthly\
  \ fees vs contract minimums.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unit/refs/heads/main/finops/unit-finops.yml
sources:
- https://www.unit.co/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinTech
- BaaS
- Banking
- Payments
- Card Issuing
- ACH
- FinOps
- FOCUS
---
