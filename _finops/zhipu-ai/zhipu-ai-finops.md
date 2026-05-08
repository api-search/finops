---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: zhipu-ai-openapi.json
  format: json
  label: Z.ai Open Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zhipu-ai/refs/heads/main/openapi/zhipu-ai-openapi.json
billing_model:
  billingCurrency: USD/CNY
  billingFrequency: On-Demand (Recharge) / Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Mixed (Usage and Subscription)
description: 'FOCUS-aligned FinOps profile for Z.ai / Zhipu AI. Two commercial paths: prepaid API balance consumed against per-million-token rates per model, plus GLM Coding Plan subscription with capped usage windows.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Zhipu AI
  ProviderName: Zhipu AI
  PublisherName: Zhipu AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Z.ai Open Platform
layout: finops
meters:
- aggregation: sum
  description: Input tokens by model.
  dimensions:
  - model
  - account
  name: input_tokens
  unit: tokens
- aggregation: sum
  description: Cached input tokens (currently free).
  dimensions:
  - model
  - account
  name: cached_input_tokens
  unit: tokens
- aggregation: sum
  description: Output tokens by model.
  dimensions:
  - model
  - account
  name: output_tokens
  unit: tokens
- aggregation: sum
  description: Images generated.
  dimensions:
  - model
  - account
  name: image_generations
  unit: images
- aggregation: sum
  description: Videos generated.
  dimensions:
  - model
  - account
  name: video_generations
  unit: videos
- aggregation: sum
  description: Web search tool invocations.
  dimensions:
  - account
  name: web_search_calls
  unit: calls
- aggregation: sum
  description: Audio transcription tokens.
  dimensions:
  - model
  - account
  name: audio_transcription_tokens
  unit: tokens
- aggregation: sum
  description: Agent service tokens.
  dimensions:
  - agent
  - account
  name: agent_tokens
  unit: tokens
name: Zhipu Ai Finops
provider_name: Zhipu AI
provider_slug: zhipu-ai
publisher_name: Zhipu AI
service_category: AI and Machine Learning
slug: zhipu-ai-finops
source_filename: zhipu-ai-finops.yml
source_heading: FinOps Profile
source_url: https://docs.z.ai/guides/overview/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Zhipu AI\nproviderId: zhipu-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- GLM\n- FinOps\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Z.ai / Zhipu AI. Two commercial paths: prepaid API balance\n  consumed against per-million-token rates per model, plus GLM Coding Plan subscription with\n  capped usage windows.\nnotes: >-\n  Cached input storage is currently free (limited-time). Plan deductions are weighted by\n  peak/off-peak windows for some models.\nsources:\n- https://docs.z.ai/guides/overview/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Zhipu AI\nserviceCategory:\
  \ AI and Machine Learning\nbillingModel:\n  pricingCategory: Mixed (Usage and Subscription)\n  billingFrequency: On-Demand (Recharge) / Monthly\n  billingCurrency: USD/CNY\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Z.ai Open Platform\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Zhipu AI\n  PublisherName: Zhipu AI\n  InvoiceIssuerName: Zhipu AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: input_tokens\n  description: Input tokens by model.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: cached_input_tokens\n  description: Cached input tokens (currently free).\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: output_tokens\n  description: Output tokens by model.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: image_generations\n  description: Images generated.\n  unit: images\n  aggregation: sum\n  dimensions: [model,\
  \ account]\n- name: video_generations\n  description: Videos generated.\n  unit: videos\n  aggregation: sum\n  dimensions: [model, account]\n- name: web_search_calls\n  description: Web search tool invocations.\n  unit: calls\n  aggregation: sum\n  dimensions: [account]\n- name: audio_transcription_tokens\n  description: Audio transcription tokens.\n  unit: tokens\n  aggregation: sum\n  dimensions: [model, account]\n- name: agent_tokens\n  description: Agent service tokens.\n  unit: tokens\n  aggregation: sum\n  dimensions: [agent, account]\nprinciples:\n- name: Visibility\n  description: Console reports balance and consumption per model; coding plan dashboards show window utilization.\n- name: Allocation\n  description: Tag API keys per workload; coding-plan seats per developer.\n- name: Optimization\n  description: Use Flash variants (free or near-free) for non-critical paths; off-peak windows reduce coding-plan deductions.\n- name: Accountability\n  description: Track GLM Coding Plan\
  \ window utilization; renew or right-size at billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zhipu-ai/refs/heads/main/finops/zhipu-ai-finops.yml
sources:
- https://docs.z.ai/guides/overview/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- GLM
- FinOps
- FOCUS
---
