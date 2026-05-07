---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: progressive-auto-quote-api-openapi.yml
  format: yaml
  label: Progressive Auto Quote API
  slug: auto-quote-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/progressive/refs/heads/main/openapi/progressive-auto-quote-api-openapi.yml
- filename: progressive-certificate-of-insurance-api-openapi.yml
  format: yaml
  label: Progressive Certificate of Insurance API
  slug: certificate-of-insurance-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/progressive/refs/heads/main/openapi/progressive-certificate-of-insurance-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: FOCUS-aligned FinOps shape for Progressive. There is no public API or usage-billing surface; cost flow is contract-driven.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Progressive Casualty Insurance Company
  ProviderName: Progressive
  PublisherName: Progressive Casualty Insurance Company
  ServiceCategory: Insurance
  ServiceName: Progressive
layout: finops
meters:
- aggregation: sum
  name: contract_fees
  unit: varies
name: Progressive Finops
provider_name: Progressive
provider_slug: progressive
publisher_name: Progressive Casualty Insurance Company
service_category: Insurance
slug: progressive-finops
source_filename: progressive-finops.yml
source_heading: FinOps Profile
source_url: https://www.progressive.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Progressive\nproviderId: progressive\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Financial Services\n  - Auto Insurance\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Progressive. There is no public API or usage-billing surface;\n  cost flow is contract-driven.\nnotes: No public billing or usage telemetry. Placeholder for contract-driven cost.\nsources:\n  - https://www.progressive.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Progressive Casualty Insurance Company\nserviceCategory: Insurance\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\nfocusColumns:\n  ServiceName: Progressive\n  ServiceCategory: Insurance\n  ProviderName: Progressive\n  PublisherName: Progressive Casualty Insurance Company\n  InvoiceIssuerName: Progressive Casualty Insurance Company\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Cost visibility flows from contract invoices and partner reporting; no API usage telemetry\n      is published.\n  - name: Allocation\n    description: Allocate by partner / aggregator agreement and integration scope.\n  - name: Optimization\n    description: Optimization happens at contract renewal; no consumption-side levers are exposed.\n  - name: Accountability\n    description: Spend is owned by the procurement / partnership relationship, not by an API consumption\n      budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/progressive/refs/heads/main/finops/progressive-finops.yml
sources:
- https://www.progressive.com/
specification: FinOps Framework
tags:
- Insurance
- Financial Services
- Auto Insurance
- FinOps
- FOCUS
---
