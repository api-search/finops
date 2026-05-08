---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: murf-openapi.yml
  format: yaml
  label: Murf API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/murf/refs/heads/main/openapi/murf-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based (Per Minute / Per Endpoint)
description: FOCUS-aligned FinOps view of Murf. Falcon TTS streams at a flat $0.01/min with no tiered confusion. Other endpoints (Gen 2 TTS, Dubbing, Voice Changer, Translation) priced per the API pricing page. Murf positions itself as up to 50% cheaper than competitor stacks.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Murf
  ProviderName: Murf
  PublisherName: Murf
  ServiceCategory: AI
  ServiceName: Murf API
layout: finops
meters:
- aggregation: sum
  description: Falcon TTS streaming minutes at $0.01/min flat.
  dimensions:
  - account
  - region
  name: falcon_tts_minutes
  unit: minute
- aggregation: sum
  description: Gen 2 TTS studio synthesis usage.
  dimensions:
  - account
  - voice
  name: gen2_tts_usage
  unit: minute
- aggregation: sum
  description: Dubbing API minutes processed.
  dimensions:
  - account
  - target_language
  name: dubbing_minutes
  unit: minute
- aggregation: sum
  description: Voice Changer API minutes processed.
  dimensions:
  - account
  name: voice_changer_minutes
  unit: minute
- aggregation: sum
  description: Translation API usage.
  dimensions:
  - account
  - target_language
  name: translation_units
  unit: word
name: Murf Finops
provider_name: Murf
provider_slug: murf
publisher_name: Murf
service_category: AI
slug: murf-finops
source_filename: murf-finops.yml
source_heading: FinOps Profile
source_url: https://murf.ai/api
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Murf\nproviderId: murf\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- TTS\n- Voiceover\n- Audio\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Murf. Falcon TTS streams at a flat $0.01/min with no tiered\n  confusion. Other endpoints (Gen 2 TTS, Dubbing, Voice Changer, Translation) priced per the\n  API pricing page. Murf positions itself as up to 50% cheaper than competitor stacks.\nnotes: Falcon flat rate makes per-minute budgeting trivial; other endpoints require per-product cost tracking.\nsources:\n- https://murf.ai/api\n- https://murf.ai/api/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Murf\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage-Based (Per Minute / Per Endpoint)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Murf API\n  ServiceCategory: AI\n  ProviderName: Murf\n  PublisherName: Murf\n  InvoiceIssuerName: Murf\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: falcon_tts_minutes\n  description: Falcon TTS streaming minutes at $0.01/min flat.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - region\n- name: gen2_tts_usage\n  description: Gen 2 TTS studio synthesis usage.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - voice\n- name: dubbing_minutes\n  description: Dubbing API minutes processed.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - target_language\n- name: voice_changer_minutes\n  description: Voice Changer API minutes processed.\n  unit: minute\n\
  \  aggregation: sum\n  dimensions:\n  - account\n- name: translation_units\n  description: Translation API usage.\n  unit: word\n  aggregation: sum\n  dimensions:\n  - account\n  - target_language\nprinciples:\n- name: Visibility\n  description: Track per-endpoint usage in Murf API dashboard.\n- name: Allocation\n  description: Tag voices and integrations per consuming product.\n- name: Optimization\n  description: Falcon flat rate suits high-volume voice agents; reserve Gen 2 for studio quality where needed.\n- name: Accountability\n  description: Assign owners per product (TTS, Dubbing, Voice Changer, Translation).\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/murf/refs/heads/main/finops/murf-finops.yml
sources:
- https://murf.ai/api
- https://murf.ai/api/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- TTS
- Voiceover
- Audio
- FinOps
- Cost Management
- FOCUS
---
