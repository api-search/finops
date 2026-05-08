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
description: FinOps scaffold for Ameresco. The company invoices customers under energy performance contracts and project services agreements rather than a metered API. FOCUS mappings remain conceptual until a metered API offering is published.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Ameresco, Inc.
  ProviderName: Ameresco
  PublisherName: Ameresco, Inc.
  ServiceCategory: Energy Services
  ServiceName: Ameresco API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until Ameresco publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: Ameresco Finops
provider_name: Ameresco
provider_slug: ameresco
publisher_name: Ameresco, Inc.
service_category: Energy Services
slug: ameresco-finops
source_filename: ameresco-finops.yml
source_heading: FinOps Profile
source_url: https://www.ameresco.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ameresco\nproviderId: ameresco\npublisherName: Ameresco, Inc.\nserviceCategory: Energy Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy Efficiency\n  - Clean Energy\n  - Services\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for Ameresco. The company invoices customers under energy performance contracts and project services agreements rather than a metered API. FOCUS mappings remain conceptual until a metered API offering is published.\nnotes: >-\n  Ameresco is an energy services company (ESCO) delivering performance contracts, distributed generation, and asset management to public-sector and large commercial customers. It does not publish a public API developer portal with documented pricing or rate limits. Reconcile if Ameresco publishes a public API.\nsources:\n  - https://www.ameresco.com\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Ameresco API\n  ServiceCategory: Energy Services\n  ProviderName: Ameresco\n  PublisherName: Ameresco, Inc.\n  InvoiceIssuerName: Ameresco, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until Ameresco publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage\
  \ API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the Ameresco service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the Ameresco relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ameresco/refs/heads/main/finops/ameresco-finops.yml
sources:
- https://www.ameresco.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Energy Efficiency
- Clean Energy
- Services
- FinOps
- FOCUS
---
