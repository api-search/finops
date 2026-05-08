---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tyson-foods-edi-integration-api-openapi.yml
  format: yaml
  label: Tyson Foods EDI Integration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tyson-foods/refs/heads/main/openapi/tyson-foods-edi-integration-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom Contract
description: 'FOCUS-aligned FinOps for Tyson Foods: B2B-only integration spend, billed under custom partner contracts; no public usage-based meters published.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Tyson Foods, Inc.
  ProviderName: Tyson Foods
  PublisherName: Tyson Foods, Inc.
  ServiceCategory: B2B Integration
  ServiceName: Tyson Foods Integration
layout: finops
meters:
- aggregation: sum
  description: Active partner integration contract period
  name: contract_term
  unit: month
name: Tyson Foods Finops
provider_name: Tyson Foods
provider_slug: tyson-foods
publisher_name: Tyson Foods, Inc.
service_category: B2B Integration
slug: tyson-foods-finops
source_filename: tyson-foods-finops.yml
source_heading: FinOps Profile
source_url: https://www.tysonfoods.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tyson Foods\nproviderId: tyson-foods\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - B2B Integration\n  - EDI\n  - Food\n  - Supply Chain\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Tyson Foods: B2B-only integration spend, billed under custom partner\n  contracts; no public usage-based meters published.'\nnotes: Tyson Foods has no public API pricing or developer portal. FinOps mapping is best-effort and reflects\n  contract-driven B2B integration; meters and FOCUS columns will need to be reconciled against actual\n  invoices.\nsources:\n  - https://www.tysonfoods.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Tyson Foods, Inc.\nserviceCategory: B2B Integration\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Tyson Foods Integration\n  ServiceCategory: B2B Integration\n  ProviderName: Tyson Foods\n  PublisherName: Tyson Foods, Inc.\n  InvoiceIssuerName: Tyson Foods, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_term\n    description: Active partner integration contract period\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile spend from the partner integration contract and any EDI VAN charges; Tyson\n      does not expose a public usage telemetry surface.\n  - name: Allocation\n    description: Allocate to the consuming line of business (retail, food-service, logistics) per the\n      contract's scope of work.\n  - name: Optimization\n    description: Re-scope contract on\
  \ renewal based on volume of orders, ASNs, and invoices exchanged;\n      consolidate trading-partner connections where possible.\n  - name: Accountability\n    description: Supply-chain and IT integration owners review contract performance and renewal terms\n      against actual order volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tyson-foods/refs/heads/main/finops/tyson-foods-finops.yml
sources:
- https://www.tysonfoods.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- B2B Integration
- EDI
- Food
- Supply Chain
- FinOps
- FOCUS
---
