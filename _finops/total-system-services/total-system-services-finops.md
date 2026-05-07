---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tsys-payment-gateway-openapi.yml
  format: yaml
  label: TSYS Payment Gateway
  slug: tsys-payment-gateway
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/total-system-services/refs/heads/main/openapi/tsys-payment-gateway-openapi.yml
- filename: tsys-issuing-openapi.yml
  format: yaml
  label: TSYS Issuing Platform
  slug: tsys-issuing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/total-system-services/refs/heads/main/openapi/tsys-issuing-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Contracted Per-Transaction + Platform Fee
description: TSYS (now part of Global Payments) bills processing partners on contracted per-transaction and platform-fee terms. There is no public meter rate card; this artifact describes the structural shape only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Global Payments Inc.
  ProviderName: Total System Services
  PublisherName: Global Payments Inc.
  ServiceCategory: Payments Processing
  ServiceName: Total System Services
layout: finops
meters:
- aggregation: sum
  description: Authorizations, captures, refunds, and reversals processed through TSYS Payment Gateway or Merchant Services.
  dimensions:
  - card_brand
  - card_present
  - region
  name: card_transactions_processed
  unit: transaction
- aggregation: avg
  description: Cardholder accounts maintained on the TSYS Issuing Platform.
  dimensions:
  - product
  - region
  name: accounts_on_file
  unit: account-month
- aggregation: sum
  description: Monthly platform / connectivity fee separate from per-transaction pricing.
  dimensions:
  - service
  name: platform_fee
  unit: month
name: Total System Services Finops
provider_name: Total System Services
provider_slug: total-system-services
publisher_name: Global Payments Inc.
service_category: Payments Processing
slug: total-system-services-finops
source_filename: total-system-services-finops.yml
source_heading: FinOps Profile
source_url: https://www.tsys.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Total System Services\nproviderId: total-system-services\npublisherName: Global Payments Inc.\nserviceCategory: Payments Processing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Payments\n  - Payment Processing\n  - Card Issuing\n  - Merchant Services\n  - FinOps\n  - FOCUS\ndescription: 'TSYS (now part of Global Payments) bills processing partners on contracted per-transaction\n  and platform-fee terms. There is no public meter rate card; this artifact describes the structural shape\n  only.'\nsources:\n  - https://www.tsys.com/\nnotes: Pricing not publicly retrievable; meters are descriptive and unpriced.\nbillingModel:\n\
  \  pricingCategory: Contracted Per-Transaction + Platform Fee\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Total System Services\n  ServiceCategory: Payments Processing\n  ProviderName: Total System Services\n  PublisherName: Global Payments Inc.\n  InvoiceIssuerName: Global Payments Inc.\n  BillingCurrency: USD\nmeters:\n  - name: card_transactions_processed\n    description: Authorizations, captures, refunds, and reversals processed through TSYS Payment Gateway\n      or Merchant Services.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - card_brand\n      - card_present\n      - region\n  - name: accounts_on_file\n    description: Cardholder accounts maintained on the TSYS Issuing Platform.\n    unit: account-month\n    aggregation: avg\n    dimensions:\n      - product\n      - region\n  - name: platform_fee\n    description: Monthly platform /\
  \ connectivity fee separate from per-transaction pricing.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: Reconcile the monthly TSYS settlement statement against your switch / authorization logs;\n      because rates are tiered by network and volume, line-item detail must be requested from your TSYS\n      relationship manager.\n  - name: Allocation\n    description: Attribute processing fees per card product / merchant-of-record entity. Keep BIN, MID,\n      and chain hierarchy in your COA so chargeback maps to the correct cost center.\n  - name: Optimization\n    description: Routinely review network routing (debit network choice), interchange-optimization data\n      submission quality (Level 2/3), and tier breakpoints to keep the blended take-rate near contract\n      floor.\n  - name: Accountability\n    description: Treasury / payments operations owns reconciliation against TSYS; product owners own\n  \
  \    issuing-platform fees per program.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/total-system-services/refs/heads/main/finops/total-system-services-finops.yml
sources:
- https://www.tsys.com/
specification: FinOps Framework
tags:
- Payments
- Payment Processing
- Card Issuing
- Merchant Services
- FinOps
- FOCUS
---
