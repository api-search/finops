---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: greenhouse-harvest-openapi.yml
  format: yaml
  label: Greenhouse Harvest API
  slug: harvest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-harvest-openapi.yml
- filename: greenhouse-job-board-openapi.yml
  format: yaml
  label: Greenhouse Job Board API
  slug: job-board
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-job-board-openapi.yml
- filename: greenhouse-ingestion-openapi.yml
  format: yaml
  label: Greenhouse Candidate Ingestion API
  slug: ingestion
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-ingestion-openapi.yml
- filename: greenhouse-onboarding-openapi.yml
  format: yaml
  label: Greenhouse Onboarding API
  slug: onboarding
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-onboarding-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Greenhouse: tiered annual subscription (Core / Plus / Pro) with custom pricing per customer; APIs included at no per-call charge. Cost grows with tier and with employee / hiring-team count rather than with API volume.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Greenhouse Software, Inc.
  ProviderName: Greenhouse
  PublisherName: Greenhouse Software, Inc.
  ServiceCategory: Recruiting / ATS SaaS
  ServiceName: Greenhouse
layout: finops
meters:
- aggregation: sum
  description: Annual platform subscription fee per tier
  dimensions:
  - tier
  name: subscription_fee
  unit: year
- aggregation: max
  description: Hiring team seats provisioned (scoping factor for tier sizing)
  dimensions:
  - team
  - region
  name: hiring_team_seats
  unit: seat
- aggregation: sum
  description: API requests across Harvest / Job Board / Candidate Ingestion / Onboarding (operational metric, not directly billed)
  dimensions:
  - api
  - integration
  name: api_requests
  unit: request
- aggregation: sum
  description: Outbound webhook deliveries
  dimensions:
  - event_type
  name: webhook_deliveries
  unit: event
name: Greenhouse Finops
provider_name: Greenhouse
provider_slug: greenhouse
publisher_name: Greenhouse Software, Inc.
service_category: Recruiting / ATS SaaS
slug: greenhouse-finops
source_filename: greenhouse-finops.yml
source_heading: FinOps Profile
source_url: https://www.greenhouse.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Greenhouse\nproviderId: greenhouse\npublisherName: Greenhouse Software, Inc.\nserviceCategory: Recruiting / ATS SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - ATS\n  - Recruiting\n  - HR\ndescription: 'FOCUS-aligned FinOps for Greenhouse: tiered annual subscription (Core / Plus / Pro)\n  with custom pricing per customer; APIs included at no per-call charge. Cost grows with tier and\n  with employee / hiring-team count rather than with API volume.'\nsources:\n  - https://www.greenhouse.com/pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Greenhouse\n  ServiceCategory: Recruiting / ATS SaaS\n  ProviderName: Greenhouse\n  PublisherName: Greenhouse Software, Inc.\n  InvoiceIssuerName: Greenhouse Software, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_fee\n    description: Annual platform subscription fee per tier\n    unit: year\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: hiring_team_seats\n    description: Hiring team seats provisioned (scoping factor for tier sizing)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - team\n      - region\n  - name: api_requests\n    description: API requests across Harvest / Job Board / Candidate Ingestion / Onboarding\n      (operational metric, not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - integration\n  - name: webhook_deliveries\n    description: Outbound\
  \ webhook deliveries\n    unit: event\n    aggregation: sum\n    dimensions:\n      - event_type\nprinciples:\n  - name: Visibility\n    description: Use Greenhouse usage reports plus integration logs (Harvest X-RateLimit-Remaining\n      values) to understand consumption profile and pre-empt limit pressure.\n  - name: Allocation\n    description: Map hiring teams / business units to Greenhouse user groups so the annual\n      subscription can be allocated by hiring volume per division.\n  - name: Optimization\n    description: Right-size tier (Core vs Plus vs Pro) to actual hiring complexity and feature\n      need; consolidate redundant integrations to limit API and webhook fan-out; clean up\n      inactive users at renewal.\n  - name: Accountability\n    description: Designate a Talent / People-Ops owner accountable for the Greenhouse contract\n      and integration health; review usage at renewal time.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/finops/greenhouse-finops.yml
sources:
- https://www.greenhouse.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- ATS
- Recruiting
- HR
---
