---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openmercantil-openapi.yml
  format: yaml
  label: OpenMercantil Public API
  slug: openmercantil-public-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openmercantil/refs/heads/main/openapi/openmercantil-openapi.yml
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly Or Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  paymentProcessor: Stripe
  pricingCategory: Subscription + One-Time Donation
  vatHandling: Spanish VAT (21%) added at checkout where applicable
description: FOCUS-aligned FinOps framing for OpenMercantil. The public REST API is free and rate-limited; commercial surface is a flat-rate website / dataset subscription (Profesional / MAX) plus optional one-time donations. There is no metered per-request billing on the public API, so cost-allocation meters here track subscription seats and donation revenue rather than API usage.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: OpenMercantil
  ProviderName: OpenMercantil
  PublisherName: OpenMercantil
  ServiceCategory: Open Data
  ServiceName: OpenMercantil
layout: finops
meters:
- aggregation: count
  dimensions:
  - plan
  - billingCycle
  name: subscription_seats
  unit: seat
- aggregation: sum
  dimensions:
  - plan
  - billingCycle
  name: subscription_revenue
  unit: EUR
- aggregation: sum
  dimensions:
  - source
  name: donation_revenue
  unit: EUR
- aggregation: count
  dimensions:
  - endpoint
  - sourceIp
  name: free_api_requests
  unit: request
name: Openmercantil Finops
provider_name: OpenMercantil
provider_slug: openmercantil
publisher_name: OpenMercantil
service_category: Open Data / Public Records
slug: openmercantil-finops
source_filename: openmercantil-finops.yml
source_heading: FinOps Profile
source_url: https://openmercantil.es/precios
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenMercantil\nproviderId: openmercantil\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Open Data\n  - Spain\n  - Company Data\n  - BORME\ndescription: >-\n  FOCUS-aligned FinOps framing for OpenMercantil. The public REST API is free\n  and rate-limited; commercial surface is a flat-rate website / dataset\n  subscription (Profesional / MAX) plus optional one-time donations. There is\n  no metered per-request billing on the public API, so cost-allocation meters\n  here track subscription seats and donation revenue rather than API usage.\nnotes: >-\n  No metered API pricing is published by OpenMercantil. Pricing is flat\n  monthly/annual subscription via Stripe with optional one-time donations.\n  Reconcile if a usage-priced API tier becomes available.\nsources:\n  - https://openmercantil.es/precios\n  - https://openmercantil.es/api/documentacion\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenMercantil\nserviceCategory: Open Data / Public Records\nbillingModel:\n  pricingCategory: Subscription + One-Time Donation\n  billingFrequency: Monthly Or Annual\n  billingCurrency: EUR\n  vatHandling: Spanish VAT (21%) added at checkout where applicable\n  paymentProcessor: Stripe\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: OpenMercantil\n  ServiceCategory: Open Data\n  ProviderName: OpenMercantil\n  PublisherName: OpenMercantil\n  InvoiceIssuerName: OpenMercantil\n  BillingCurrency: EUR\nmeters:\n  - name: subscription_seats\n    unit: seat\n    aggregation: count\n    dimensions:\n      - plan\n      - billingCycle\n  - name: subscription_revenue\n    unit: EUR\n    aggregation: sum\n\
  \    dimensions:\n      - plan\n      - billingCycle\n  - name: donation_revenue\n    unit: EUR\n    aggregation: sum\n    dimensions:\n      - source\n  - name: free_api_requests\n    unit: request\n    aggregation: count\n    dimensions:\n      - endpoint\n      - sourceIp\nprinciples:\n  - name: Visibility\n    description: >-\n      Reconcile Stripe invoice exports against the Profesional and MAX plan\n      definitions; track donation income as a separate revenue line. Public\n      API traffic is not invoiced but should be observed for capacity planning.\n  - name: Allocation\n    description: >-\n      Allocate seats and donation revenue back to project budgets. Allocate\n      free-tier API traffic by endpoint and source-IP cohort for\n      infrastructure cost attribution.\n  - name: Optimization\n    description: >-\n      Encourage consumers to use export endpoints and CSV downloads rather\n      than per-record looped requests to reduce upstream BORME and Nominatim\n      lookup\
  \ costs. Cache the geocode and sources/status endpoints aggressively.\n  - name: Accountability\n    description: >-\n      OpenMercantil treasurer/owner reviews monthly Stripe statements and\n      donation totals; engineering reviews per-endpoint request volume for\n      free-tier infrastructure cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openmercantil/refs/heads/main/finops/openmercantil-finops.yml
sources:
- https://openmercantil.es/precios
- https://openmercantil.es/api/documentacion
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Open Data
- Spain
- Company Data
- BORME
---
