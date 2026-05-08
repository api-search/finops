---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps view of Tink. Sales-led contracts. Cost is typically per consented end user (Account Aggregation), per Account Check, per Income Check, or per initiated Payment (PISP). Visa- affiliated discounts may apply.
focus_columns:
  BillingCurrency: EUR
  ChargeCategory: Usage
  InvoiceIssuerName: Tink AB
  ProviderName: Tink AB
  PublisherName: Tink AB
  ServiceCategory: Open Banking
  ServiceName: Tink Open Banking
layout: finops
meters:
- aggregation: count_distinct
  description: Per active consented end user (Account Aggregation).
  dimensions:
  - end_user
  name: consented_user
  unit: user_month
- aggregation: sum
  description: Per Account Check call.
  dimensions:
  - client
  name: account_check
  unit: call
- aggregation: sum
  description: Per initiated payment.
  dimensions:
  - client
  name: payment_initiation
  unit: payment
name: Tink Finops
provider_name: Tink
provider_slug: tink
publisher_name: Tink AB (Visa)
service_category: Open Banking
slug: tink-finops
source_filename: tink-finops.yml
source_heading: FinOps Profile
source_url: https://tink.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tink\nproviderId: tink\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Open Banking\n  - Fintech\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Tink. Sales-led contracts. Cost is typically per consented end user (Account\n  Aggregation), per Account Check, per Income Check, or per initiated Payment (PISP). Visa-\n  affiliated discounts may apply.\nsources:\n  - https://tink.com/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tink AB (Visa)\nserviceCategory: Open Banking\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: EUR\n\
  \  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Tink Open Banking\n  ServiceCategory: Open Banking\n  ProviderName: Tink AB\n  PublisherName: Tink AB\n  InvoiceIssuerName: Tink AB\n  BillingCurrency: EUR\n  ChargeCategory: Usage\nmeters:\n  - name: consented_user\n    description: Per active consented end user (Account Aggregation).\n    unit: user_month\n    aggregation: count_distinct\n    dimensions:\n      - end_user\n  - name: account_check\n    description: Per Account Check call.\n    unit: call\n    aggregation: sum\n    dimensions:\n      - client\n  - name: payment_initiation\n    description: Per initiated payment.\n    unit: payment\n    aggregation: sum\n    dimensions:\n      - client\nprinciples:\n  - name: Visibility\n    description: Track per-product per-event cost; reconcile vendor invoices monthly.\n  - name: Allocation\n    description: Allocate per consuming product line; tag end-user IDs to cost center.\n  -\
  \ name: Optimization\n    description: Reduce unnecessary refreshes; respect SCA cadence; cache categorized signals.\n  - name: Accountability\n    description: Assign a billing owner; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tink/refs/heads/main/finops/tink-finops.yml
sources:
- https://tink.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Open Banking
- Fintech
- FinOps
- FOCUS
---
