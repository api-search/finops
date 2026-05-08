---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: smartbear-swaggerhub-openapi.yml
  format: yaml
  label: SwaggerHub API
  slug: swaggerhub
  spec_type: OpenAPI
  url: https://openapi/smartbear-swaggerhub-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: 'FOCUS-aligned FinOps placeholder for SmartBear: portfolio of design, testing, and observability tools sold per-product with contact-sales pricing; meters below describe the typical invoice-line shape but unit prices are set per signed agreement.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SmartBear Software, Inc.
  ProviderName: SmartBear
  PublisherName: SmartBear Software, Inc.
  ServiceCategory: API Design / Testing / Observability
  ServiceName: SmartBear
layout: finops
meters:
- aggregation: max
  description: Designer seats licensed in SwaggerHub / SwaggerHub Portal.
  dimensions:
  - product
  - environment
  name: swaggerhub_seats
  unit: seat
- aggregation: max
  description: ReadyAPI floating / named licenses.
  dimensions:
  - product
  name: readyapi_seats
  unit: seat
- aggregation: max
  description: TestComplete user / runtime licenses.
  dimensions:
  - product
  name: testcomplete_seats
  unit: seat
- aggregation: sum
  description: BugSnag billable error / session events.
  dimensions:
  - project
  - environment
  name: bugsnag_events
  unit: event
- aggregation: max
  description: AlertSite synthetic monitor count.
  dimensions:
  - location
  name: alertsite_monitors
  unit: varies
name: Smartbear Finops
provider_name: SmartBear
provider_slug: smartbear
publisher_name: SmartBear Software, Inc.
service_category: API Design / Testing / Observability
slug: smartbear-finops
source_filename: smartbear-finops.yml
source_heading: FinOps Profile
source_url: https://smartbear.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SmartBear\nproviderId: smartbear\npublisherName: SmartBear Software, Inc.\nserviceCategory: API Design / Testing / Observability\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Design\n  - API Testing\n  - Observability\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for SmartBear: portfolio of design, testing, and\n  observability tools sold per-product with contact-sales pricing; meters below describe the typical\n  invoice-line shape but unit prices are set per signed agreement.'\nsources:\n  - https://smartbear.com/\nnotes: |\n  No unified public price list. Meters reflect the typical SmartBear\
  \ invoice line items (per-product\n  seat / agent / project counts) but the actual unit prices come from each customer's order form.\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: SmartBear\n  ServiceCategory: API Design / Testing / Observability\n  ProviderName: SmartBear\n  PublisherName: SmartBear Software, Inc.\n  InvoiceIssuerName: SmartBear Software, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: swaggerhub_seats\n    description: Designer seats licensed in SwaggerHub / SwaggerHub Portal.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n      - environment\n  - name: readyapi_seats\n    description: ReadyAPI floating / named licenses.\n    unit: seat\n    aggregation: max\n    dimensions:\n      - product\n  - name: testcomplete_seats\n    description: TestComplete user / runtime licenses.\n    unit: seat\n    aggregation: max\n    dimensions:\n\
  \      - product\n  - name: bugsnag_events\n    description: BugSnag billable error / session events.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - project\n      - environment\n  - name: alertsite_monitors\n    description: AlertSite synthetic monitor count.\n    unit: varies\n    aggregation: max\n    dimensions:\n      - location\nprinciples:\n  - name: Visibility\n    description: Aggregate seat / event / monitor counts from each product's admin console; SmartBear\n      does not provide a unified consumption export across the portfolio.\n  - name: Allocation\n    description: Allocate per product line and per consuming team by mapping each SwaggerHub project,\n      BugSnag project, or ReadyAPI seat to its owning engineering team.\n  - name: Optimization\n    description: Reclaim inactive SwaggerHub / ReadyAPI seats; tune BugSnag sampling and AlertSite\n      monitor cadence to keep event / monitor counts within tier caps.\n  - name: Accountability\n    description:\
  \ API platform owner reconciles monthly per-product utilization against the annual\n      order forms and approves seat additions or product expansions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/smartbear/refs/heads/main/finops/smartbear-finops.yml
sources:
- https://smartbear.com/
specification: FinOps Framework
tags:
- API Design
- API Testing
- Observability
- FinOps
- FOCUS
---
