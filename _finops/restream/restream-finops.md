---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: restream-openapi.yml
  format: yaml
  label: Restream API
  slug: restream-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/restream/refs/heads/main/openapi/restream-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Restream. Restream is sold as a tiered SaaS subscription with optional Clips add-on packs and per-seat charges on the Business tier. There is no per-API-request meter; spend scales with the subscription tier and add-on packs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Restream, Inc.
  ProviderName: Restream
  PublisherName: Restream, Inc.
  ServiceCategory: Live Streaming
  ServiceName: Restream
layout: finops
meters:
- aggregation: max
  dimensions:
  - tier
  name: subscription_tier
  unit: month
- aggregation: sum
  name: team_seats
  unit: seat
- aggregation: sum
  dimensions:
  - tier
  name: clips_addon
  unit: clip
- aggregation: max
  dimensions:
  - tier
  name: simultaneous_channels
  unit: channel
name: Restream Finops
provider_name: Restream
provider_slug: restream
publisher_name: Restream, Inc.
service_category: Live Streaming
slug: restream-finops
source_filename: restream-finops.yml
source_heading: FinOps Profile
source_url: https://restream.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Restream\nproviderId: restream\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Live Streaming\n  - Multistreaming\ndescription: FOCUS-aligned FinOps for Restream. Restream is sold as a tiered SaaS subscription with optional\n  Clips add-on packs and per-seat charges on the Business tier. There is no per-API-request meter; spend\n  scales with the subscription tier and add-on packs.\nsources:\n  - https://restream.io/pricing\n  - https://developers.restream.io/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Restream, Inc.\nserviceCategory: Live Streaming\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Restream\n  ServiceCategory: Live Streaming\n  ProviderName: Restream\n  PublisherName: Restream, Inc.\n  InvoiceIssuerName: Restream, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_tier\n    unit: month\n    aggregation: max\n    dimensions:\n      - tier\n  - name: team_seats\n    unit: seat\n    aggregation: sum\n  - name: clips_addon\n    unit: clip\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: simultaneous_channels\n    unit: channel\n    aggregation: max\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Restream account billing page (subscription, team seats, Clips\n      add-on). There is no usage-API export; surface the billing page to finance and the team owner.\n  - name: Allocation\n    description: Allocate the subscription and Clips add-on to\
  \ the production team or show that uses\n      the workspace. On Business, allocate per team-workspace seat.\n  - name: Optimization\n    description: Optimize by tier-fit — match the simultaneous-channel cap to actual destinations used,\n      drop unused team seats on Business, and size Clips packs to actual clip volume rather than buying\n      headroom.\n  - name: Accountability\n    description: Owner is the production / broadcast lead who controls the Restream workspace and selects\n      the subscription tier.\nnotes: Tiered SaaS subscription with seat and Clips add-ons; no per-request meter exists. Generic\n  per-call FOCUS columns and meters removed.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/restream/refs/heads/main/finops/restream-finops.yml
sources:
- https://restream.io/pricing
- https://developers.restream.io/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Live Streaming
- Multistreaming
---
