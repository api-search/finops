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
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Bundled Banking Fees
description: 'FOCUS-aligned FinOps shape for the Truist (formerly BB&T) developer-portal APIs: partner / open-banking program access with banking fees flowing through the underlying customer account relationship, not metered per API call.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Truist Bank
  PricingCategory: Bundled Banking Fees
  PricingUnit: account
  ProviderName: Truist
  PublisherName: Truist Financial Corporation
  ServiceCategory: Banking / Open Banking APIs
  ServiceName: Truist Developer APIs
layout: finops
meters:
- aggregation: max
  description: Accounts linked under partner-application OAuth consent
  dimensions:
  - account_type
  - partner
  name: linked_accounts
  unit: account
- aggregation: sum
  description: API request volume — operational meter, not necessarily per-call billed
  dimensions:
  - api
  - partner
  name: api_calls
  unit: request
- aggregation: sum
  description: Settled transaction value visible through the API
  dimensions:
  - account_type
  - transaction_type
  name: transaction_volume
  unit: USD
name: Bbandt Corp Finops
provider_name: BB&T Corp (Truist)
provider_slug: bbandt-corp
publisher_name: Truist Financial Corporation
service_category: Banking / Open Banking APIs
slug: bbandt-corp-finops
source_filename: bbandt-corp-finops.yml
source_heading: FinOps Profile
source_url: https://developer.truist.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: BB&T Corp (Truist)\nproviderId: bbandt-corp\npublisherName: Truist Financial Corporation\nserviceCategory: Banking / Open Banking APIs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Open Banking\n  - Truist\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for the Truist (formerly BB&T) developer-portal APIs: partner\n  / open-banking program access with banking fees flowing through the underlying customer account relationship,\n  not metered per API call.'\nnotes: No public rate card. Replace meter values with the partner-program agreement once available.\nsources:\n  - https://developer.truist.com/\nprinciples:\n  - name: Visibility\n\
  \    description: Use the accounts and transactions APIs to surface deposits, payments, and fees back to\n      the consuming application or fintech for end-customer attribution.\n  - name: Allocation\n    description: Allocate banking fees to the originating account holder; allocate API consumption back\n      to the partner application via OAuth client identity.\n  - name: Optimization\n    description: Cache reference data (account metadata, last-known-good balance) to minimize redundant\n      polling; prefer event/webhook integration where Truist offers it.\n  - name: Accountability\n    description: Designate a partner-program owner who manages the Truist developer agreement, monitors\n      consent expirations, and reviews fee pass-through monthly.\nbillingModel:\n  pricingCategory: Bundled Banking Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n\
  \  ServiceName: Truist Developer APIs\n  ServiceCategory: Banking / Open Banking APIs\n  ProviderName: Truist\n  PublisherName: Truist Financial Corporation\n  InvoiceIssuerName: Truist Bank\n  PricingCategory: Bundled Banking Fees\n  PricingUnit: account\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: linked_accounts\n    description: Accounts linked under partner-application OAuth consent\n    unit: account\n    aggregation: max\n    dimensions:\n      - account_type\n      - partner\n  - name: api_calls\n    description: API request volume — operational meter, not necessarily per-call billed\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\n  - name: transaction_volume\n    description: Settled transaction value visible through the API\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account_type\n      - transaction_type\napis:\n  - name: Truist Personal and Small Business Accounts API\n    baseURL: ''\n    serviceName:\
  \ Truist Personal and Small Business Accounts API\n    serviceCategory: API\n  - name: Truist Personal and Small Business Transactions API\n    baseURL: ''\n    serviceName: Truist Personal and Small Business Transactions API\n    serviceCategory: API\n  - name: Truist Commercial Accounts API\n    baseURL: ''\n    serviceName: Truist Commercial Accounts API\n    serviceCategory: API\n  - name: Truist Commercial Account Transactions API\n    baseURL: ''\n    serviceName: Truist Commercial Account Transactions API\n    serviceCategory: API\n  - name: Truist Association Services API\n    baseURL: ''\n    serviceName: Truist Association Services API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Linked Account\n    metric: total_partner_fees / linked_accounts\n    target: align to per-account customer LTV\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bbandt-corp/refs/heads/main/finops/bbandt-corp-finops.yml
sources:
- https://developer.truist.com/
specification: FinOps Framework
tags:
- Banking
- Open Banking
- Truist
- FinOps
- FOCUS
---
