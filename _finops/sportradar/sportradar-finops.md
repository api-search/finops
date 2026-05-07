---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sportradar-sports-data-openapi.yml
  format: yaml
  label: Sportradar Sports Data API
  slug: sports-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sportradar/refs/heads/main/openapi/sportradar-sports-data-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales
description: FOCUS-aligned FinOps placeholder for Sportradar. Cost is governed by the bilateral data-licensing contract — typically a fixed annual fee plus variable components for matches, streams, or revenue share — rather than a per-API-call meter.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sportradar AG
  ProviderName: Sportradar
  PublisherName: Sportradar AG
  ServiceCategory: Sports Data
  ServiceName: Sportradar
layout: finops
meters:
- aggregation: sum
  description: Placeholder for the contracted data license; the actual billable unit (annual fee, per-match, per-stream, revenue share) varies by product and customer.
  dimensions:
  - sport
  - region
  - use_case
  name: contracted_data_license
  unit: varies
name: Sportradar Finops
provider_name: Sportradar
provider_slug: sportradar
publisher_name: Sportradar AG
service_category: Sports Data Licensing
slug: sportradar-finops
source_filename: sportradar-finops.yml
source_heading: FinOps Profile
source_url: https://sportradar.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sportradar\nproviderId: sportradar\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Sports Data\n  - Media\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Sportradar. Cost is governed by\n  the bilateral data-licensing contract — typically a fixed annual fee plus\n  variable components for matches, streams, or revenue share — rather than a\n  per-API-call meter.\nsources:\n  - https://sportradar.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sportradar AG\nserviceCategory: Sports Data Licensing\nbillingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD (settlement varies)\n\
  \  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sportradar\n  ServiceCategory: Sports Data\n  ProviderName: Sportradar\n  PublisherName: Sportradar AG\n  InvoiceIssuerName: Sportradar AG\n  BillingCurrency: USD\nmeters:\n  - name: contracted_data_license\n    description: Placeholder for the contracted data license; the actual billable\n      unit (annual fee, per-match, per-stream, revenue share) varies by product\n      and customer.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - sport\n      - region\n      - use_case\nprinciples:\n  - name: Visibility\n    description: Visibility is provided through the customer portal and contract\n      reporting deliverables. There is no public usage-API for cost extraction.\n  - name: Allocation\n    description: Costs are allocated against the licensing business unit\n      (sportsbook, media product, league partner) named in the contract.\n  - name: Optimization\n    description: Optimization happens at\
  \ contract renewal — scoping the right\n      sport packages and feed depth for the use case rather than tuning request\n      patterns.\n  - name: Accountability\n    description: Owned by the commercial / product owner that signs the\n      sportsbook or media data agreement.\nnotes: No self-serve per-call billing surface; all commercial relationships are\n  contracted.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sportradar/refs/heads/main/finops/sportradar-finops.yml
sources:
- https://sportradar.com/
specification: FinOps Framework
tags:
- Sports Data
- Media
- FinOps
- FOCUS
---
