---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract / Custom
description: Vertex Pharmaceuticals is a biotechnology company without a public developer API or metered billing surface. This artifact retains the FinOps shape only to mark the catalog entry as a Contact Sales / partnership engagement.
focus_columns:
  BillingCurrency: USD
  ProviderName: Vertex Pharmaceuticals
  PublisherName: Vertex Pharmaceuticals Incorporated
  ServiceCategory: Pharmaceuticals
  ServiceName: Vertex Pharmaceuticals
layout: finops
meters:
- aggregation: sum
  name: contract_engagement
  unit: varies
name: Vertex Pharmaceuticals Finops
provider_name: Vertex Pharmaceuticals
provider_slug: vertex-pharmaceuticals
publisher_name: Vertex Pharmaceuticals Incorporated
service_category: Pharmaceuticals
slug: vertex-pharmaceuticals-finops
source_filename: vertex-pharmaceuticals-finops.yml
source_heading: FinOps Profile
source_url: https://www.vrtx.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Vertex Pharmaceuticals\nproviderId: vertex-pharmaceuticals\npublisherName: Vertex Pharmaceuticals Incorporated\nserviceCategory: Pharmaceuticals\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Pharmaceuticals\n  - Life Sciences\ndescription: Vertex Pharmaceuticals is a biotechnology company without a public developer API or\n  metered billing surface. This artifact retains the FinOps shape only to mark the catalog entry as\n  a Contact Sales / partnership engagement.\nsources:\n  - https://www.vrtx.com/\nnotes: No public unit pricing, FOCUS columns, or meters are reconcilable. Treat as partnership-\n  governed.\nbillingModel:\n  pricingCategory:\
  \ Contract / Custom\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Vertex Pharmaceuticals\n  ServiceCategory: Pharmaceuticals\n  ProviderName: Vertex Pharmaceuticals\n  PublisherName: Vertex Pharmaceuticals Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: contract_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No usage telemetry is published; visibility is provided through partnership reporting\n      cadences agreed in the data-sharing contract.\n  - name: Allocation\n    description: Costs are allocated through the partnership P&L; there is no per-tenant or per-API\n      breakdown to attribute.\n  - name: Optimization\n    description: Optimization is contractual - scope, term length, and milestone-based commercial\n      structures negotiated in the partnership agreement.\n  - name: Accountability\n    description: The Vertex business-development\
  \ counterparty owns commercial terms; the consuming\n      organization's partnership lead owns spend on its side.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vertex-pharmaceuticals/refs/heads/main/finops/vertex-pharmaceuticals-finops.yml
sources:
- https://www.vrtx.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Pharmaceuticals
- Life Sciences
---
