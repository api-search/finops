---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Service
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable (Regional Bank)
description: FOCUS-aligned FinOps placeholder for South State Corporation. South State is a regional U.S. bank holding company with no developer billing surface; this artifact captures the publisher entity only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: South State Bank, N.A.
  ProviderName: South State Corporation
  PublisherName: South State Corporation
  ServiceCategory: Regional Banking
  ServiceName: South State Bank Services
layout: finops
meters: []
name: South State Corporation Finops
provider_name: South State Corporation
provider_slug: south-state-corporation
publisher_name: South State Corporation
service_category: Regional Banking
slug: south-state-corporation-finops
source_filename: south-state-corporation-finops.yml
source_heading: FinOps Profile
source_url: https://www.southstatebank.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: South State Corporation\nproviderId: south-state-corporation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for South State Corporation. South State is a regional\n  U.S. bank holding company with no developer billing surface; this artifact captures the publisher entity\n  only.'\nsources:\n  - https://www.southstatebank.com/\nnotes: South State does not expose a public developer API or usage-based billing surface. Meters cannot\n  be reconciled because there are no published API consumption units. Account-level service charges are\n  product disclosures, not FinOps meters.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: South State Corporation\nserviceCategory: Regional Banking\nbillingModel:\n  pricingCategory: Not Applicable (Regional Bank)\n  billingFrequency: Per-Service\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: South State Bank Services\n  ServiceCategory: Regional Banking\n  ProviderName: South State Corporation\n  PublisherName: South State Corporation\n  InvoiceIssuerName: South State Bank, N.A.\n  BillingCurrency: USD\nmeters: []\nprinciples:\n  - name: Visibility\n    description: Customer-facing consumption (interest, fees, treasury services) is surfaced through online\n      banking statements and treasury reporting, not a developer billing API.\n  - name: Allocation\n    description: Not applicable on a developer surface; allocation is at the corporate-treasury account\n      level, governed by the bank's commercial banking agreement.\n  - name: Optimization\n    description:\
  \ Not applicable at the API/FinOps layer; account-level optimization (sweep accounts, fee\n      analysis) is the customer's treasury function.\n  - name: Accountability\n    description: Customer-level accountability is governed by the South State commercial banking agreement,\n      not by a developer/tenant contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/south-state-corporation/refs/heads/main/finops/south-state-corporation-finops.yml
sources:
- https://www.southstatebank.com/
specification: FinOps Framework
tags:
- Banking
- Financial Services
- FinOps
- FOCUS
---
