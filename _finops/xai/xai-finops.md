---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: xai-openapi.json
  format: json
  label: xAI Chat Completions API
  slug: xai-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Responses API
  slug: xai-responses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Images API
  slug: xai-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Video Generation API
  slug: xai-video-generation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Voice API
  slug: xai-voice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Embeddings API
  slug: xai-embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Models API
  slug: xai-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
- filename: xai-openapi.json
  format: json
  label: xAI Batch API
  slug: xai-batch-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/openapi/xai-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage-Based
description: FinOps view of xAI API spend. Billing is usage-based, charged per token (input/output, with cached-input discounts) per model, plus per-call fees for built-in tools and a Batch API tier offering 20-50% discounts. Spend is reported on the team-level invoice in USD.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: xAI
  PricingCategory: Usage-Based
  ProviderName: xAI
  PublisherName: xAI
  ServiceCategory: AI and Machine Learning
  ServiceName: xAI API
layout: finops
meters:
- aggregation: sum
  description: Tokens sent in the request (prompt) per model.
  dimensions:
  - team
  - model
  - api
  name: input_tokens
  unit: tokens
- aggregation: sum
  description: Cached-input tokens billed at a reduced rate when prompt caching applies.
  dimensions:
  - team
  - model
  name: cached_input_tokens
  unit: tokens
- aggregation: sum
  description: Tokens generated in the model response per model.
  dimensions:
  - team
  - model
  - api
  name: output_tokens
  unit: tokens
- aggregation: sum
  description: Calls to built-in tools (e.g., Live Search) priced per 1,000 invocations.
  dimensions:
  - team
  - tool
  name: tool_invocations
  unit: invocations
- aggregation: sum
  description: Tokens consumed via the Batch API at 20-50% discount.
  dimensions:
  - team
  - model
  name: batch_tokens
  unit: tokens
- aggregation: sum
  description: Image generation requests (per image / per resolution tier).
  dimensions:
  - team
  - model
  name: image_generations
  unit: images
- aggregation: sum
  description: Video generation requests (per video / per duration tier).
  dimensions:
  - team
  - model
  name: video_generations
  unit: videos
name: Xai Finops
provider_name: xAI
provider_slug: xai
publisher_name: xAI
service_category: AI and Machine Learning
slug: xai-finops
source_filename: xai-finops.yml
source_heading: FinOps Profile
source_url: https://x.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: xAI\nproviderId: xai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Foundation Models\n- Grok\n- Generative AI\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of xAI API spend. Billing is usage-based, charged per token\n  (input/output, with cached-input discounts) per model, plus per-call fees for\n  built-in tools and a Batch API tier offering 20-50% discounts. Spend is\n  reported on the team-level invoice in USD.\nnotes: >-\n  Per-model token rates are subject to change; verify current rates against the\n  xAI Console Models page when reconciling.\nsources:\n- https://x.ai/\n- https://docs.x.ai/docs/models\n- https://console.x.ai/team/default/models\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: xAI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: xAI API\n  ServiceCategory: AI and Machine Learning\n  ProviderName: xAI\n  PublisherName: xAI\n  InvoiceIssuerName: xAI\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingCategory: Usage-Based\nmeters:\n- name: input_tokens\n  description: Tokens sent in the request (prompt) per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n  - api\n- name: cached_input_tokens\n  description: Cached-input tokens billed at a reduced rate when prompt caching applies.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n- name: output_tokens\n  description: Tokens generated in the model\
  \ response per model.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n  - api\n- name: tool_invocations\n  description: Calls to built-in tools (e.g., Live Search) priced per 1,000 invocations.\n  unit: invocations\n  aggregation: sum\n  dimensions:\n  - team\n  - tool\n- name: batch_tokens\n  description: Tokens consumed via the Batch API at 20-50% discount.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n- name: image_generations\n  description: Image generation requests (per image / per resolution tier).\n  unit: images\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n- name: video_generations\n  description: Video generation requests (per video / per duration tier).\n  unit: videos\n  aggregation: sum\n  dimensions:\n  - team\n  - model\nprinciples:\n- name: Visibility\n  description: Pull team-level usage from the xAI Console and join with invoice exports.\n- name: Allocation\n  description: Tag API keys per workload/team and\
  \ map back to internal cost centers.\n- name: Optimization\n  description: Route non-realtime workloads through the Batch API for 20-50% savings; use cached-input tokens where prompts are reused.\n- name: Accountability\n  description: Assign owners per team and per API key; review monthly token burn vs. budget.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/xai/refs/heads/main/finops/xai-finops.yml
sources:
- https://x.ai/
- https://docs.x.ai/docs/models
- https://console.x.ai/team/default/models
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Foundation Models
- Grok
- Generative AI
- FinOps
- Cost Management
- FOCUS
---
