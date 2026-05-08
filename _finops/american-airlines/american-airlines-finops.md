---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: american-airlines-runway-developer-api-openapi.yml
  format: yaml
  label: American Airlines Runway Developer API
  slug: runway-developer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/american-airlines/refs/heads/main/openapi/american-airlines-runway-developer-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Enterprise / Bilateral
description: FinOps scaffold for American Airlines. Runway is internal cost (allocated through engineering chargeback) rather than an externally invoiced API. External travel-distribution flows are settled through GDS / NDC commercial agreements. FOCUS mappings remain conceptual.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: American Airlines, Inc.
  ProviderName: American Airlines
  PublisherName: American Airlines, Inc.
  ServiceCategory: Airlines / Travel
  ServiceName: American Airlines Runway Developer API
layout: finops
meters:
- aggregation: sum
  description: Placeholder meter for engagements settled outside a metered API. Real meters cannot be enumerated until American Airlines publishes a metered API billing surface.
  name: contracted_engagement
  unit: varies
name: American Airlines Finops
provider_name: American Airlines
provider_slug: american-airlines
publisher_name: American Airlines, Inc.
service_category: Airlines / Travel
slug: american-airlines-finops
source_filename: american-airlines-finops.yml
source_heading: FinOps Profile
source_url: https://developer.aa.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: American Airlines\nproviderId: american-airlines\npublisherName: American Airlines, Inc.\nserviceCategory: Airlines / Travel\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Airlines\n  - Aviation\n  - Flights\n  - Travel\n  - Booking\n  - Developer Experience\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps scaffold for American Airlines. Runway is internal cost (allocated through engineering chargeback) rather than an externally invoiced API. External travel-distribution flows are settled through GDS / NDC commercial agreements. FOCUS mappings remain conceptual.\nnotes: >-\n  American Airlines' Runway platform (built on Spotify Backstage) is American Airlines' internal developer experience for engineering teams - not a publicly consumable, priced API. External flight data, booking, and status integrations are delivered through GDS\
  \ partners (Sabre, Amadeus) and corporate / NDC channels under bilateral agreements. No public price list or rate-limit documentation is published. Reconcile if a public API tier emerges.\nsources:\n  - https://developer.aa.com/\n  - https://github.com/AmericanAirlines\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Enterprise / Bilateral\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: American Airlines Runway Developer API\n  ServiceCategory: Airlines / Travel\n  ProviderName: American Airlines\n  PublisherName: American Airlines, Inc.\n  InvoiceIssuerName: American Airlines, Inc.\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Purchase\nmeters:\n  - name: contracted_engagement\n    description: >-\n      Placeholder meter for engagements settled outside a metered API. Real\n      meters cannot be enumerated until American Airlines publishes a metered\n      API billing surface.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: >-\n      Without a public usage API, consumers must rely on contract reporting,\n      invoice line items, and any tenant dashboards provided under the\n      partner agreement.\n  - name: Allocation\n    description: >-\n      Allocate spend by purchase order, contract identifier, or business unit\n      receiving the American Airlines service. Tag at the procurement layer, not\n      the API call layer.\n  - name: Optimization\n    description: >-\n      Optimization levers live in commercial negotiation (volume commitments,\n      term length, scope) rather than in API-level caching or throttling.\n  - name: Accountability\n    description:\
  \ >-\n      Procurement and the business owner of the American Airlines relationship own\n      the spend; finance reviews invoice lines on the contract cadence.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/american-airlines/refs/heads/main/finops/american-airlines-finops.yml
sources:
- https://developer.aa.com/
- https://github.com/AmericanAirlines
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Airlines
- Aviation
- Flights
- Travel
- Booking
- Developer Experience
- FinOps
- FOCUS
---
