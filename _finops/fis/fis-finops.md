---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fis-payments-openapi.yml
  format: yaml
  label: FIS Payments API
  slug: fis-payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fis/refs/heads/main/openapi/fis-payments-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Usage
description: FOCUS-aligned FinOps mapping for FIS — enterprise B2B fintech billed via per-product licensing plus volume meters (per-account, per-transaction, per-asset under management) under master service agreements.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Fidelity National Information Services, Inc.
  ProviderName: Fidelity National Information Services, Inc.
  PublisherName: Fidelity National Information Services, Inc.
  ServiceCategory: Financial Services Software
  ServiceName: FIS
layout: finops
meters:
- aggregation: max
  description: Active customer accounts on FIS-hosted banking platforms (used as the primary core-banking volume meter)
  dimensions:
  - product
  - region
  - institution
  name: licensed_accounts
  unit: account-month
- aggregation: sum
  description: Payment, ACH, wire, card, and core-banking transactions processed
  dimensions:
  - product
  - rail
  - institution
  name: transactions_processed
  unit: transaction
- aggregation: avg
  description: Wealth management assets administered (used as the volume meter for wealth/trust products)
  dimensions:
  - product
  - institution
  name: assets_under_administration
  unit: USD
- aggregation: sum
  description: Recurring product, module, and platform license fees
  dimensions:
  - product
  - institution
  name: licensing_fees
  unit: month
- aggregation: sum
  description: One-time implementation, integration, and professional-services charges
  dimensions:
  - product
  - institution
  name: implementation_services
  unit: project
name: Fis Finops
provider_name: FIS Global
provider_slug: fis
publisher_name: Fidelity National Information Services, Inc.
service_category: Financial Services Software
slug: fis-finops
source_filename: fis-finops.yml
source_heading: FinOps Profile
source_url: https://www.fisglobal.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: FIS\nproviderId: fis\npublisherName: Fidelity National Information Services, Inc.\nserviceCategory: Financial Services Software\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Core Banking\n  - Financial Services\n  - Payments\n  - Wealth Management\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for FIS — enterprise B2B fintech billed via per-product licensing plus volume meters (per-account, per-transaction, per-asset under management) under master service agreements.\nnotes: FIS does not publish public price lists. Meters below model the expected line items on FI customer invoices but\
  \ exact billing structure varies per product (Modern Banking Platform, IBS, HORIZON, etc.) and per contract.\nsources:\n  - https://www.fisglobal.com/\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: FIS\n  ServiceCategory: Financial Services Software\n  ProviderName: Fidelity National Information Services, Inc.\n  PublisherName: Fidelity National Information Services, Inc.\n  InvoiceIssuerName: Fidelity National Information Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: licensed_accounts\n    description: Active customer accounts on FIS-hosted banking platforms (used as the primary core-banking volume meter)\n    unit: account-month\n    aggregation: max\n    dimensions:\n      - product\n      - region\n      - institution\n  - name: transactions_processed\n \
  \   description: Payment, ACH, wire, card, and core-banking transactions processed\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - product\n      - rail\n      - institution\n  - name: assets_under_administration\n    description: Wealth management assets administered (used as the volume meter for wealth/trust products)\n    unit: USD\n    aggregation: avg\n    dimensions:\n      - product\n      - institution\n  - name: licensing_fees\n    description: Recurring product, module, and platform license fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - institution\n  - name: implementation_services\n    description: One-time implementation, integration, and professional-services charges\n    unit: project\n    aggregation: sum\n    dimensions:\n      - product\n      - institution\nprinciples:\n  - name: Visibility\n    description: Reconcile FIS monthly invoices against internal account/transaction counts pulled from your data warehouse;\
  \ require contract pricing schedules to be tagged by product line for chargeback.\n  - name: Allocation\n    description: Use product, rail, and institution dimensions to allocate FIS spend to business lines (retail, commercial, wealth, payments).\n  - name: Optimization\n    description: Lever cost via account dormancy cleanup, channel routing (least-cost rails), batch consolidation, and renegotiating tiered minimums on contract renewal.\n  - name: Accountability\n    description: Vendor-management ownership of the FIS master service agreement should sit with COO/CIO office; finance reviews quarterly true-ups against minimum commitments.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fis/refs/heads/main/finops/fis-finops.yml
sources:
- https://www.fisglobal.com/
specification: FinOps Framework
tags:
- Banking
- Core Banking
- Financial Services
- Payments
- Wealth Management
- FinOps
- FOCUS
---
