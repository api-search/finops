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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps view of Inworld AI. Inworld combines a credit-based monthly subscription with usage-based meters across TTS (per 1M characters), STT (per hour), and LLM Router (provider passthrough). Higher tiers unlock 20-40% off rates.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Inworld AI
  ProviderName: Inworld AI
  PublisherName: Inworld AI
  ServiceCategory: AI
  ServiceName: Inworld AI Voice and Conversational AI
layout: finops
meters:
- aggregation: sum
  description: TTS character usage priced per 1M characters with tier-based discounts.
  dimensions:
  - account
  - voice_model
  name: tts_characters
  unit: character
- aggregation: sum
  description: Speech-to-Text hour usage at $0.35/hour standard.
  dimensions:
  - account
  name: stt_hours
  unit: hour
- aggregation: sum
  description: Realtime API speech-to-speech included with all plans.
  dimensions:
  - account
  name: realtime_minutes
  unit: minute
- aggregation: sum
  description: LLM Router pass-through token usage at provider cost.
  dimensions:
  - account
  - provider_model
  name: llm_router_tokens
  unit: token
- aggregation: sum
  description: Monthly credit allocation tied to plan tier.
  dimensions:
  - account
  - plan
  name: monthly_credits
  unit: USD
name: Inworld Finops
provider_name: Inworld AI
provider_slug: inworld
publisher_name: Inworld AI
service_category: AI
slug: inworld-finops
source_filename: inworld-finops.yml
source_heading: FinOps Profile
source_url: https://inworld.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Inworld AI\nproviderId: inworld\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- Characters\n- Games\n- Conversational\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Inworld AI. Inworld combines a credit-based monthly\n  subscription with usage-based meters across TTS (per 1M characters), STT (per hour), and\n  LLM Router (provider passthrough). Higher tiers unlock 20-40% off rates.\nnotes: Plan tier sizing materially affects unit costs across all four products.\nsources:\n- https://inworld.ai/pricing\n- https://docs.inworld.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Inworld AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Inworld AI Voice and Conversational AI\n  ServiceCategory: AI\n  ProviderName: Inworld AI\n  PublisherName: Inworld AI\n  InvoiceIssuerName: Inworld AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: tts_characters\n  description: TTS character usage priced per 1M characters with tier-based discounts.\n  unit: character\n  aggregation: sum\n  dimensions:\n  - account\n  - voice_model\n- name: stt_hours\n  description: Speech-to-Text hour usage at $0.35/hour standard.\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - account\n- name: realtime_minutes\n  description: Realtime API speech-to-speech included with all plans.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n- name: llm_router_tokens\n  description:\
  \ LLM Router pass-through token usage at provider cost.\n  unit: token\n  aggregation: sum\n  dimensions:\n  - account\n  - provider_model\n- name: monthly_credits\n  description: Monthly credit allocation tied to plan tier.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\nprinciples:\n- name: Visibility\n  description: Track credit burn and per-meter usage in Inworld dashboard.\n- name: Allocation\n  description: Tag voices and game/title workloads to attribute usage.\n- name: Optimization\n  description: Move to higher tiers when projected burn unlocks 20-40% rate discounts; choose TTS-1.5 Mini where quality permits.\n- name: Accountability\n  description: Assign a credit budget owner per game/title.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/inworld/refs/heads/main/finops/inworld-finops.yml
sources:
- https://inworld.ai/pricing
- https://docs.inworld.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- Characters
- Games
- Conversational
- FinOps
- Cost Management
- FOCUS
---
