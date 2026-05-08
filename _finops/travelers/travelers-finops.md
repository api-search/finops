---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: travelers-openapi.yml
  format: yaml
  label: Travelers API
  slug: travelers
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/travelers/refs/heads/main/openapi/travelers-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Negotiated
description: FinOps shape for Travelers cannot be reconciled from public sources; the developer portal and pricing are gated and access is governed by partner agreements.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Travelers Indemnity Company
  ProviderName: Travelers
  PublisherName: The Travelers Indemnity Company
  ServiceCategory: Insurance
  ServiceName: Travelers API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: varies
name: Travelers Finops
provider_name: Travelers
provider_slug: travelers
publisher_name: The Travelers Indemnity Company
service_category: Insurance
slug: travelers-finops
source_filename: travelers-finops.yml
source_heading: FinOps Profile
source_url: https://developer.travelers.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Travelers\nproviderId: travelers\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Property Casualty\n  - Commercial Insurance\n  - Claims\n  - Fortune 500\n  - FinOps\n  - FOCUS\ndescription: FinOps shape for Travelers cannot be reconciled from public sources; the developer portal\n  and pricing are gated and access is governed by partner agreements.\nsources:\n  - https://developer.travelers.com\nnotes: Public pricing, billing, and usage telemetry surfaces are not disclosed. FOCUS mappings and\n  meters can only be confirmed against an executed Travelers partner / integration agreement.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ The Travelers Indemnity Company\nserviceCategory: Insurance\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Travelers API\n  ServiceCategory: Insurance\n  ProviderName: Travelers\n  PublisherName: The Travelers Indemnity Company\n  InvoiceIssuerName: The Travelers Indemnity Company\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Consumption data is exchanged via the Travelers partner channel rather than a public\n      usage API; visibility depends on the reporting clauses of the integration agreement.\n  - name: Allocation\n    description: Allocate costs to the line of business consuming Travelers integrations (claims,\n      quoting, policy servicing) using the contract identifier as the primary tag.\n  - name: Optimization\n\
  \    description: Optimization levers are negotiated (volume tiers, term length, multi-product bundling)\n      rather than surfaced through self-serve tooling.\n  - name: Accountability\n    description: Procurement and the integrating insurance line of business co-own the contract; renewals\n      and usage true-ups are governed by the partner agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/travelers/refs/heads/main/finops/travelers-finops.yml
sources:
- https://developer.travelers.com
specification: FinOps Framework
tags:
- Insurance
- Property Casualty
- Commercial Insurance
- Claims
- Fortune 500
- FinOps
- FOCUS
---
