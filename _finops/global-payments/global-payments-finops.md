---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: global-payments-unified-payments-api-openapi.yml
  format: yaml
  label: Global Payments Unified Payments API
  slug: payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/global-payments/refs/heads/main/openapi/global-payments-unified-payments-api-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Take Rate + Subscription
description: 'FOCUS-aligned FinOps framing for Global Payments: take-rate-based payment processing with monthly gateway/platform fees. Specific rates are merchant-specific and not publicly posted, so this artifact captures meter shape only.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Global Payments Inc.
  ProviderName: Global Payments
  PublisherName: Global Payments Inc.
  ServiceCategory: Payments
  ServiceName: Global Payments
layout: finops
meters:
- aggregation: sum
  description: Authorized card transactions processed
  dimensions:
  - card_brand
  - card_present
  - currency
  - country
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Total processed volume
  dimensions:
  - card_brand
  - currency
  name: transaction_volume
  unit: USD
- aggregation: sum
  description: Disputed / charged-back transactions
  name: chargebacks
  unit: transaction
- aggregation: sum
  description: Gateway / platform recurring fee
  name: monthly_platform_fee
  unit: month
- aggregation: max
  description: Active card-present POS terminals
  name: pos_devices
  unit: device-month
name: Global Payments Finops
provider_name: Global Payments
provider_slug: global-payments
publisher_name: Global Payments Inc.
service_category: Payments
slug: global-payments-finops
source_filename: global-payments-finops.yml
source_heading: FinOps Profile
source_url: https://www.globalpayments.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Global Payments\nproviderId: global-payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Payments\n  - Payment Processing\ndescription: 'FOCUS-aligned FinOps framing for Global Payments: take-rate-based payment processing with\n  monthly gateway/platform fees. Specific rates are merchant-specific and not publicly posted, so this\n  artifact captures meter shape only.'\nnotes: Reconcile after a public rate card or account-specific contract is referenced.\nsources:\n  - https://www.globalpayments.com/\n  - https://developer.globalpay.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Global Payments Inc.\nserviceCategory:\
  \ Payments\nbillingModel:\n  pricingCategory: Take Rate + Subscription\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Global Payments\n  ServiceCategory: Payments\n  ProviderName: Global Payments\n  PublisherName: Global Payments Inc.\n  InvoiceIssuerName: Global Payments Inc.\n  BillingCurrency: USD\nmeters:\n  - name: card_transactions\n    description: Authorized card transactions processed\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - card_present\n      - currency\n      - country\n  - name: transaction_volume\n    description: Total processed volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - currency\n  - name: chargebacks\n    description: Disputed / charged-back transactions\n    unit: transaction\n    aggregation: sum\n  - name:\
  \ monthly_platform_fee\n    description: Gateway / platform recurring fee\n    unit: month\n    aggregation: sum\n  - name: pos_devices\n    description: Active card-present POS terminals\n    unit: device-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Use Global Payments merchant statements and reporting APIs to surface daily settlement,\n      take-rate, and chargeback exposure.\n  - name: Allocation\n    description: Tag payments by storefront / channel / business unit via the gateway's metadata fields\n      to allocate processing cost.\n  - name: Optimization\n    description: Negotiate interchange-plus pricing at scale; route low-risk volume to cheaper rails;\n      monitor downgrade rates that erode effective take-rate.\n  - name: Accountability\n    description: Finance reconciles daily settlement files against ledger; merchant operations owns chargeback\n      response and rate renegotiation.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/global-payments/refs/heads/main/finops/global-payments-finops.yml
sources:
- https://www.globalpayments.com/
- https://developer.globalpay.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Payments
- Payment Processing
---
