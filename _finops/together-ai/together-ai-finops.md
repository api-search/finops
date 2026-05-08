---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Chat Completions API
  slug: together-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Completions API
  slug: together-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Embeddings API
  slug: together-embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Rerank API
  slug: together-rerank-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Images API
  slug: together-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Video API
  slug: together-video-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Audio API
  slug: together-audio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Vision API
  slug: together-vision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Fine-Tuning API
  slug: together-fine-tuning-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Files API
  slug: together-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Models API
  slug: together-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Batch API
  slug: together-batch-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Code Interpreter API
  slug: together-code-interpreter-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Evaluations API
  slug: together-evaluations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
- filename: together-ai-openapi.yml
  format: yaml
  label: Together Dedicated Endpoints API
  slug: together-dedicated-endpoints-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/openapi/together-ai-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based
description: FinOps view of Together AI spend. Together bills usage-based per-token rates for serverless inference (chat, embeddings, rerank, vision, audio), per-asset rates for image and video, per-1M-character rates for audio, per-token rates for fine-tuning training, and hourly rates for dedicated endpoints and GPU clusters (with reserved discounts).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Together AI
  PricingCategory: Usage-Based
  ProviderName: Together AI
  PublisherName: Together AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Together AI Cloud
layout: finops
meters:
- aggregation: sum
  description: Tokens sent in chat / completion requests, billed per 1M tokens per model.
  dimensions:
  - account
  - model
  - api
  name: input_tokens
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
  description: Tokens processed for embeddings, billed per 1M tokens per model.
  dimensions:
  - account
  - model
  name: embedding_tokens
  unit: tokens
- aggregation: sum
  description: Documents reranked, billed per 1K or per 1M units depending on model.
  dimensions:
  - account
  - model
  name: rerank_documents
  unit: documents
- aggregation: sum
  description: Image generation requests, billed per image per model/quality tier.
  dimensions:
  - account
  - model
  name: image_generations
  unit: images
- aggregation: sum
  description: Video generation requests, billed per video per model/quality tier.
  dimensions:
  - account
  - model
  name: video_generations
  unit: videos
- aggregation: sum
  description: TTS / STT character counts, billed per 1M characters per model.
  dimensions:
  - account
  - model
  name: audio_characters
  unit: characters
- aggregation: sum
  description: Training tokens for fine-tuning jobs, billed per 1M tokens per base-model size class.
  dimensions:
  - account
  - base_model
  - method
  name: fine_tuning_tokens
  unit: tokens
- aggregation: sum
  description: Wall-clock hours of dedicated inference endpoint runtime per GPU class.
  dimensions:
  - account
  - endpoint
  - gpu_class
  name: dedicated_endpoint_hours
  unit: hours
- aggregation: sum
  description: Wall-clock hours of bare-metal GPU cluster runtime per GPU class and reservation tier.
  dimensions:
  - account
  - cluster
  - gpu_class
  - reservation_tier
  name: gpu_cluster_hours
  unit: hours
- aggregation: sum
  description: Tokens consumed via the Batch API at up to 50% discount versus serverless.
  dimensions:
  - account
  - model
  name: batch_tokens
  unit: tokens
name: Together Ai Finops
provider_name: Together AI
provider_slug: together-ai
publisher_name: Together AI
service_category: AI and Machine Learning
slug: together-ai-finops
source_filename: together-ai-finops.yml
source_heading: FinOps Profile
source_url: https://www.together.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Together AI\nproviderId: together-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Inference\n- Open Source\n- Fine-tuning\n- GPU\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of Together AI spend. Together bills usage-based per-token rates\n  for serverless inference (chat, embeddings, rerank, vision, audio), per-asset\n  rates for image and video, per-1M-character rates for audio, per-token rates\n  for fine-tuning training, and hourly rates for dedicated endpoints and GPU\n  clusters (with reserved discounts).\nnotes: >-\n  Per-model rates change frequently; verify against the Together pricing page at\n  reconciliation. Batch API consistently offers up to 50% off serverless rates.\nsources:\n- https://www.together.ai/pricing\n- https://docs.together.ai/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Together AI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Together AI Cloud\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Together AI\n  PublisherName: Together AI\n  InvoiceIssuerName: Together AI\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Usage-Based\nmeters:\n- name: input_tokens\n  description: Tokens sent in chat / completion requests, billed per 1M tokens per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n  - api\n- name: output_tokens\n  description: Tokens generated, billed per 1M tokens\
  \ per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n  - api\n- name: embedding_tokens\n  description: Tokens processed for embeddings, billed per 1M tokens per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: rerank_documents\n  description: Documents reranked, billed per 1K or per 1M units depending on model.\n  unit: documents\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: image_generations\n  description: Image generation requests, billed per image per model/quality tier.\n  unit: images\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: video_generations\n  description: Video generation requests, billed per video per model/quality tier.\n  unit: videos\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n- name: audio_characters\n  description: TTS / STT character counts, billed per 1M characters per model.\n  unit: characters\n  aggregation: sum\n  dimensions:\n\
  \  - account\n  - model\n- name: fine_tuning_tokens\n  description: Training tokens for fine-tuning jobs, billed per 1M tokens per base-model size class.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - base_model\n  - method\n- name: dedicated_endpoint_hours\n  description: Wall-clock hours of dedicated inference endpoint runtime per GPU class.\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - account\n  - endpoint\n  - gpu_class\n- name: gpu_cluster_hours\n  description: Wall-clock hours of bare-metal GPU cluster runtime per GPU class and reservation tier.\n  unit: hours\n  aggregation: sum\n  dimensions:\n  - account\n  - cluster\n  - gpu_class\n  - reservation_tier\n- name: batch_tokens\n  description: Tokens consumed via the Batch API at up to 50% discount versus serverless.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - account\n  - model\nprinciples:\n- name: Visibility\n  description: Pull token / asset / hour usage from the Together console; export\
  \ invoices monthly.\n- name: Allocation\n  description: Tag API keys per workload/team and join usage to internal cost centers.\n- name: Optimization\n  description: Move non-realtime workloads to Batch (-50%); pick smaller open-source models when quality permits; reserve GPU clusters for steady-state workloads.\n- name: Accountability\n  description: Assign owners per endpoint, fine-tuning job, and GPU cluster reservation.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/finops/together-ai-finops.yml
sources:
- https://www.together.ai/pricing
- https://docs.together.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Inference
- Open Source
- Fine-tuning
- GPU
- FinOps
- Cost Management
- FOCUS
---
