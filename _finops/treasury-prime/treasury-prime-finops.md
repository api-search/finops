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
description: 'Treasury Prime bills under contract: monthly platform fee, per-transaction, per-card, ACH/wire, with deposit-share economics with the partner bank.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Treasury Prime
  ProviderName: Treasury Prime
  PublisherName: Treasury Prime
  ServiceCategory: BaaS
  ServiceName: Treasury Prime
layout: finops
meters:
- aggregation: sum
  description: Account transactions processed.
  dimensions:
  - program
  - bank
  name: transactions
  unit: transaction
- aggregation: max
  description: Active cards.
  dimensions:
  - program
  name: active_cards
  unit: card
- aggregation: sum
  description: ACH transfers.
  dimensions:
  - program
  name: ach_transfers
  unit: transfer
name: Treasury Prime Finops
provider_name: Treasury Prime
provider_slug: treasury-prime
publisher_name: Treasury Prime
service_category: FinTech
slug: treasury-prime-finops
source_filename: treasury-prime-finops.yml
source_heading: FinOps Profile
source_url: https://www.treasuryprime.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Treasury Prime\nproviderId: treasury-prime\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- FinTech\n- BaaS\n- Banking\n- Payments\n- Card Issuing\n- ACH\n- FinOps\n- FOCUS\ndescription: 'Treasury Prime bills under contract: monthly platform fee, per-transaction,\n  per-card, ACH/wire, with deposit-share economics with the partner bank.'\nnotes: Invoiced via Treasury Prime.\nsources:\n- https://www.treasuryprime.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Treasury Prime\nserviceCategory: FinTech\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Treasury Prime\n  ServiceCategory: BaaS\n  ProviderName: Treasury Prime\n  PublisherName: Treasury Prime\n  InvoiceIssuerName: Treasury Prime\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: transactions\n  description: Account transactions processed.\n  unit: transaction\n  aggregation: sum\n  dimensions:\n  - program\n  - bank\n- name: active_cards\n  description: Active cards.\n  unit: card\n  aggregation: max\n  dimensions:\n  - program\n- name: ach_transfers\n  description: ACH transfers.\n  unit: transfer\n  aggregation: sum\n  dimensions:\n  - program\nprinciples:\n- name: Visibility\n  description: Use Treasury Prime reporting endpoints and statements API.\n- name: Allocation\n  description: Tag accounts and cards per business unit.\n- name: Optimization\n  description: Use book transfers within the network where possible.\n- name: Accountability\n  description:\
  \ Program owners review fees vs minimums.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/treasury-prime/refs/heads/main/finops/treasury-prime-finops.yml
sources:
- https://www.treasuryprime.com/
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
