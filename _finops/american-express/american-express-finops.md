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
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise / Bilateral
description: FinOps scaffold for American Express developer APIs. Amex bills via the merchant discount rate and interchange + acquirer fees rather than a stand-alone metered API. FOCUS columns describe the payment-processing shape; specific meters remain conceptual until Amex publishes per-API billing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: American Express Company
  ProviderName: American Express
  PublisherName: American Express Company
  ServiceCategory: Payments
  ServiceName: American Express Developer APIs
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until American Express publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: American Express Finops
provider_name: American Express
provider_slug: american-express
publisher_name: American Express Company
service_category: Payments
slug: american-express-finops
source_filename: american-express-finops.yml
source_heading: FinOps Profile
source_url: https://developer.americanexpress.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: American Express\nproviderId: american-express\npublisherName: American Express Company\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Credit Cards\n  - Financial Services\n  - Payments\n  - Tokenization\n  - Fraud Prevention\n  - Rewards\n  - Banking\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for American Express developer APIs. Amex bills via the merchant discount rate and interchange + acquirer fees rather than a stand-alone metered API. FOCUS columns describe the payment-processing shape; specific meters remain conceptual until Amex publishes per-API billing.\nnotes: >-\n  American Express developer APIs (Token Service / AETS, Enhanced Authorization, Account & Transaction) are partner-only. Access requires a merchant or issuing-partner agreement; pricing is embedded in the merchant discount\
  \ rate / interchange and acquirer fees rather than a stand-alone API price. Rate limits and SLAs are governed per-contract and not published publicly. Reconcile if Amex publishes a public price list or rate-limit page.\nsources:\n  - https://developer.americanexpress.com/\n  - https://developer.americanexpress.com/products/amex-token-service/overview\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: American Express Developer APIs\n  ServiceCategory: Payments\n  ProviderName: American Express\n  PublisherName: American Express Company\n  InvoiceIssuerName:\
  \ American Express Company\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until American Express publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the American Express service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level\
  \ caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the American Express relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/american-express/refs/heads/main/finops/american-express-finops.yml
sources:
- https://developer.americanexpress.com/
- https://developer.americanexpress.com/products/amex-token-service/overview
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Credit Cards
- Financial Services
- Payments
- Tokenization
- Fraud Prevention
- Rewards
- Banking
- FinOps
- FOCUS
---
