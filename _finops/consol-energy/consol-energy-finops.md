---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Not Applicable
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable
description: 'FOCUS-aligned FinOps for CONSOL Energy / Core Natural Resources: not an API/SaaS provider but a coal-mining producer; FinOps applies to commercial counterparty spend, not API consumption.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Core Natural Resources, Inc.
  ProviderName: CONSOL Energy
  PublisherName: Core Natural Resources, Inc.
  ServiceCategory: Energy / Coal Mining
  ServiceName: CONSOL Energy
layout: finops
meters:
- aggregation: sum
  description: Procurement / commercial invoices from CONSOL Energy / Core Natural Resources as counterparty
  dimensions:
  - business_unit
  - contract
  name: counterparty_invoice
  unit: invoice
name: Consol Energy Finops
provider_name: CONSOL Energy
provider_slug: consol-energy
publisher_name: Core Natural Resources, Inc.
service_category: Energy / Coal Mining
slug: consol-energy-finops
source_filename: consol-energy-finops.yml
source_heading: FinOps Profile
source_url: https://corenaturalresources.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CONSOL Energy\nproviderId: consol-energy\npublisherName: Core Natural Resources, Inc.\nserviceCategory: Energy / Coal Mining\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Coal Mining\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CONSOL Energy / Core Natural Resources: not an API/SaaS provider\n  but a coal-mining producer; FinOps applies to commercial counterparty spend, not API consumption.'\nnotes: CONSOL Energy / Core Natural Resources is not a software vendor; this artifact is included for\n  catalog completeness only.\nsources:\n  - https://corenaturalresources.com\nbillingModel:\n\
  \  pricingCategory: Not Applicable\n  billingFrequency: Not Applicable\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: CONSOL Energy\n  ServiceCategory: Energy / Coal Mining\n  ProviderName: CONSOL Energy\n  PublisherName: Core Natural Resources, Inc.\n  InvoiceIssuerName: Core Natural Resources, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: counterparty_invoice\n    description: Procurement / commercial invoices from CONSOL Energy / Core Natural Resources as counterparty\n    unit: invoice\n    aggregation: sum\n    dimensions:\n      - business_unit\n      - contract\nprinciples:\n  - name: Visibility\n    description: Counterparty invoices flow through procurement / treasury systems rather than a developer\n      console.\n  - name: Allocation\n    description: Allocate via standard procurement cost-center mapping; no API allocation applies.\n  - name: Optimization\n    description: No software-side optimization\
  \ is applicable.\n  - name: Accountability\n    description: Procurement / supply-chain teams own the counterparty relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/consol-energy/refs/heads/main/finops/consol-energy-finops.yml
sources:
- https://corenaturalresources.com
specification: FinOps Framework
tags:
- Coal Mining
- Energy
- FinOps
- FOCUS
---
