---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: minimax-ai-openapi.json
  format: json
  label: MiniMax Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/minimax-ai/refs/heads/main/openapi/minimax-ai-openapi.json
billing_model:
  billingCurrency: USD/CNY
  billingFrequency: Monthly / On-Demand
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Mixed (Usage and Subscription)
description: 'FOCUS-aligned FinOps profile for MiniMax. Mixed billing model: PAYG token/character/second metering plus subscription Token Plan, Audio Subscription, and Video Packages.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: MiniMax
  ProviderName: MiniMax
  PublisherName: MiniMax
  ServiceCategory: AI and Machine Learning
  ServiceName: MiniMax Platform
layout: finops
meters:
- aggregation: sum
  description: Input tokens for text models.
  dimensions:
  - model
  - account
  name: text_input_tokens
  unit: tokens
- aggregation: sum
  description: Output tokens for text models.
  dimensions:
  - model
  - account
  name: text_output_tokens
  unit: tokens
- aggregation: sum
  description: Characters synthesized.
  dimensions:
  - voice_model
  - account
  name: speech_characters
  unit: characters
- aggregation: sum
  description: Generated video seconds.
  dimensions:
  - video_model
  - account
  name: video_seconds
  unit: seconds
- aggregation: sum
  description: Images generated.
  dimensions:
  - model
  - account
  name: image_generations
  unit: images
- aggregation: sum
  description: Music tracks generated.
  dimensions:
  - model
  - account
  name: music_generations
  unit: tracks
name: Minimax Ai Finops
provider_name: MiniMax
provider_slug: minimax-ai
publisher_name: MiniMax
service_category: AI and Machine Learning
slug: minimax-ai-finops
source_filename: minimax-ai-finops.yml
source_heading: FinOps Profile
source_url: https://platform.minimax.io/docs/pricing/overview
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: MiniMax\nproviderId: minimax-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Multimodal\n- FinOps\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for MiniMax. Mixed billing model: PAYG token/character/second\n  metering plus subscription Token Plan, Audio Subscription, and Video Packages.\nnotes: >-\n  Multi-modality means meter dimensions span tokens, characters, seconds, and image counts.\n  Subscription products map to FOCUS Purchase; consumption maps to Usage.\nsources:\n- https://platform.minimax.io/docs/pricing/overview\n- https://platform.minimax.io/docs/guides/rate-limits\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: MiniMax\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Mixed (Usage and Subscription)\n  billingFrequency: Monthly / On-Demand\n  billingCurrency: USD/CNY\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: MiniMax Platform\n  ServiceCategory: AI and Machine Learning\n  ProviderName: MiniMax\n  PublisherName: MiniMax\n  InvoiceIssuerName: MiniMax\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: text_input_tokens\n  description: Input tokens for text models.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: text_output_tokens\n  description: Output tokens for text models.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: speech_characters\n  description: Characters synthesized.\n  unit: characters\n  aggregation: sum\n  dimensions: [voice_model, account]\n- name: video_seconds\n  description: Generated video seconds.\n  unit: seconds\n\
  \  aggregation: sum\n  dimensions: [video_model, account]\n- name: image_generations\n  description: Images generated.\n  unit: images\n  aggregation: sum\n  dimensions: [model, account]\n- name: music_generations\n  description: Music tracks generated.\n  unit: tracks\n  aggregation: sum\n  dimensions: [model, account]\nprinciples:\n- name: Visibility\n  description: Console exports usage by modality; balance API tracks prepaid spend.\n- name: Allocation\n  description: Tag API keys to attribute multi-modal spend across teams.\n- name: Optimization\n  description: Use highspeed variants for latency-sensitive paths; switch to Token Plan if monthly token spend stabilizes.\n- name: Accountability\n  description: Subscription products require renewal review; PAYG requires balance alerting.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/minimax-ai/refs/heads/main/finops/minimax-ai-finops.yml
sources:
- https://platform.minimax.io/docs/pricing/overview
- https://platform.minimax.io/docs/guides/rate-limits
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Multimodal
- FinOps
- FOCUS
---
