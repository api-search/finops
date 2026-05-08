---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: marqeta-core-api-openapi.yml
  format: yaml
  label: Marqeta Core API
  slug: core-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/openapi/marqeta-core-api-openapi.yml
- filename: marqeta-diva-api-openapi.yml
  format: yaml
  label: Marqeta Diva API
  slug: diva-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/openapi/marqeta-diva-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Negotiated
description: 'Marqeta bills under bespoke contracts: platform minimums, per-transaction fees, card production, interchange share, premium service fees.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Marqeta
  ProviderName: Marqeta
  PublisherName: Marqeta
  ServiceCategory: Card Issuing
  ServiceName: Marqeta
layout: finops
meters:
- aggregation: sum
  description: Card transactions processed.
  dimensions:
  - program
  - card_product
  name: transactions
  unit: transaction
- aggregation: sum
  description: Cards produced (physical / virtual).
  dimensions:
  - program
  - card_product
  name: cards_issued
  unit: card
- aggregation: sum
  description: Interchange revenue share.
  dimensions:
  - program
  name: interchange
  unit: USD
name: Marqeta Finops
provider_name: Marqeta
provider_slug: marqeta
publisher_name: Marqeta, Inc.
service_category: FinTech
slug: marqeta-finops
source_filename: marqeta-finops.yml
source_heading: FinOps Profile
source_url: https://www.marqeta.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Marqeta\nproviderId: marqeta\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- FinTech\n- BaaS\n- Card Issuing\n- Payments\n- Embedded Finance\n- FinOps\n- FOCUS\ndescription: 'Marqeta bills under bespoke contracts: platform minimums, per-transaction\n  fees, card production, interchange share, premium service fees.'\nnotes: Invoiced via Marqeta. Use program-level reporting endpoints to attribute costs.\nsources:\n- https://www.marqeta.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Marqeta, Inc.\nserviceCategory: FinTech\nbillingModel:\n  pricingCategory: Negotiated\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Marqeta\n  ServiceCategory: Card Issuing\n  ProviderName: Marqeta\n  PublisherName: Marqeta\n  InvoiceIssuerName: Marqeta\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: transactions\n  description: Card transactions processed.\n  unit: transaction\n  aggregation: sum\n  dimensions:\n  - program\n  - card_product\n- name: cards_issued\n  description: Cards produced (physical / virtual).\n  unit: card\n  aggregation: sum\n  dimensions:\n  - program\n  - card_product\n- name: interchange\n  description: Interchange revenue share.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - program\nprinciples:\n- name: Visibility\n  description: Pull program-level reports from Marqeta's reporting endpoints and invoices.\n- name: Allocation\n  description: Tag transactions by card_product and business unit.\n- name: Optimization\n  description: Right-size card products;\
  \ align RTD timeouts to lower decline costs.\n- name: Accountability\n  description: Program owners review monthly fees against contract minimums.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/marqeta/refs/heads/main/finops/marqeta-finops.yml
sources:
- https://www.marqeta.com/
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
