---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hume-ai-voices-openapi.yml
  format: yaml
  label: Hume Voices API
  slug: voices
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hume-ai/refs/heads/main/openapi/hume-ai-voices-openapi.yml
- filename: hume-ai-tts-openapi.yml
  format: yaml
  label: Hume Octave Text-to-Speech API
  slug: tts
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hume-ai/refs/heads/main/openapi/hume-ai-tts-openapi.yml
- filename: hume-ai-evi-openapi.yml
  format: yaml
  label: Hume Empathic Voice Interface (EVI) API
  slug: evi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hume-ai/refs/heads/main/openapi/hume-ai-evi-openapi.yml
- filename: hume-ai-expression-openapi.yml
  format: yaml
  label: Hume Expression Measurement API
  slug: expression
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hume-ai/refs/heads/main/openapi/hume-ai-expression-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps view of Hume AI. Hume bills via subscription plan tiers (with bundled TTS characters and EVI minutes) plus per-character TTS overage and per-minute EVI overage. Expression Measurement is fully pay-as-you-go priced per minute, image, or word.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hume AI
  ProviderName: Hume AI
  PublisherName: Hume AI
  ServiceCategory: AI
  ServiceName: Hume AI Voice and Expression Measurement
layout: finops
meters:
- aggregation: sum
  description: Monthly TTS character allowance with overage at $0.05-0.15 per 1,000.
  dimensions:
  - account
  - voice
  name: tts_characters
  unit: character
- aggregation: sum
  description: EVI speech-to-speech monthly minute allowance with overage at $0.04-0.06/min.
  dimensions:
  - account
  - chat_group
  name: evi_minutes
  unit: minute
- aggregation: sum
  description: Video-with-audio expression measurement at $0.0828/min.
  dimensions:
  - account
  - job
  name: expression_video_minutes
  unit: minute
- aggregation: sum
  description: Audio-only expression measurement at $0.0639/min.
  dimensions:
  - account
  - job
  name: expression_audio_minutes
  unit: minute
- aggregation: sum
  description: Image expression measurement at $0.00204 each.
  dimensions:
  - account
  - job
  name: expression_images
  unit: image
- aggregation: sum
  description: Text expression measurement at $0.00024/word.
  dimensions:
  - account
  - job
  name: expression_words
  unit: word
name: Hume Ai Finops
provider_name: Hume AI
provider_slug: hume-ai
publisher_name: Hume AI
service_category: AI
slug: hume-ai-finops
source_filename: hume-ai-finops.yml
source_heading: FinOps Profile
source_url: https://www.hume.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hume AI\nproviderId: hume-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Voice\n- Empathic\n- Emotion\n- Multimodal\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Hume AI. Hume bills via subscription plan tiers (with bundled\n  TTS characters and EVI minutes) plus per-character TTS overage and per-minute EVI overage.\n  Expression Measurement is fully pay-as-you-go priced per minute, image, or word.\nnotes: Plan-tier sizing is the dominant FinOps decision; right-size based on monthly TTS character + EVI minute projections.\nsources:\n- https://www.hume.ai/pricing\n- https://dev.hume.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hume AI\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Hume AI Voice and Expression Measurement\n  ServiceCategory: AI\n  ProviderName: Hume AI\n  PublisherName: Hume AI\n  InvoiceIssuerName: Hume AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: tts_characters\n  description: Monthly TTS character allowance with overage at $0.05-0.15 per 1,000.\n  unit: character\n  aggregation: sum\n  dimensions:\n  - account\n  - voice\n- name: evi_minutes\n  description: EVI speech-to-speech monthly minute allowance with overage at $0.04-0.06/min.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - chat_group\n- name: expression_video_minutes\n  description: Video-with-audio expression measurement at $0.0828/min.\n\
  \  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - job\n- name: expression_audio_minutes\n  description: Audio-only expression measurement at $0.0639/min.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - account\n  - job\n- name: expression_images\n  description: Image expression measurement at $0.00204 each.\n  unit: image\n  aggregation: sum\n  dimensions:\n  - account\n  - job\n- name: expression_words\n  description: Text expression measurement at $0.00024/word.\n  unit: word\n  aggregation: sum\n  dimensions:\n  - account\n  - job\nprinciples:\n- name: Visibility\n  description: Use Hume billing dashboard to track TTS characters, EVI minutes, and Expression Measurement usage by job.\n- name: Allocation\n  description: Tag voices, EVI configs, and Expression Measurement jobs to business units.\n- name: Optimization\n  description: Right-size plan tier; for Expression Measurement, batch larger jobs and prefer audio-only over video where possible.\n- name: Accountability\n\
  \  description: Assign owners for TTS, EVI, and Expression Measurement budget lines separately.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hume-ai/refs/heads/main/finops/hume-ai-finops.yml
sources:
- https://www.hume.ai/pricing
- https://dev.hume.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Voice
- Empathic
- Emotion
- Multimodal
- FinOps
- Cost Management
- FOCUS
---
