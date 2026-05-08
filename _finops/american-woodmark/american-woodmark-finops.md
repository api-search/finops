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
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise / Bilateral
description: FinOps scaffold for American Woodmark. The company invoices retail and homebuilder customers under standard building-products trade terms rather than a metered API. FOCUS mappings remain conceptual.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: American Woodmark Corporation
  ProviderName: American Woodmark
  PublisherName: American Woodmark Corporation
  ServiceCategory: Building Products
  ServiceName: American Woodmark API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until American Woodmark publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: American Woodmark Finops
provider_name: American Woodmark
provider_slug: american-woodmark
publisher_name: American Woodmark Corporation
service_category: Building Products
slug: american-woodmark-finops
source_filename: american-woodmark-finops.yml
source_heading: FinOps Profile
source_url: https://www.americanwoodmark.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: American Woodmark\nproviderId: american-woodmark\npublisherName: American Woodmark Corporation\nserviceCategory: Building Products\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Cabinetry\n  - Home Products\n  - Construction\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for American Woodmark. The company invoices retail and homebuilder customers under standard building-products trade terms rather than a metered API. FOCUS mappings remain conceptual.\nnotes: >-\n  American Woodmark is a kitchen and bath cabinet manufacturer; it does not publish a public API developer portal with documented pricing or rate limits. Trading-partner integrations with home centers and homebuilders are governed by EDI and bilateral agreements. Reconcile if a public API is launched.\nsources:\n  - https://www.americanwoodmark.com\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: American Woodmark API\n  ServiceCategory: Building Products\n  ProviderName: American Woodmark\n  PublisherName: American Woodmark Corporation\n  InvoiceIssuerName: American Woodmark Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until American Woodmark publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name:\
  \ Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the American Woodmark service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the American Woodmark relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/american-woodmark/refs/heads/main/finops/american-woodmark-finops.yml
sources:
- https://www.americanwoodmark.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Cabinetry
- Home Products
- Construction
- FinOps
- FOCUS
---
