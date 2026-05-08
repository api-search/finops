---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: CNY
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage Based
description: FOCUS-aligned FinOps profile for ByteDance Doubao via Volcano Engine Ark. Pay-as-you-go per-token / per-call billing aggregated to the Volcano Engine cloud invoice. Reserved capacity available for predictable workloads.
focus_columns:
  BillingCurrency: CNY
  ChargeCategory: Usage
  InvoiceIssuerName: Volcano Engine
  ProviderName: Volcano Engine
  PublisherName: Volcano Engine
  ServiceCategory: AI and Machine Learning
  ServiceName: Volcano Engine Ark (Doubao)
layout: finops
meters:
- aggregation: sum
  description: Input tokens by Doubao variant.
  dimensions:
  - model
  - endpoint
  - account
  name: input_tokens
  unit: tokens
- aggregation: sum
  description: Output tokens by Doubao variant.
  dimensions:
  - model
  - endpoint
  - account
  name: output_tokens
  unit: tokens
- aggregation: sum
  description: Seedream image generation calls.
  dimensions:
  - model
  - account
  name: image_generations
  unit: images
- aggregation: sum
  description: Seedance video seconds.
  dimensions:
  - model
  - account
  name: video_seconds
  unit: seconds
- aggregation: sum
  description: TTS characters synthesized.
  dimensions:
  - voice
  - account
  name: tts_characters
  unit: characters
- aggregation: sum
  description: Embedding tokens.
  dimensions:
  - model
  - account
  name: embedding_tokens
  unit: tokens
name: Doubao Finops
provider_name: ByteDance Doubao
provider_slug: doubao
publisher_name: Volcano Engine (ByteDance)
service_category: AI and Machine Learning
slug: doubao-finops
source_filename: doubao-finops.yml
source_heading: FinOps Profile
source_url: https://www.volcengine.com/docs/82379
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ByteDance Doubao\nproviderId: doubao\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- ByteDance\n- FinOps\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for ByteDance Doubao via Volcano Engine Ark. Pay-as-you-go\n  per-token / per-call billing aggregated to the Volcano Engine cloud invoice. Reserved\n  capacity available for predictable workloads.\nnotes: Pricing primarily in CNY; verify FX exposure when consolidating to USD reporting.\nsources:\n- https://www.volcengine.com/docs/82379\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Volcano Engine (ByteDance)\nserviceCategory:\
  \ AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage Based\n  billingFrequency: Monthly\n  billingCurrency: CNY\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Volcano Engine Ark (Doubao)\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Volcano Engine\n  PublisherName: Volcano Engine\n  InvoiceIssuerName: Volcano Engine\n  BillingCurrency: CNY\n  ChargeCategory: Usage\nmeters:\n- name: input_tokens\n  description: Input tokens by Doubao variant.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, endpoint, account]\n- name: output_tokens\n  description: Output tokens by Doubao variant.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, endpoint, account]\n- name: image_generations\n  description: Seedream image generation calls.\n  unit: images\n  aggregation: sum\n  dimensions: [model, account]\n- name: video_seconds\n  description: Seedance video seconds.\n  unit: seconds\n  aggregation: sum\n  dimensions:\
  \ [model, account]\n- name: tts_characters\n  description: TTS characters synthesized.\n  unit: characters\n  aggregation: sum\n  dimensions: [voice, account]\n- name: embedding_tokens\n  description: Embedding tokens.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\nprinciples:\n- name: Visibility\n  description: Volcano Engine billing console exports usage by endpoint and model.\n- name: Allocation\n  description: Tag endpoints and use account hierarchy to attribute spend.\n- name: Optimization\n  description: Use Doubao-Lite for cheap paths, reserved instances for predictable load.\n- name: Accountability\n  description: Reserved-instance renewals and rate-card reviews via Volcano Engine sales.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/doubao/refs/heads/main/finops/doubao-finops.yml
sources:
- https://www.volcengine.com/docs/82379
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- ByteDance
- FinOps
- FOCUS
---
