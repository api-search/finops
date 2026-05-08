---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Contract
  chargeCategories:
  - Purchase
  pricingCategory: Partner Contract
description: Structural FinOps placeholder for Papa John's International. No public per-API pricing; partner integrations are contracted.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Papa John's International, Inc.
  ProviderName: Papa John's International
  PublisherName: Papa John's International, Inc.
  ServiceCategory: Food Service / QSR
  ServiceName: Papa John's International API
layout: finops
meters:
- aggregation: count
  description: Partner-contract integration fee, structure varies
  dimensions:
  - partner
  name: partner_integration_fee
  unit: contract-year
name: Papa Johns International Finops
provider_name: Papa John's International
provider_slug: papa-johns-international
publisher_name: Papa John's International, Inc.
service_category: Food Service / QSR
slug: papa-johns-international-finops
source_filename: papa-johns-international-finops.yml
source_heading: FinOps Profile
source_url: https://www.papajohns.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Papa John's International\nproviderId: papa-johns-international\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public pricing or usage API. Structural FinOps placeholder only — integrations\n  are partner-only.\ntags:\n  - FinOps\n  - FOCUS\n  - QSR\n  - Food Service\ndescription: Structural FinOps placeholder for Papa John's International. No public per-API\n  pricing; partner integrations are contracted.\nsources:\n  - https://www.papajohns.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Papa John's International, Inc.\nserviceCategory: Food Service / QSR\nbillingModel:\n  pricingCategory:\
  \ Partner Contract\n  billingFrequency: Per Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Papa John's International API\n  ServiceCategory: Food Service / QSR\n  ProviderName: Papa John's International\n  PublisherName: Papa John's International, Inc.\n  InvoiceIssuerName: Papa John's International, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: partner_integration_fee\n    description: Partner-contract integration fee, structure varies\n    unit: contract-year\n    aggregation: count\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Visibility comes from partner reporting; no Papa John's-published usage API.\n  - name: Allocation\n    description: Allocate by integration partner contract.\n  - name: Optimization\n    description: Renewal-time renegotiation based on transaction volume realized.\n  - name: Accountability\n    description: Partner relationship owner accountable\
  \ for integration cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/papa-johns-international/refs/heads/main/finops/papa-johns-international-finops.yml
sources:
- https://www.papajohns.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- QSR
- Food Service
---
