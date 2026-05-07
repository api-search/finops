---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: visa-acceptance-payments-openapi.yml
  format: yaml
  label: Visa Acceptance Payments API
  slug: visa-acceptance-payments
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/visa-acceptance/refs/heads/main/openapi/visa-acceptance-payments-openapi.yml
- filename: visa-acceptance-payments-openapi.yml
  format: yaml
  label: Visa Acceptance Invoicing API
  slug: visa-acceptance-invoicing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/visa-acceptance/refs/heads/main/openapi/visa-acceptance-payments-openapi.yml
- filename: visa-acceptance-payments-openapi.yml
  format: yaml
  label: Visa Acceptance Pay by Link API
  slug: visa-acceptance-pay-by-link
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/visa-acceptance/refs/heads/main/openapi/visa-acceptance-payments-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Refund
  - Adjustment
  pricingCategory: Take Rate + Subscription
description: FOCUS-aligned FinOps shape for Visa Acceptance / Cybersource. Pricing is contractual per-merchant; meters reflect the canonical line items on a card-acceptance invoice rather than publicly priced units.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CyberSource Corporation
  ProviderName: Visa Acceptance Solutions
  PublisherName: CyberSource Corporation
  ServiceCategory: Payments
  ServiceName: Visa Acceptance / Cybersource
layout: finops
meters:
- aggregation: sum
  dimensions:
  - card_brand
  - region
  - mcc
  name: card_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - card_brand
  - region
  name: transaction_volume
  unit: USD
- aggregation: sum
  name: tokenization_requests
  unit: request
- aggregation: sum
  dimensions:
  - decision_outcome
  name: fraud_screen_requests
  unit: request
- aggregation: sum
  name: refunds
  unit: transaction
name: Visa Acceptance Finops
provider_name: Visa Acceptance
provider_slug: visa-acceptance
publisher_name: CyberSource Corporation (a Visa company)
service_category: Payments
slug: visa-acceptance-finops
source_filename: visa-acceptance-finops.yml
source_heading: FinOps Profile
source_url: https://developer.cybersource.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Visa Acceptance\nproviderId: visa-acceptance\npublisherName: CyberSource Corporation (a Visa company)\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\n  - Card Acceptance\n  - Cybersource\ndescription: FOCUS-aligned FinOps shape for Visa Acceptance / Cybersource. Pricing is contractual\n  per-merchant; meters reflect the canonical line items on a card-acceptance invoice rather than\n  publicly priced units.\nsources:\n  - https://developer.cybersource.com/\nnotes: No public unit prices were available; per-transaction take rate, interchange, and\n  value-added-service fees are negotiated under the merchant\
  \ processing agreement.\nbillingModel:\n  pricingCategory: Take Rate + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Visa Acceptance / Cybersource\n  ServiceCategory: Payments\n  ProviderName: Visa Acceptance Solutions\n  PublisherName: CyberSource Corporation\n  InvoiceIssuerName: CyberSource Corporation\n  BillingCurrency: USD\nmeters:\n  - name: card_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - region\n      - mcc\n  - name: transaction_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - region\n  - name: tokenization_requests\n    unit: request\n    aggregation: sum\n  - name: fraud_screen_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - decision_outcome\n  - name: refunds\n    unit: transaction\n \
  \   aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Business Center reports and Reporting / On-Demand Reporting REST APIs to\n      pull settlement, fee, and transaction-level detail; reconcile against the monthly merchant\n      statement.\n  - name: Allocation\n    description: Tag transactions with merchant_defined_data fields (MID, sub-merchant, brand) so\n      cost can be allocated across business units sharing a Visa Acceptance contract.\n  - name: Optimization\n    description: Levers include processor / acquirer routing, network tokenization to lift auth\n      rates, decision-manager rule tuning to reduce false declines, and renegotiating tier breaks\n      against settled volume.\n  - name: Accountability\n    description: Payments / treasury owns the merchant agreement; engineering owns API integration\n      and decision-manager rules; finance reconciles the monthly statement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/visa-acceptance/refs/heads/main/finops/visa-acceptance-finops.yml
sources:
- https://developer.cybersource.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
- Card Acceptance
- Cybersource
---
