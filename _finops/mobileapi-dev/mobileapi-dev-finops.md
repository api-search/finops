---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mobileapi-openapi.yml
  format: yaml
  label: MobileAPI
  slug: mobileapi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mobileapi-dev/refs/heads/main/openapi/mobileapi-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  paymentProcessor: Stripe
  pricingCategory: Tiered Subscription with Monthly Request Quota
  refundPolicy: 30-day money-back guarantee on paid plans
description: FOCUS-aligned FinOps view for MobileAPI.dev. Billing is a flat-rate monthly subscription per API key, gated by request quota; the only public meter is total successful requests against the quota. Enterprise overage and custom rates are negotiated outside the public surface.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  ChargeFrequency: Recurring
  CommitmentDiscountCategory: Spend
  PricingCategory: Standard
  ProviderName: MobileAPI.dev
  PublisherName: MobileAPI.dev
  ServiceCategory: Data API
  ServiceName: MobileAPI
layout: finops
meters:
- aggregation: sum
  description: Total successful API requests counted against the monthly quota; visible via X-RateLimit-Remaining header.
  name: api_requests
  unit: request
- aggregation: sum
  description: Subset of api_requests routed to /devices/ai-query/; only available on Pro/Enterprise.
  name: ai_query_requests
  unit: request
- aggregation: sum
  description: HTTP 429 responses; not directly billed but indicate quota saturation.
  name: rate_limit_violations
  unit: event
name: Mobileapi Dev Finops
provider_name: MobileAPI.dev
provider_slug: mobileapi-dev
publisher_name: MobileAPI.dev
service_category: Data API - Device Specifications
slug: mobileapi-dev-finops
source_filename: mobileapi-dev-finops.yml
source_heading: FinOps Profile
source_url: https://mobileapi.dev/#pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: MobileAPI.dev\nproviderId: mobileapi-dev\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Device Specifications\n  - Mobile Devices\ndescription: >-\n  FOCUS-aligned FinOps view for MobileAPI.dev. Billing is a flat-rate monthly\n  subscription per API key, gated by request quota; the only public meter is\n  total successful requests against the quota. Enterprise overage and custom\n  rates are negotiated outside the public surface.\nsources:\n  - https://mobileapi.dev/#pricing\n  - https://mobileapi.dev/docs/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: MobileAPI.dev\nserviceCategory: Data API - Device Specifications\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription with Monthly Request Quota\n  billingFrequency: Monthly\n  billingCurrency: USD\n  paymentProcessor: Stripe\n  refundPolicy: 30-day money-back guarantee on paid plans\nfocusColumns:\n  ServiceName: MobileAPI\n  ServiceCategory: Data API\n  ProviderName: MobileAPI.dev\n  PublisherName: MobileAPI.dev\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  ChargeFrequency: Recurring\n  PricingCategory: Standard\n  CommitmentDiscountCategory: Spend\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    description: Total successful API requests counted against the monthly quota; visible via X-RateLimit-Remaining header.\n  - name: ai_query_requests\n    unit: request\n    aggregation: sum\n    description: Subset of api_requests routed to /devices/ai-query/; only available on Pro/Enterprise.\n  - name: rate_limit_violations\n    unit: event\n    aggregation: sum\n    description: HTTP 429 responses; not directly billed but indicate\
  \ quota saturation.\ncostAllocationDimensions:\n  - name: APIKey\n    description: Each issued API key is the natural cost-allocation unit.\n  - name: Plan\n    description: Free / Pro / Enterprise determines the unit cost.\n  - name: Environment\n    description: Customers commonly issue separate keys per dev/stage/prod for chargeback.\nprinciples:\n  - name: Visibility\n    description: >-\n      Track monthly request totals and remaining quota via X-RateLimit-Remaining /\n      X-RateLimit-Reset headers and the /me/ endpoint.\n  - name: Allocation\n    description: >-\n      Issue per-team or per-environment API keys so request volumes can be tagged\n      back to a specific cost center without provider-side support.\n  - name: Optimization\n    description: >-\n      Cache device records aggressively; the data refreshes weekly on Pro and\n      daily on Enterprise, so most reads are safely cached. Use autocomplete\n      ahead of search to reduce wasted lookups.\n  - name: Accountability\n\
  \    description: >-\n      Set spend alerts at 80% and 100% of monthly quota (the provider also\n      emails at these thresholds). Promote keys from Free to Pro before quota\n      exhaustion to avoid 429s in production.\nnotes:\n  - Enterprise rates are not publicly listed; negotiate overage and per-call rates with sales.\n  - Stripe webhook /payment_successful is the only documented billing-event integration surface.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mobileapi-dev/refs/heads/main/finops/mobileapi-dev-finops.yml
sources:
- https://mobileapi.dev/#pricing
- https://mobileapi.dev/docs/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Device Specifications
- Mobile Devices
---
