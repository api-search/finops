---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: prudential-financial-developer-api-openapi.yml
  format: yaml
  label: Prudential Financial Developer API
  slug: prudential-financial-developer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prudential-financial/refs/heads/main/openapi/prudential-financial-developer-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: FOCUS-aligned FinOps shape for Prudential Financial. No public API or usage-billing surface exists; cost flow is contract-driven.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Prudential Insurance Company of America
  ProviderName: Prudential Financial
  PublisherName: The Prudential Insurance Company of America
  ServiceCategory: Insurance
  ServiceName: Prudential Financial
layout: finops
meters:
- aggregation: sum
  name: contract_fees
  unit: varies
name: Prudential Financial Finops
provider_name: Prudential Financial
provider_slug: prudential-financial
publisher_name: The Prudential Insurance Company of America
service_category: Insurance
slug: prudential-financial-finops
source_filename: prudential-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.prudential.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Prudential Financial\nproviderId: prudential-financial\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Financial Services\n  - Retirement\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Prudential Financial. No public API or usage-billing surface\n  exists; cost flow is contract-driven.\nnotes: No public billing or usage telemetry. Placeholder for contract-driven cost.\nsources:\n  - https://www.prudential.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Prudential Insurance Company of America\nserviceCategory: Insurance\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Prudential Financial\n  ServiceCategory: Insurance\n  ProviderName: Prudential Financial\n  PublisherName: The Prudential Insurance Company of America\n  InvoiceIssuerName: The Prudential Insurance Company of America\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Cost visibility flows from contract invoices and partner reporting; no API usage telemetry\n      is published.\n  - name: Allocation\n    description: Allocate by partner / aggregator / plan-sponsor agreement.\n  - name: Optimization\n    description: Optimization happens at contract renewal; no consumption-side levers are exposed.\n  - name: Accountability\n    description: Spend is owned by the procurement / partnership relationship, not by an API consumption\n      budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/prudential-financial/refs/heads/main/finops/prudential-financial-finops.yml
sources:
- https://www.prudential.com/
specification: FinOps Framework
tags:
- Insurance
- Financial Services
- Retirement
- FinOps
- FOCUS
---
