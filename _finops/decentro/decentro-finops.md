---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: decentro-kyc-api-openapi.yml
  format: yaml
  label: Decentro KYC & Onboarding API
  slug: kyc-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/decentro/refs/heads/main/openapi/decentro-kyc-api-openapi.yml
- filename: decentro-payments-api-openapi.yml
  format: yaml
  label: Decentro Payments API
  slug: payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/decentro/refs/heads/main/openapi/decentro-payments-api-openapi.yml
- filename: decentro-virtual-accounts-api-openapi.yml
  format: yaml
  label: Decentro Virtual Accounts API
  slug: virtual-accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/decentro/refs/heads/main/openapi/decentro-virtual-accounts-api-openapi.yml
- filename: decentro-ledger-api-openapi.yml
  format: yaml
  label: Decentro Ledger API
  slug: ledger-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/decentro/refs/heads/main/openapi/decentro-ledger-api-openapi.yml
billing_model:
  billingCurrency: INR
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Pay-As-You-Go + Pass-Through
description: 'FOCUS-aligned FinOps for Decentro: pay-per-API-call usage billing across six product categories, with bank-side and regulator-side surcharges (UPI/IMPS/NEFT/RTGS, Aadhaar, DigiLocker, credit bureaus) passed through. Rates are negotiated per merchant and not public.'
focus_columns:
  BillingCurrency: INR
  ChargeCategory: Usage
  InvoiceIssuerName: Decentro Tech Pvt Ltd
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Decentro
  PublisherName: Decentro Tech Pvt Ltd
  RegionId: IN
  ServiceCategory: Banking-as-a-Service
  ServiceName: Decentro
  ServiceSubcategory: India FinTech Infrastructure
layout: finops
meters:
- aggregation: count
  description: KYC, onboarding, Aadhaar, and DigiLocker verification calls.
  dimensions:
  - product
  - upstream_provider
  - merchant
  name: kyc_calls
  unit: request
- aggregation: count
  description: Money-movement transactions across UPI, IMPS, NEFT, and RTGS rails.
  dimensions:
  - rail
  - sponsor_bank
  - direction
  - merchant
  name: payment_transactions
  unit: transaction
- aggregation: count
  description: Virtual account create, fetch, balance, and reconciliation operations.
  dimensions:
  - operation
  - merchant
  name: virtual_account_operations
  unit: request
- aggregation: count
  description: Ledger journal, account, and transaction operations.
  dimensions:
  - operation
  - merchant
  name: ledger_operations
  unit: request
- aggregation: count
  description: Alternate-data and intelligence lookups.
  dimensions:
  - data_source
  - merchant
  name: bytes_calls
  unit: request
- aggregation: count
  description: Forensics and document-fraud verification calls.
  dimensions:
  - check_type
  - merchant
  name: scanner_calls
  unit: request
- aggregation: sum
  description: Sponsor-bank and regulator surcharges passed through to the merchant.
  dimensions:
  - rail
  - sponsor_bank
  name: bank_passthrough_charges
  unit: transaction
name: Decentro Finops
provider_name: Decentro
provider_slug: decentro
publisher_name: Decentro Tech Pvt Ltd
service_category: Banking-as-a-Service
slug: decentro-finops
source_filename: decentro-finops.yml
source_heading: FinOps Profile
source_url: https://decentro.tech
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Decentro\nproviderId: decentro\npublisherName: Decentro Tech Pvt Ltd\nserviceCategory: Banking-as-a-Service\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking-as-a-Service\n  - FinTech\n  - India\n  - Payments\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Decentro: pay-per-API-call usage billing across six product\n  categories, with bank-side and regulator-side surcharges (UPI/IMPS/NEFT/RTGS, Aadhaar,\n  DigiLocker, credit bureaus) passed through. Rates are negotiated per merchant and not public.'\nsources:\n  - https://decentro.tech\n  - https://in.decentro.tech\nnotes: No public per-call INR\
  \ rates. Meters reflect Decentro's product categories; dollar/INR\n  values must come from the customer's portal or master service agreement.\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Pass-Through\n  billingFrequency: Monthly\n  billingCurrency: INR\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Decentro\n  ServiceCategory: Banking-as-a-Service\n  ServiceSubcategory: India FinTech Infrastructure\n  ProviderName: Decentro\n  PublisherName: Decentro Tech Pvt Ltd\n  InvoiceIssuerName: Decentro Tech Pvt Ltd\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: INR\n  ChargeCategory: Usage\n  RegionId: IN\nmeters:\n  - name: kyc_calls\n    description: KYC, onboarding, Aadhaar, and DigiLocker verification calls.\n    unit: request\n    aggregation: count\n    dimensions:\n      - product\n      - upstream_provider\n      - merchant\n  - name: payment_transactions\n    description: Money-movement transactions\
  \ across UPI, IMPS, NEFT, and RTGS rails.\n    unit: transaction\n    aggregation: count\n    dimensions:\n      - rail\n      - sponsor_bank\n      - direction\n      - merchant\n  - name: virtual_account_operations\n    description: Virtual account create, fetch, balance, and reconciliation operations.\n    unit: request\n    aggregation: count\n    dimensions:\n      - operation\n      - merchant\n  - name: ledger_operations\n    description: Ledger journal, account, and transaction operations.\n    unit: request\n    aggregation: count\n    dimensions:\n      - operation\n      - merchant\n  - name: bytes_calls\n    description: Alternate-data and intelligence lookups.\n    unit: request\n    aggregation: count\n    dimensions:\n      - data_source\n      - merchant\n  - name: scanner_calls\n    description: Forensics and document-fraud verification calls.\n    unit: request\n    aggregation: count\n    dimensions:\n      - check_type\n      - merchant\n  - name: bank_passthrough_charges\n\
  \    description: Sponsor-bank and regulator surcharges passed through to the merchant.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - rail\n      - sponsor_bank\nprinciples:\n  - name: Visibility\n    description: Use the Decentro merchant portal usage and settlement reports to track call\n      volume by product category and rail. Reconcile pass-through bank charges line-by-line against\n      the monthly invoice and settlement file.\n  - name: Allocation\n    description: Issue separate Decentro client_id / secret pairs per consuming product so calls\n      can be attributed to a business line. Tag webhooks and ledger transactions with internal\n      account identifiers for downstream attribution.\n  - name: Optimization\n    description: Cache KYC results subject to RBI re-KYC rules to avoid repeat lookups, route\n      payouts through the cheapest acceptable rail (IMPS vs NEFT vs RTGS), and pre-fund virtual\n      accounts during festival/salary peaks rather\
  \ than retry-storming. Batch where the rail\n      allows.\n  - name: Accountability\n    description: Designate a single ops owner for the Decentro relationship who reviews monthly\n      settlement and bank surcharges, validates KPI guardrails (cost-per-onboarded-user,\n      cost-per-payout), and renegotiates rates when volume thresholds are hit.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/decentro/refs/heads/main/finops/decentro-finops.yml
sources:
- https://decentro.tech
- https://in.decentro.tech
specification: FinOps Framework
tags:
- Banking-as-a-Service
- FinTech
- India
- Payments
- FinOps
- FOCUS
---
