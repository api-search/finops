---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription with Word Allowance
description: FOCUS-aligned FinOps view of PlayHT. PlayHT bills as monthly subscription tiers with bundled word allowances (5K / 600K / unlimited). API access requires Enterprise tier. Effective per-character cost depends on plan tier and actual usage.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: PlayHT
  ProviderName: PlayHT
  PublisherName: PlayHT
  ServiceCategory: AI
  ServiceName: PlayHT TTS API
layout: finops
meters:
- aggregation: sum
  description: Words sent to TTS synthesis (drawn down from monthly allowance).
  dimensions:
  - account
  - voice
  name: words_synthesized
  unit: word
- aggregation: max
  description: PlayHT subscription seats per plan tier.
  dimensions:
  - account
  - plan
  name: subscription_seats
  unit: seat
- aggregation: max
  description: Voice clone count under enterprise plans.
  dimensions:
  - account
  name: voice_clones
  unit: clone
name: Play Ht Finops
provider_name: PlayHT
provider_slug: play-ht
publisher_name: PlayHT
service_category: AI
slug: play-ht-finops
source_filename: play-ht-finops.yml
source_heading: FinOps Profile
source_url: https://play.ht/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PlayHT\nproviderId: play-ht\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- TTS\n- Voice Cloning\n- Audio\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of PlayHT. PlayHT bills as monthly subscription tiers with\n  bundled word allowances (5K / 600K / unlimited). API access requires Enterprise tier.\n  Effective per-character cost depends on plan tier and actual usage.\nnotes: Plan-tier sizing is the dominant FinOps lever; calculate effective per-word cost vs alternatives at expected monthly volume.\nsources:\n- https://play.ht/pricing/\n- https://docs.play.ht/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: PlayHT\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription with Word Allowance\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: PlayHT TTS API\n  ServiceCategory: AI\n  ProviderName: PlayHT\n  PublisherName: PlayHT\n  InvoiceIssuerName: PlayHT\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: words_synthesized\n  description: Words sent to TTS synthesis (drawn down from monthly allowance).\n  unit: word\n  aggregation: sum\n  dimensions:\n  - account\n  - voice\n- name: subscription_seats\n  description: PlayHT subscription seats per plan tier.\n  unit: seat\n  aggregation: max\n  dimensions:\n  - account\n  - plan\n- name: voice_clones\n  description: Voice clone count under enterprise plans.\n  unit: clone\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track word burn against monthly plan\
  \ allowance in PlayHT studio.\n- name: Allocation\n  description: Tag voices and integrations to consuming business units.\n- name: Optimization\n  description: Move to Premium when Professional 600K/month is consistently exceeded; negotiate Enterprise for production API.\n- name: Accountability\n  description: Assign owner per plan and per integration consuming TTS.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/play-ht/refs/heads/main/finops/play-ht-finops.yml
sources:
- https://play.ht/pricing/
- https://docs.play.ht/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- TTS
- Voice Cloning
- Audio
- FinOps
- Cost Management
- FOCUS
---
