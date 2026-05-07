---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: live-nation-entertainment-ticketmaster-discovery-api-openapi.yml
  format: yaml
  label: Ticketmaster Discovery API
  slug: ticketmaster-discovery-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/live-nation-entertainment/refs/heads/main/openapi/live-nation-entertainment-ticketmaster-discovery-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Free API + Affiliate Revenue Share
description: 'FOCUS-aligned FinOps for Live Nation / Ticketmaster: the public Discovery API is free with a 5,000 call/day, 5 req/sec quota, so direct API spend is zero. Commercial value flows through affiliate / partner ticket-sales revenue share rather than API fees. FinOps for consumers focuses on quota headroom (avoid 429s) and affiliate ROI rather than line-item API cost.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Ticketmaster L.L.C.
  ProviderName: Live Nation Entertainment
  PublisherName: Live Nation Entertainment, Inc.
  ServiceCategory: Ticketing / Events
  ServiceName: Ticketmaster Discovery API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api_key
  - endpoint
  - market
  - locale
  name: discovery_api_calls
  unit: request
- aggregation: max
  dimensions:
  - api_key
  name: daily_quota_consumed
  unit: request
- aggregation: sum
  dimensions:
  - partner
  - market
  - event_type
  name: affiliate_referrals
  unit: referral
- aggregation: sum
  dimensions:
  - partner
  - market
  - event_type
  name: affiliate_revenue
  unit: USD
name: Live Nation Entertainment Finops
provider_name: live-nation-entertainment
provider_slug: live-nation-entertainment
publisher_name: Live Nation Entertainment, Inc. / Ticketmaster L.L.C.
service_category: Ticketing / Events
slug: live-nation-entertainment-finops
source_filename: live-nation-entertainment-finops.yml
source_heading: FinOps Profile
source_url: https://developer.ticketmaster.com/products-and-docs/apis/getting-started/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Live Nation Entertainment\nproviderId: live-nation-entertainment\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Ticketing\n  - Events\n  - Venues\ndescription: 'FOCUS-aligned FinOps for Live Nation / Ticketmaster: the public Discovery API is free\n  with a 5,000 call/day, 5 req/sec quota, so direct API spend is zero. Commercial value flows through\n  affiliate / partner ticket-sales revenue share rather than API fees. FinOps for consumers focuses\n  on quota headroom (avoid 429s) and affiliate ROI rather than line-item API cost.'\nsources:\n  - https://developer.ticketmaster.com/products-and-docs/apis/getting-started/\n  - https://developer.ticketmaster.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Live Nation Entertainment, Inc. / Ticketmaster L.L.C.\nserviceCategory: Ticketing / Events\nbillingModel:\n  pricingCategory: Free API + Affiliate Revenue Share\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Ticketmaster Discovery API\n  ServiceCategory: Ticketing / Events\n  ProviderName: Live Nation Entertainment\n  PublisherName: Live Nation Entertainment, Inc.\n  InvoiceIssuerName: Ticketmaster L.L.C.\n  BillingCurrency: USD\nmeters:\n  - name: discovery_api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\n      - market\n      - locale\n  - name: daily_quota_consumed\n    unit: request\n    aggregation: max\n    dimensions:\n      - api_key\n  - name: affiliate_referrals\n    unit: referral\n    aggregation: sum\n    dimensions:\n      - partner\n\
  \      - market\n      - event_type\n  - name: affiliate_revenue\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - partner\n      - market\n      - event_type\nprinciples:\n  - name: Visibility\n    description: Read Rate-Limit / Rate-Limit-Available / Rate-Limit-Reset response headers on every\n      call; export them to your observability platform for headroom dashboards. Use the affiliate /\n      partner reporting portal for revenue share.\n  - name: Allocation\n    description: Issue distinct API keys per integration / brand to attribute Discovery API consumption\n      and to scope quota-increase requests; tag affiliate URLs with sub-IDs for revenue allocation.\n  - name: Optimization\n    description: Cache event / venue / classification results; use search filters and pagination to stay\n      within 5,000/day; throttle clients to 5 req/sec with token-bucket; only request quota increases\n      after compliance / branding review readiness.\n  - name: Accountability\n\
  \    description: Assign an integration owner who watches 429 rate and quota headroom, and a partner-program\n      owner who reviews affiliate revenue against ticket-referral targets each month.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/live-nation-entertainment/refs/heads/main/finops/live-nation-entertainment-finops.yml
sources:
- https://developer.ticketmaster.com/products-and-docs/apis/getting-started/
- https://developer.ticketmaster.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Ticketing
- Events
- Venues
---
