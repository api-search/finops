---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (developer) / Monthly (consumer)
  chargeCategories:
  - Purchase
  - Subscription
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile for Apple Music. The Apple Music API does not bill per-call. The two cost lines are (1) the annual Apple Developer Program fee and (2) end-user Apple Music subscriptions consumed by app users. Apple does not invoice apps for catalog calls.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Apple Inc.
  ProviderName: Apple Inc.
  PublisherName: Apple Inc.
  ServiceCategory: Music Streaming
  ServiceName: Apple Music
layout: finops
meters:
- aggregation: sum
  description: Annual Apple Developer Program membership.
  dimensions:
  - team_id
  name: developer_program_membership
  unit: year
- aggregation: count
  description: Apple Music subscription billed directly to the end user.
  dimensions:
  - tier
  - country
  name: end_user_subscription
  unit: month
name: Apple Music Finops
provider_name: Apple Music
provider_slug: apple-music
publisher_name: Apple Inc.
service_category: Music Streaming
slug: apple-music-finops
source_filename: apple-music-finops.yml
source_heading: FinOps Profile
source_url: https://developer.apple.com/programs/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Apple Music\nproviderId: apple-music\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Music\n- Streaming\n- Apple\n- MusicKit\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Apple Music. The Apple Music API does not bill per-call. The two cost lines are (1) the annual Apple Developer Program fee and (2) end-user Apple Music subscriptions consumed by app users. Apple does not invoice apps for catalog calls.\nnotes: API is free with the Developer Program; consumer subscriptions are billed directly by Apple to end users, not to the app developer.\nsources:\n- https://developer.apple.com/programs/\n- https://developer.apple.com/documentation/applemusicapi\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Apple Inc.\nserviceCategory: Music Streaming\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual (developer) / Monthly (consumer)\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Subscription\nfocusColumns:\n  ServiceName: Apple Music\n  ServiceCategory: Music Streaming\n  ProviderName: Apple Inc.\n  PublisherName: Apple Inc.\n  InvoiceIssuerName: Apple Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: developer_program_membership\n  description: Annual Apple Developer Program membership.\n  unit: year\n  aggregation: sum\n  dimensions:\n  - team_id\n- name: end_user_subscription\n  description: Apple Music subscription billed directly to the end user.\n  unit: month\n  aggregation: count\n  dimensions:\n  - tier\n  - country\nprinciples:\n- name: Visibility\n  description: Track Apple Developer Program\
  \ renewals; understand subscriber-mix drives feature availability, not your cost.\n- name: Allocation\n  description: Allocate Developer Program cost to the team owning the MusicKit identifier.\n- name: Optimization\n  description: No call-level optimization needed; cache catalog data and minimize repeated lookups.\n- name: Accountability\n  description: Single team owns the MusicKit identifier and signing key.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/apple-music/refs/heads/main/finops/apple-music-finops.yml
sources:
- https://developer.apple.com/programs/
- https://developer.apple.com/documentation/applemusicapi
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Music
- Streaming
- Apple
- MusicKit
- FinOps
- Cost Management
- FOCUS
---
