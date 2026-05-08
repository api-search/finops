---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (consumer)
  chargeCategories:
  - Subscription
  pricingCategory: Free / Subscription
description: FOCUS-aligned FinOps profile for SoundCloud. The API itself has no per-call charge for approved partners; cost concentration is on the consumer subscription side (Go, Go+, Artist Pro, Pro Unlimited) and on creator tooling. Treat the API as a free dependency once approved.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: SoundCloud
  ProviderName: SoundCloud
  PublisherName: SoundCloud
  ServiceCategory: Music Streaming
  ServiceName: SoundCloud API
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
  description: Consumer (listener/creator) subscription tier billing.
  dimensions:
  - tier
  name: consumer_subscription
  unit: month
name: Soundcloud Finops
provider_name: SoundCloud
provider_slug: soundcloud
publisher_name: SoundCloud
service_category: Music Streaming
slug: soundcloud-finops
source_filename: soundcloud-finops.yml
source_heading: FinOps Profile
source_url: https://developers.soundcloud.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SoundCloud\nproviderId: soundcloud\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Music\n- Streaming\n- Audio\n- OAuth\n- Tracks\n- Playlists\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for SoundCloud. The API itself has no per-call charge for approved\n  partners; cost concentration is on the consumer subscription side (Go, Go+, Artist Pro, Pro\n  Unlimited) and on creator tooling. Treat the API as a free dependency once approved.\nnotes: API is free; consumer/creator subscriptions are billed separately by SoundCloud.\nsources:\n- https://developers.soundcloud.com/\n- https://soundcloud.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: SoundCloud\nserviceCategory: Music Streaming\nbillingModel:\n  pricingCategory: Free / Subscription\n  billingFrequency: Monthly (consumer)\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\nfocusColumns:\n  ServiceName: SoundCloud API\n  ServiceCategory: Music Streaming\n  ProviderName: SoundCloud\n  PublisherName: SoundCloud\n  InvoiceIssuerName: SoundCloud\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: api_requests\n  description: API request count (free; observability only).\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app\n  - endpoint\n- name: consumer_subscription\n  description: Consumer (listener/creator) subscription tier billing.\n  unit: month\n  aggregation: count\n  dimensions:\n  - tier\nprinciples:\n- name: Visibility\n  description: Track API usage via internal logs; consumer subscriptions are billed separately.\n- name: Allocation\n  description: Allocate creator tooling subscriptions (Artist Pro, Pro\
  \ Unlimited) to the team or artist that owns the SoundCloud account.\n- name: Optimization\n  description: Cache stream URLs and metadata; avoid burning play-count quota on duplicate requests.\n- name: Accountability\n  description: Single team owns the SoundCloud app credentials and any creator subscriptions.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/soundcloud/refs/heads/main/finops/soundcloud-finops.yml
sources:
- https://developers.soundcloud.com/
- https://soundcloud.com/pricing
specification: FinOps Framework
tags:
- Music
- Streaming
- Audio
- OAuth
- Tracks
- Playlists
- FinOps
- Cost Management
- FOCUS
---
