---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: ChatGPT API
  slug: chatgpt-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Responses API
  slug: openai-responses-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Embeddings API
  slug: openai-embeddings-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Images API
  slug: openai-images-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Audio API
  slug: openai-audio-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Moderations API
  slug: openai-moderations-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Fine-Tuning API
  slug: openai-fine-tuning-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Files API
  slug: openai-files-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Batch API
  slug: openai-batch-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Uploads API
  slug: openai-uploads-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Vector Stores API
  slug: openai-vector-stores-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Realtime API
  slug: openai-realtime-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Models API
  slug: openai-models-api
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for ChatGPT: per-seat monthly subscriptions for the consumer/business tiers plus per-token pay-as-you-go billing for the OpenAI Platform API.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: OpenAI, OpCo, LLC
  ProviderName: OpenAI
  PublisherName: OpenAI, OpCo, LLC
  ServiceCategory: AI / LLM
  ServiceName: ChatGPT
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - workspace
  name: chatgpt_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - model
  - organization
  - project
  name: tokens_input
  unit: token
- aggregation: sum
  dimensions:
  - model
  - organization
  - project
  name: tokens_output
  unit: token
- aggregation: sum
  dimensions:
  - model
  name: cached_input_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  - resolution
  name: image_generations
  unit: image
- aggregation: sum
  dimensions:
  - model
  name: audio_seconds
  unit: second
- aggregation: sum
  dimensions:
  - base_model
  name: fine_tuning_training_tokens
  unit: token
- aggregation: sum
  dimensions:
  - model
  name: batch_api_tokens
  unit: token
name: Chatgpt Finops
provider_name: ChatGPT
provider_slug: chatgpt
publisher_name: OpenAI, OpCo, LLC
service_category: AI / LLM
slug: chatgpt-finops
source_filename: chatgpt-finops.yml
source_heading: FinOps Profile
source_url: https://openai.com/chatgpt/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ChatGPT\nproviderId: chatgpt\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Artificial Intelligence\n  - LLM\ndescription: 'FOCUS-aligned FinOps for ChatGPT: per-seat monthly subscriptions for the consumer/business\n  tiers plus per-token pay-as-you-go billing for the OpenAI Platform API.'\nsources:\n  - https://openai.com/chatgpt/pricing\n  - https://openai.com/api/pricing\n  - https://platform.openai.com/docs/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenAI, OpCo, LLC\nserviceCategory: AI / LLM\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: ChatGPT\n  ServiceCategory: AI / LLM\n  ProviderName: OpenAI\n  PublisherName: OpenAI, OpCo, LLC\n  InvoiceIssuerName: OpenAI, OpCo, LLC\n  BillingCurrency: USD\nmeters:\n  - name: chatgpt_seats\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - plan\n      - workspace\n  - name: tokens_input\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - organization\n      - project\n  - name: tokens_output\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n      - organization\n      - project\n  - name: cached_input_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\n  - name: image_generations\n    unit: image\n    aggregation: sum\n    dimensions:\n      - model\n      - resolution\n  - name: audio_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n\
  \      - model\n  - name: fine_tuning_training_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - base_model\n  - name: batch_api_tokens\n    unit: token\n    aggregation: sum\n    dimensions:\n      - model\nprinciples:\n  - name: Visibility\n    description: Use the OpenAI Platform usage dashboard, the /v1/usage and /v1/organization/costs APIs,\n      and per-project API keys to break out token consumption by team/project; ChatGPT seat usage is\n      visible in the workspace admin console.\n  - name: Allocation\n    description: Tag API keys per project; use OpenAI Projects to scope budgets and route invoices.\n      For ChatGPT seats, allocate by workspace / department.\n  - name: Optimization\n    description: Use prompt caching (50% off cached input tokens), the Batch API (~50% off, 24-hour\n      SLA), structured outputs to reduce retries, and lighter models (gpt-4o-mini, o-series-mini) where\n      quality permits. Right-size frontier-model use to actual reasoning\
  \ needs.\n  - name: Accountability\n    description: Set per-project hard spend limits; enable email alerts on usage thresholds; review\n      monthly invoice line items against project budgets and renegotiate Enterprise terms based on observed\n      consumption.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chatgpt/refs/heads/main/finops/chatgpt-finops.yml
sources:
- https://openai.com/chatgpt/pricing
- https://openai.com/api/pricing
- https://platform.openai.com/docs/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Artificial Intelligence
- LLM
---
