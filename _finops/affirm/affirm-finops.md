---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: affirm-direct-api-openapi.yml
  format: yaml
  label: Affirm Direct API
  slug: direct-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/affirm/refs/heads/main/openapi/affirm-direct-api-openapi.yml
- filename: affirm-checkout-openapi.yml
  format: yaml
  label: Affirm Checkout API
  slug: checkout-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/affirm/refs/heads/main/openapi/affirm-checkout-openapi.yml
- filename: affirm-transactions-openapi.yml
  format: yaml
  label: Affirm Transactions API
  slug: transactions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/affirm/refs/heads/main/openapi/affirm-transactions-openapi.yml
- filename: affirm-promos-openapi.yml
  format: yaml
  label: Affirm Promos API
  slug: promos-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/affirm/refs/heads/main/openapi/affirm-promos-openapi.yml
- filename: affirm-disputes-openapi.yml
  format: yaml
  label: Affirm Disputes API
  slug: disputes-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/affirm/refs/heads/main/openapi/affirm-disputes-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Refund
  - Adjustment
  pricingCategory: Take Rate
description: 'FOCUS-aligned FinOps for Affirm: take-rate-based merchant billing for Buy-Now-Pay-Later consumer financing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Affirm, Inc.
  ProviderName: Affirm
  PublisherName: Affirm, Inc.
  ServiceCategory: Payments / BNPL
  ServiceName: Affirm
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - term
  - merchant
  name: completed_loans
  unit: loan
- aggregation: sum
  dimensions:
  - merchant
  - product
  name: gmv
  unit: USD
- aggregation: sum
  dimensions:
  - merchant
  name: merchant_discount
  unit: USD
- aggregation: sum
  dimensions:
  - merchant
  name: per_transaction_fee
  unit: USD
- aggregation: sum
  dimensions:
  - merchant
  name: refunds
  unit: USD
name: Affirm Finops
provider_name: affirm
provider_slug: affirm
publisher_name: Affirm, Inc.
service_category: Payments / BNPL
slug: affirm-finops
source_filename: affirm-finops.yml
source_heading: FinOps Profile
source_url: https://www.affirm.com/business
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: affirm\nproviderId: affirm\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Affirm bills merchants via a take-rate (MDR + fixed fee) model. Specific rates are not\n  published and are negotiated per merchant.\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\n  - BNPL\ndescription: 'FOCUS-aligned FinOps for Affirm: take-rate-based merchant billing for Buy-Now-Pay-Later\n  consumer financing.'\nsources:\n  - https://www.affirm.com/business\n  - https://docs.affirm.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Affirm, Inc.\nserviceCategory: Payments / BNPL\nbillingModel:\n  pricingCategory: Take Rate\n  billingFrequency: Continuous Settlement\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Usage\n    - Refund\n    - Adjustment\nfocusColumns:\n  ServiceName: Affirm\n  ServiceCategory: Payments / BNPL\n  ProviderName: Affirm\n  PublisherName: Affirm, Inc.\n  InvoiceIssuerName: Affirm, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: completed_loans\n    unit: loan\n    aggregation: sum\n    dimensions:\n      - product\n      - term\n      - merchant\n  - name: gmv\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - merchant\n      - product\n  - name: merchant_discount\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - merchant\n  - name: per_transaction_fee\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - merchant\n  - name: refunds\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - merchant\nprinciples:\n  - name: Visibility\n    description: Use Affirm Merchant Dashboard / settlement reports to track GMV, MDR, fees, and\n      refunds at order grain.\n  - name: Allocation\n    description:\
  \ Tag Affirm checkout sessions with the consuming product/team for chargeback in\n      multi-brand merchants.\n  - name: Optimization\n    description: Negotiate MDR breakpoints by GMV; route shorter-term Pay-in-4 vs longer-term\n      installment based on AOV; monitor lift vs cost.\n  - name: Accountability\n    description: Assign payments-finance owner; reconcile monthly Affirm settlements against\n      ledger; investigate take-rate variance.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/affirm/refs/heads/main/finops/affirm-finops.yml
sources:
- https://www.affirm.com/business
- https://docs.affirm.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
- BNPL
---
