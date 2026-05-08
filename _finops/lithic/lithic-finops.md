---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lithic-openapi.yml
  format: yaml
  label: Lithic REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lithic/refs/heads/main/openapi/lithic-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: 'Lithic bills under contract: monthly platform fee, per-transaction, per-card, ACH/wire, dispute, plus interchange share.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lithic
  ProviderName: Lithic
  PublisherName: Lithic
  ServiceCategory: Card Issuing
  ServiceName: Lithic
layout: finops
meters:
- aggregation: sum
  description: Card transactions processed.
  dimensions:
  - program
  - card_product
  name: transactions
  unit: transaction
- aggregation: max
  description: Active cards (physical / virtual).
  dimensions:
  - program
  - card_product
  name: cards_active
  unit: card
- aggregation: sum
  description: ACH transfer count.
  dimensions:
  - program
  name: ach_transfers
  unit: transfer
- aggregation: sum
  description: Wire transfer count.
  dimensions:
  - program
  name: wire_transfers
  unit: transfer
name: Lithic Finops
provider_name: Lithic
provider_slug: lithic
publisher_name: Lithic, Inc.
service_category: FinTech
slug: lithic-finops
source_filename: lithic-finops.yml
source_heading: FinOps Profile
source_url: https://lithic.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lithic\nproviderId: lithic\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- FinTech\n- BaaS\n- Card Issuing\n- Payments\n- Embedded Finance\n- FinOps\n- FOCUS\ndescription: 'Lithic bills under contract: monthly platform fee, per-transaction,\n  per-card, ACH/wire, dispute, plus interchange share.'\nnotes: Invoiced via Lithic.\nsources:\n- https://lithic.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lithic, Inc.\nserviceCategory: FinTech\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n\
  \  - Adjustment\nfocusColumns:\n  ServiceName: Lithic\n  ServiceCategory: Card Issuing\n  ProviderName: Lithic\n  PublisherName: Lithic\n  InvoiceIssuerName: Lithic\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: transactions\n  description: Card transactions processed.\n  unit: transaction\n  aggregation: sum\n  dimensions:\n  - program\n  - card_product\n- name: cards_active\n  description: Active cards (physical / virtual).\n  unit: card\n  aggregation: max\n  dimensions:\n  - program\n  - card_product\n- name: ach_transfers\n  description: ACH transfer count.\n  unit: transfer\n  aggregation: sum\n  dimensions:\n  - program\n- name: wire_transfers\n  description: Wire transfer count.\n  unit: transfer\n  aggregation: sum\n  dimensions:\n  - program\nprinciples:\n- name: Visibility\n  description: Pull Lithic invoices and transaction reporting via the API.\n- name: Allocation\n  description: Tag cards/accounts by business unit; one financial_account per cost\n   \
  \ center.\n- name: Optimization\n  description: Use ASA to lower fraud losses; archive unused cards to reduce per-card\n    fees.\n- name: Accountability\n  description: Program owners review monthly contract minimums vs activity.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lithic/refs/heads/main/finops/lithic-finops.yml
sources:
- https://lithic.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinTech
- BaaS
- Card Issuing
- Payments
- Embedded Finance
- FinOps
- FOCUS
---
