---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openai-chat-completions-openapi.yml
  format: yaml
  label: OpenAI Chat Completions API
  slug: openai-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-chat-completions-openapi.yml
- filename: openai-completions-openapi.yml
  format: yaml
  label: OpenAI Completions API
  slug: openai-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-completions-openapi.yml
- filename: openai-images-openapi.yml
  format: yaml
  label: OpenAI Images API
  slug: openai-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-images-openapi.yml
- filename: openai-embeddings-openapi.yml
  format: yaml
  label: OpenAI Embeddings API
  slug: openai-embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-embeddings-openapi.yml
- filename: openai-audio-openapi.yml
  format: yaml
  label: OpenAI Audio API
  slug: openai-audio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-audio-openapi.yml
- filename: openai-moderations-openapi.yml
  format: yaml
  label: OpenAI Moderations API
  slug: openai-moderations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-moderations-openapi.yml
- filename: openai-assistants-openapi.yml
  format: yaml
  label: OpenAI Assistants API
  slug: openai-assistants-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/openapi/openai-assistants-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Credit
  - Adjustment
  pricingCategory: Token-Based Usage + Committed Throughput
description: 'FOCUS-aligned FinOps for the OpenAI API platform: token-based pay-as-you-go billing across text, image, audio, and video models, with batch and prompt-caching discounts plus optional Provisioned Throughput commitments for enterprise.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenAI, L.L.C.
  PricingUnit: token
  ProviderName: OpenAI
  PublisherName: OpenAI, L.L.C.
  ServiceCategory: AI Infrastructure
  ServiceName: OpenAI API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  - organization
  - project
  - api_key
  - cached
  name: tokens_input
  unit: token
- aggregation: sum
  dimensions:
  - model
  - organization
  - project
  - api_key
  - reasoning
  name: tokens_output
  unit: token
- aggregation: sum
  dimensions:
  - model
  - organization
  name: cached_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  - resolution
  - quality
  name: image_generations
  unit: image
- aggregation: sum
  dimensions:
  - model
  - resolution
  name: video_seconds
  unit: second
- aggregation: sum
  dimensions:
  - model
  - direction
  name: audio_seconds
  unit: second
- aggregation: sum
  dimensions:
  - tool
  name: tool_calls
  unit: call
- aggregation: sum
  dimensions:
  - vector_store
  name: file_storage
  unit: GB-day
- aggregation: sum
  dimensions:
  - model
  name: provisioned_throughput_hours
  unit: PTU-hour
name: Openai Apis Finops
provider_name: OpenAI APIs
provider_slug: openai-apis
publisher_name: OpenAI, L.L.C.
service_category: AI Infrastructure
slug: openai-apis-finops
source_filename: openai-apis-finops.yml
source_heading: FinOps Profile
source_url: https://openai.com/api/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenAI APIs\nproviderId: openai-apis\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Artificial Intelligence\n  - Language Models\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for the OpenAI API platform: token-based pay-as-you-go billing across\n  text, image, audio, and video models, with batch and prompt-caching discounts plus optional Provisioned\n  Throughput commitments for enterprise.'\nsources:\n  - https://openai.com/api/pricing/\n  - https://platform.openai.com/docs/guides/rate-limits\n  - https://platform.openai.com/usage\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenAI, L.L.C.\nserviceCategory: AI\
  \ Infrastructure\nbillingModel:\n  pricingCategory: Token-Based Usage + Committed Throughput\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: OpenAI API\n  ServiceCategory: AI Infrastructure\n  ProviderName: OpenAI\n  PublisherName: OpenAI, L.L.C.\n  InvoiceIssuerName: OpenAI, L.L.C.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: token\nmeters:\n  - name: tokens_input\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - organization\n      - project\n      - api_key\n      - cached\n  - name: tokens_output\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - organization\n      - project\n      - api_key\n      - reasoning\n  - name: cached_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - organization\n  - name: image_generations\n    unit: image\n    aggregation:\
  \ sum\n    dimensions:\n      - model\n      - resolution\n      - quality\n  - name: video_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n      - model\n      - resolution\n  - name: audio_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n      - model\n      - direction\n  - name: tool_calls\n    unit: call\n    aggregation: sum\n    dimensions:\n      - tool\n  - name: file_storage\n    unit: GB-day\n    aggregation: sum\n    dimensions:\n      - vector_store\n  - name: provisioned_throughput_hours\n    unit: PTU-hour\n    aggregation: sum\n    dimensions:\n      - model\nprinciples:\n  - name: Visibility\n    description: Use the Usage dashboard, the /v1/usage endpoint, and project-scoped API keys to attribute\n      tokens and cost per team/feature in near-real-time.\n  - name: Allocation\n    description: Create separate Projects and API keys per workload; tag requests with metadata such as\n      user/feature in your application logs to back-allocate\
  \ spend.\n  - name: Optimization\n    description: Route to the cheapest sufficient model (nano/mini before flagship), enable prompt caching,\n      use the Batch API for non-urgent jobs (50% off), trim system prompts, and prefer structured outputs\n      over chain-of-thought when latency permits.\n  - name: Accountability\n    description: Set hard usage limits and per-project budget alerts in the OpenAI console; assign a model-cost\n      owner who reviews the monthly invoice against forecast and investigates token-cost regressions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openai-apis/refs/heads/main/finops/openai-apis-finops.yml
sources:
- https://openai.com/api/pricing/
- https://platform.openai.com/docs/guides/rate-limits
- https://platform.openai.com/usage
specification: FinOps Framework
tags:
- Artificial Intelligence
- Language Models
- FinOps
- Cost Management
- FOCUS
---
