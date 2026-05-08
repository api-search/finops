---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: groq-openapi.yml
  format: yaml
  label: Groq Chat Completions API
  slug: groq-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Reasoning API
  slug: groq-reasoning-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Vision API
  slug: groq-vision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Speech-to-Text API
  slug: groq-speech-to-text-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Text-to-Speech API
  slug: groq-text-to-speech-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Content Moderation API
  slug: groq-content-moderation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Batch API
  slug: groq-batch-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Flex Processing API
  slug: groq-flex-processing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Files API
  slug: groq-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Models API
  slug: groq-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Tools API
  slug: groq-tools-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq LoRA Inference API
  slug: groq-lora-inference-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
- filename: groq-openapi.yml
  format: yaml
  label: Groq Prompt Caching
  slug: groq-prompt-caching-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/openapi/groq-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based
description: FinOps view of GroqCloud spend. Groq bills usage-based per-token rates for chat / vision / reasoning per model, per-million-character rates for TTS, per-hour transcription rates for STT, per-call or per-hour rates for tools, and a 50% Batch discount. Prompt Caching gives 50% off cached input tokens.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Groq
  PricingCategory: Usage-Based
  ProviderName: Groq
  PublisherName: Groq
  ServiceCategory: AI and Machine Learning
  ServiceName: GroqCloud
layout: finops
meters:
- aggregation: sum
  description: Tokens sent in chat / vision / reasoning requests, billed per 1M tokens per model.
  dimensions:
  - account
  - model
  - api
  name: input_tokens
  unit: tokens
- aggregation: sum
  description: Cached-input tokens billed at 50% of the standard input rate.
  dimensions:
  - account
  - model
  name: cached_input_tokens
  unit: tokens
- aggregation: sum
  description: Tokens generated, billed per 1M tokens per model.
  dimensions:
  - account
  - model
  - api
  name: output_tokens
  unit: tokens
- aggregation: sum
  description: TTS characters synthesized, billed per 1M characters per voice/model.
  dimensions:
  - account
  - model
  name: tts_characters
  unit: characters
- aggregation: sum
  description: Audio hours transcribed, billed per hour per Whisper variant.
  dimensions:
  - account
  - model
  name: stt_audio_hours
  unit: hours
- aggregation: sum
  description: Tool calls (web search, Wolfram) priced per 1,000 invocations.
  dimensions:
  - account
  - tool
  name: tool_invocations
  unit: invocations
- aggregation: sum
  description: Tool compute hours (e.g., Code Execution at $0.18/hr).
  dimensions:
  - account
  - tool
  name: tool_compute_hours
  unit: hours
- aggregation: sum
  description: Tokens consumed via the Batch API at 50% discount.
  dimensions:
  - account
  - model
  name: batch_tokens
  unit: tokens
- aggregation: sum
  description: Tokens consumed via Flex Processing tier at relaxed-latency discount.
  dimensions:
  - account
  - model
  name: flex_tokens
  unit: tokens
name: Groq Finops
provider_name: Groq
provider_slug: groq
publisher_name: Groq
service_category: AI and Machine Learning
slug: groq-finops
source_filename: groq-finops.yml
source_heading: FinOps Profile
source_url: https://groq.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Groq\nproviderId: groq\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Inference\n- LPU\n- Low Latency\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of GroqCloud spend. Groq bills usage-based per-token rates for\n  chat / vision / reasoning per model, per-million-character rates for TTS,\n  per-hour transcription rates for STT, per-call or per-hour rates for tools,\n  and a 50% Batch discount. Prompt Caching gives 50% off cached input tokens.\nnotes: >-\n  Per-model rates are subject to change; verify against the Groq pricing page\n  during reconciliation.\nsources:\n- https://groq.com/pricing\n- https://console.groq.com/docs\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Groq\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: GroqCloud\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Groq\n  PublisherName: Groq\n  InvoiceIssuerName: Groq\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Usage-Based\nmeters:\n- name: input_tokens\n  description: Tokens sent in chat / vision / reasoning requests, billed per 1M tokens per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n  - api\n- name: cached_input_tokens\n  description: Cached-input tokens billed at 50% of the standard input rate.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: output_tokens\n  description: Tokens generated,\
  \ billed per 1M tokens per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n  - api\n- name: tts_characters\n  description: TTS characters synthesized, billed per 1M characters per voice/model.\n  unit: characters\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: stt_audio_hours\n  description: Audio hours transcribed, billed per hour per Whisper variant.\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: tool_invocations\n  description: Tool calls (web search, Wolfram) priced per 1,000 invocations.\n  unit: invocations\n  aggregation: sum\n  dimensions:\n  - account\n  - tool\n- name: tool_compute_hours\n  description: Tool compute hours (e.g., Code Execution at $0.18/hr).\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - account\n  - tool\n- name: batch_tokens\n  description: Tokens consumed via the Batch API at 50% discount.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n\
  - name: flex_tokens\n  description: Tokens consumed via Flex Processing tier at relaxed-latency discount.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\nprinciples:\n- name: Visibility\n  description: Pull GroqCloud usage and billing exports; inspect per-model token burn.\n- name: Allocation\n  description: Tag API keys per workload/team; map to internal cost centers.\n- name: Optimization\n  description: Use Batch (-50%) for non-realtime jobs; enable Prompt Caching; route lower-quality work to Flex; pick smaller open-source models when sufficient.\n- name: Accountability\n  description: Assign owners per project/key; review token spend monthly against budget.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/finops/groq-finops.yml
sources:
- https://groq.com/pricing
- https://console.groq.com/docs
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Inference
- LPU
- Low Latency
- FinOps
- Cost Management
- FOCUS
---
