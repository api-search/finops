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
description: 'Galileo bills under bespoke contracts: monthly platform fees, per-transaction, per-card, ACH/RTP, plus interchange/interest economics shared with the sponsor bank.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Galileo
  ProviderName: Galileo
  PublisherName: Galileo
  ServiceCategory: BaaS
  ServiceName: Galileo
layout: finops
meters:
- aggregation: sum
  description: Card and account transactions processed.
  dimensions:
  - program
  - card_product
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
  description: ACH and RTP transfers.
  dimensions:
  - program
  - rail
  name: ach_rtp_transfers
  unit: transfer
- aggregation: sum
  description: Loan/credit draws.
  dimensions:
  - program
  name: loan_drawdowns
  unit: draw
name: Galileo Fs Finops
provider_name: Galileo Financial Technologies
provider_slug: galileo-fs
publisher_name: Galileo Financial Technologies, LLC (a SoFi company)
service_category: FinTech
slug: galileo-fs-finops
source_filename: galileo-fs-finops.yml
source_heading: FinOps Profile
source_url: https://www.galileo-ft.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Galileo Financial Technologies\nproviderId: galileo-fs\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- FinTech\n- BaaS\n- Card Issuing\n- Banking\n- Payments\n- ACH\n- FinOps\n- FOCUS\ndescription: 'Galileo bills under bespoke contracts: monthly platform fees, per-transaction,\n  per-card, ACH/RTP, plus interchange/interest economics shared with the sponsor bank.'\nnotes: Invoiced via Galileo (SoFi).\nsources:\n- https://www.galileo-ft.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Galileo Financial Technologies, LLC (a SoFi company)\nserviceCategory: FinTech\nbillingModel:\n  pricingCategory:\
  \ Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Galileo\n  ServiceCategory: BaaS\n  ProviderName: Galileo\n  PublisherName: Galileo\n  InvoiceIssuerName: Galileo\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: transactions\n  description: Card and account transactions processed.\n  unit: transaction\n  aggregation: sum\n  dimensions:\n  - program\n  - card_product\n- name: active_cards\n  description: Active cards.\n  unit: card\n  aggregation: max\n  dimensions:\n  - program\n  - card_product\n- name: ach_rtp_transfers\n  description: ACH and RTP transfers.\n  unit: transfer\n  aggregation: sum\n  dimensions:\n  - program\n  - rail\n- name: loan_drawdowns\n  description: Loan/credit draws.\n  unit: draw\n  aggregation: sum\n  dimensions:\n  - program\nprinciples:\n- name: Visibility\n  description: Pull Galileo reporting endpoints; use Events API\
  \ for streaming attribution.\n- name: Allocation\n  description: Tag accounts/cards per business unit; one program per cost center where\n    possible.\n- name: Optimization\n  description: Use Auth API rules to lower fraud declines; right-size card products;\n    choose RTP over ACH for time-sensitive flows.\n- name: Accountability\n  description: Program owners review monthly contract minimums vs activity.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/galileo-fs/refs/heads/main/finops/galileo-fs-finops.yml
sources:
- https://www.galileo-ft.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinTech
- BaaS
- Card Issuing
- Banking
- Payments
- ACH
- FinOps
- FOCUS
---
