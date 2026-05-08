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
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps for UGI: regulated-utility holding company; no public API pricing or usage-meter surface. Spend mapping is contract-driven and reconciled per integration agreement.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: UGI Corporation
  ProviderName: UGI Corporation
  PublisherName: UGI Corporation
  ServiceCategory: Utility / Energy
  ServiceName: UGI Integration
layout: finops
meters:
- aggregation: sum
  description: Active partner integration contract period
  name: contract_term
  unit: month
name: Ugi Finops
provider_name: UGI Corporation
provider_slug: ugi
publisher_name: UGI Corporation
service_category: Utility / Energy
slug: ugi-finops
source_filename: ugi-finops.yml
source_heading: FinOps Profile
source_url: https://www.ugicorp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: UGI Corporation\nproviderId: ugi\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Utilities\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for UGI: regulated-utility holding company; no public API pricing\n  or usage-meter surface. Spend mapping is contract-driven and reconciled per integration agreement.'\nnotes: UGI has no public developer portal or pricing surface. Meters and FOCUS columns are placeholders\n  pending reconciliation against actual contract invoices.\nsources:\n  - https://www.ugicorp.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: UGI Corporation\n\
  serviceCategory: Utility / Energy\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: UGI Integration\n  ServiceCategory: Utility / Energy\n  ProviderName: UGI Corporation\n  PublisherName: UGI Corporation\n  InvoiceIssuerName: UGI Corporation\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    description: Active partner integration contract period\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile spend from contracted utility data-sharing agreements; UGI does not expose\n      a public usage telemetry surface.\n  - name: Allocation\n    description: Allocate per consuming line of business (gas distribution, AmeriGas propane, electric)\n      per the contract scope.\n  - name: Optimization\n    description: Re-scope the contract on renewal based on actual data exchange volume; consolidate\
  \ B2B\n      partner connections where possible.\n  - name: Accountability\n    description: Utility-IT and partner-management owners review contract performance and renewal terms.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ugi/refs/heads/main/finops/ugi-finops.yml
sources:
- https://www.ugicorp.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Energy
- Utilities
- FinOps
- FOCUS
---
