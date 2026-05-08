---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: EUR/USD
  billingFrequency: Monthly (consumer)
  chargeCategories:
  - Subscription
  pricingCategory: Free / Subscription
description: FOCUS-aligned FinOps profile for Deezer. API access is free and not invoiced. Cost concentration is on the consumer subscription side (Premium, Family, HiFi, Student), which is billed directly by Deezer to end users.
focus_columns:
  BillingCurrency: EUR
  ChargeCategory: Subscription
  InvoiceIssuerName: Deezer
  ProviderName: Deezer
  PublisherName: Deezer
  ServiceCategory: Music Streaming
  ServiceName: Deezer API
layout: finops
meters:
- aggregation: sum
  description: API request count (free; observability only).
  dimensions:
  - app
  - endpoint
  name: api_requests
  unit: request
- aggregation: count
  description: Deezer consumer subscription billing.
  dimensions:
  - tier
  - country
  name: consumer_subscription
  unit: month
name: Deezer Finops
provider_name: Deezer
provider_slug: deezer
publisher_name: Deezer
service_category: Music Streaming
slug: deezer-finops
source_filename: deezer-finops.yml
source_heading: FinOps Profile
source_url: https://developers.deezer.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Deezer\nproviderId: deezer\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Music\n- Streaming\n- Audio\n- OAuth\n- Catalog\n- Playlists\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Deezer. API access is free and not invoiced. Cost concentration is\n  on the consumer subscription side (Premium, Family, HiFi, Student), which is billed directly by\n  Deezer to end users.\nnotes: API is free; consumer subscriptions billed to end users by Deezer.\nsources:\n- https://developers.deezer.com/\n- https://www.deezer.com/offers\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Deezer\nserviceCategory: Music Streaming\n\
  billingModel:\n  pricingCategory: Free / Subscription\n  billingFrequency: Monthly (consumer)\n  billingCurrency: EUR/USD\n  chargeCategories:\n  - Subscription\nfocusColumns:\n  ServiceName: Deezer API\n  ServiceCategory: Music Streaming\n  ProviderName: Deezer\n  PublisherName: Deezer\n  InvoiceIssuerName: Deezer\n  BillingCurrency: EUR\n  ChargeCategory: Subscription\nmeters:\n- name: api_requests\n  description: API request count (free; observability only).\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app\n  - endpoint\n- name: consumer_subscription\n  description: Deezer consumer subscription billing.\n  unit: month\n  aggregation: count\n  dimensions:\n  - tier\n  - country\nprinciples:\n- name: Visibility\n  description: No API invoice; track usage internally for performance and quota planning.\n- name: Allocation\n  description: Allocate any consumer subscriptions to the team or program owning them.\n- name: Optimization\n  description: Cache catalog responses to stay\
  \ under the 50 req / 5s ceiling.\n- name: Accountability\n  description: App owner manages the Deezer developer registration and OAuth client.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deezer/refs/heads/main/finops/deezer-finops.yml
sources:
- https://developers.deezer.com/
- https://www.deezer.com/offers
specification: FinOps Framework
tags:
- Music
- Streaming
- Audio
- OAuth
- Catalog
- Playlists
- FinOps
- Cost Management
- FOCUS
---
