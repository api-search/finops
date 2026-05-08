---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: procter-and-gamble-api-marketplace-openapi.yml
  format: yaml
  label: Procter & Gamble API Marketplace
  slug: api-marketplace
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/procter-and-gamble/refs/heads/main/openapi/procter-and-gamble-api-marketplace-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: FOCUS-aligned FinOps shape for Procter & Gamble. There is no public API or usage-billing surface; cost flow is contract-driven.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Procter & Gamble Company
  ProviderName: Procter & Gamble
  PublisherName: The Procter & Gamble Company
  ServiceCategory: Consumer Goods
  ServiceName: Procter & Gamble
layout: finops
meters:
- aggregation: sum
  name: contract_fees
  unit: varies
name: Procter And Gamble Finops
provider_name: Procter & Gamble
provider_slug: procter-and-gamble
publisher_name: The Procter & Gamble Company
service_category: Consumer Goods
slug: procter-and-gamble-finops
source_filename: procter-and-gamble-finops.yml
source_heading: FinOps Profile
source_url: https://us.pg.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Procter & Gamble\nproviderId: procter-and-gamble\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Consumer Goods\n  - Retail\n  - Supply Chain\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Procter & Gamble. There is no public API or usage-billing\n  surface; cost flow is contract-driven.\nnotes: No public billing or usage telemetry. Placeholder for contract-driven cost.\nsources:\n  - https://us.pg.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Procter & Gamble Company\nserviceCategory: Consumer Goods\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\nfocusColumns:\n  ServiceName: Procter & Gamble\n  ServiceCategory: Consumer Goods\n  ProviderName: Procter & Gamble\n  PublisherName: The Procter & Gamble Company\n  InvoiceIssuerName: The Procter & Gamble Company\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Cost visibility flows from contract invoices and partner reporting; no API usage telemetry\n      is published.\n  - name: Allocation\n    description: Allocate by partner agreement and integration scope.\n  - name: Optimization\n    description: Optimization happens at contract renewal — scope, volume, and term — not via consumption\n      levers.\n  - name: Accountability\n    description: Spend is owned by the procurement / partnership relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/procter-and-gamble/refs/heads/main/finops/procter-and-gamble-finops.yml
sources:
- https://us.pg.com/
specification: FinOps Framework
tags:
- Consumer Goods
- Retail
- Supply Chain
- FinOps
- FOCUS
---
