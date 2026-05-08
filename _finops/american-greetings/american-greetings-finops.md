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
description: FinOps scaffold for American Greetings. The company invoices retailers and licensees under standard CPG trade terms rather than a metered API. FOCUS mappings remain conceptual.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: American Greetings Corporation
  ProviderName: American Greetings
  PublisherName: American Greetings Corporation
  ServiceCategory: Consumer Goods / Retail
  ServiceName: American Greetings API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until American Greetings publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: American Greetings Finops
provider_name: American Greetings
provider_slug: american-greetings
publisher_name: American Greetings Corporation
service_category: Consumer Goods / Retail
slug: american-greetings-finops
source_filename: american-greetings-finops.yml
source_heading: FinOps Profile
source_url: https://www.americangreetings.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: American Greetings\nproviderId: american-greetings\npublisherName: American Greetings Corporation\nserviceCategory: Consumer Goods / Retail\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Greeting Cards\n  - Gift Wrap\n  - Celebration\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for American Greetings. The company invoices retailers and licensees under standard CPG trade terms rather than a metered API. FOCUS mappings remain conceptual.\nnotes: >-\n  American Greetings is a consumer-products company; it does not publish a public API developer portal with documented pricing or rate limits. Retail trading-partner EDI and Creatacard / SmashUps consumer products are sold direct rather than via a priced API. Reconcile if a public API is launched.\nsources:\n  - https://www.americangreetings.com\n  - https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: American Greetings API\n  ServiceCategory: Consumer Goods / Retail\n  ProviderName: American Greetings\n  PublisherName: American Greetings Corporation\n  InvoiceIssuerName: American Greetings Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until American Greetings publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n\
  \  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the American Greetings service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description: >-\n      Procurement and the business owner of the American Greetings relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/american-greetings/refs/heads/main/finops/american-greetings-finops.yml
sources:
- https://www.americangreetings.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Greeting Cards
- Gift Wrap
- Celebration
- FinOps
- FOCUS
---
