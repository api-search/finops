---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: assistants-openapi-original.yml
  format: yaml
  label: OpenAI Assistants API
  slug: openai-assistants-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/assistants-openapi-original.yml
- filename: audio-openapi-original.yml
  format: yaml
  label: OpenAI Audio API
  slug: openai-audio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/audio-openapi-original.yml
- filename: chat-openapi-original.yml
  format: yaml
  label: OpenAI Chat API
  slug: openai-chat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/chat-openapi-original.yml
- filename: openai-chat-completions-openapi.yml
  format: yaml
  label: OpenAI Chat Completions API
  slug: openai-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/openai-chat-completions-openapi.yml
- filename: embeddings-openapi-original.yml
  format: yaml
  label: OpenAI Embeddings API
  slug: openai-embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/embeddings-openapi-original.yml
- filename: files-openapi-original.yml
  format: yaml
  label: OpenAI Files API
  slug: openai-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/files-openapi-original.yml
- filename: fine-tuning-openapi-original.yml
  format: yaml
  label: OpenAI Fine Tuning API
  slug: openai-fine-tuning-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/fine-tuning-openapi-original.yml
- filename: images-openapi-original.yml
  format: yaml
  label: OpenAI Images API
  slug: openai-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/images-openapi-original.yml
- filename: models-openapi-original.yml
  format: yaml
  label: OpenAI Models API
  slug: openai-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/models-openapi-original.yml
- filename: threads-openapi-original.yml
  format: yaml
  label: OpenAI Threads API
  slug: openai-threads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/threads-openapi-original.yml
- filename: completions-openapi-original.yml
  format: yaml
  label: OpenAI Completions API
  slug: openai-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/openapi/completions-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Usage-Based
  primaryUnit: token
description: 'FOCUS-aligned FinOps for OpenAI: token-based metering across model tiers with batch and cached-input lanes.'
focus_columns:
  PricingUnit: MTok
  ProviderName: OpenAI
  PublisherName: OpenAI
  ServiceCategory: AI and Machine Learning
  ServiceName: OpenAI API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  - project
  - user
  - cached
  name: input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  - project
  - user
  name: output_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  name: cached_input_tokens
  unit: token
- aggregation: sum
  name: image_generations
  unit: image
- aggregation: sum
  name: audio_minutes
  unit: minute
- aggregation: sum
  name: embeddings_tokens
  unit: token
- aggregation: sum
  name: fine_tuning_training_tokens
  unit: token
name: Openai Finops
provider_name: OpenAI
provider_slug: openai
publisher_name: OpenAI
service_category: AI and Machine Learning
slug: openai-finops
source_filename: openai-finops.yml
source_heading: FinOps Profile
source_url: https://developers.openai.com/api/docs/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenAI\nproviderId: openai\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI\n  - Tokens\ndescription: 'FOCUS-aligned FinOps for OpenAI: token-based metering across model tiers with batch and\n  cached-input lanes.'\nsources:\n  - https://developers.openai.com/api/docs/pricing\n  - https://platform.openai.com/docs/guides/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenAI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  primaryUnit: token\nfocusColumns:\n  ServiceName: OpenAI API\n  ServiceCategory: AI and Machine Learning\n\
  \  ProviderName: OpenAI\n  PublisherName: OpenAI\n  PricingUnit: MTok\nmeters:\n  - name: input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - project\n      - user\n      - cached\n  - name: output_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - project\n      - user\n  - name: cached_input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n  - name: image_generations\n    unit: image\n    aggregation: sum\n  - name: audio_minutes\n    unit: minute\n    aggregation: sum\n  - name: embeddings_tokens\n    unit: token\n    aggregation: sum\n  - name: fine_tuning_training_tokens\n    unit: token\n    aggregation: sum\ndiscountModels:\n  - name: Cached input\n    discount: ~10x cheaper than uncached\n  - name: Batch API\n    discount: 50% off\n  - name: Flex tier\n    discount: Reduced cost / lower priority\nprinciples:\n  - name: Visibility\n    description: Use Usage dashboard and Cost\
  \ Tracking API for per-project spend.\n  - name: Allocation\n    description: Use API keys per project; tag requests with metadata for chargeback.\n  - name: Optimization\n    description: Pick the smallest viable model, prompt-cache repeated content, batch async work.\n  - name: Accountability\n    description: Set per-project hard spend limits and email alerts.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/finops/openai-finops.yml
sources:
- https://developers.openai.com/api/docs/pricing
- https://platform.openai.com/docs/guides/rate-limits
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI
- Tokens
---
