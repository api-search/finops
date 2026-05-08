---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: moonshot-ai-openapi.json
  format: json
  label: Moonshot AI Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/moonshot-ai/refs/heads/main/openapi/moonshot-ai-openapi.json
billing_model:
  billingCurrency: CNY/USD
  billingFrequency: On-Demand (Recharge)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage Based
description: FOCUS-aligned FinOps profile for Moonshot AI / Kimi. Billing model is prepaid recharge with pay-as-you-go consumption metered against per-million-token rates per model and per direction (input cache-hit, input cache-miss, output). Batch jobs are billed at 50% of online rates.
focus_columns:
  BillingCurrency: CNY
  ChargeCategory: Usage
  InvoiceIssuerName: Moonshot AI
  ProviderName: Moonshot AI
  PublisherName: Moonshot AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Moonshot AI Platform
layout: finops
meters:
- aggregation: sum
  description: Input tokens billed when cache miss occurs.
  dimensions:
  - model
  - account
  name: input_tokens_cache_miss
  unit: tokens
- aggregation: sum
  description: Discounted input tokens served from prompt cache.
  dimensions:
  - model
  - account
  name: input_tokens_cache_hit
  unit: tokens
- aggregation: sum
  description: Generated output tokens.
  dimensions:
  - model
  - account
  name: output_tokens
  unit: tokens
- aggregation: sum
  description: Batch endpoint tokens (50% discount versus online).
  dimensions:
  - model
  - account
  name: batch_tokens
  unit: tokens
- aggregation: sum
  description: Web search tool invocations.
  dimensions:
  - account
  name: web_search_calls
  unit: calls
name: Moonshot Ai Finops
provider_name: Moonshot AI
provider_slug: moonshot-ai
publisher_name: Moonshot AI
service_category: AI and Machine Learning
slug: moonshot-ai-finops
source_filename: moonshot-ai-finops.yml
source_heading: FinOps Profile
source_url: https://platform.kimi.ai/docs/pricing/chat
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Moonshot AI\nproviderId: moonshot-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Inference\n- Long Context\n- Kimi\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Moonshot AI / Kimi. Billing model is prepaid recharge with\n  pay-as-you-go consumption metered against per-million-token rates per model and per direction\n  (input cache-hit, input cache-miss, output). Batch jobs are billed at 50% of online rates.\nnotes: >-\n  Prepaid balance maps to FOCUS Purchase / Adjustment categories; consumption maps to Usage.\n  Document extraction and storage are free at reconciliation; expect them to monetize later.\nsources:\n- https://platform.kimi.ai/docs/pricing/chat\n- https://platform.kimi.ai/docs/pricing/batch\n- https://platform.kimi.ai/docs/pricing/limits\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Moonshot AI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Usage Based\n  billingFrequency: On-Demand (Recharge)\n  billingCurrency: CNY/USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Moonshot AI Platform\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Moonshot AI\n  PublisherName: Moonshot AI\n  InvoiceIssuerName: Moonshot AI\n  BillingCurrency: CNY\n  ChargeCategory: Usage\nmeters:\n- name: input_tokens_cache_miss\n  description: Input tokens billed when cache miss occurs.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - model\n  - account\n- name: input_tokens_cache_hit\n  description: Discounted input tokens served from prompt cache.\n  unit: tokens\n  aggregation:\
  \ sum\n  dimensions:\n  - model\n  - account\n- name: output_tokens\n  description: Generated output tokens.\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - model\n  - account\n- name: batch_tokens\n  description: Batch endpoint tokens (50% discount versus online).\n  unit: tokens\n  aggregation: sum\n  dimensions:\n  - model\n  - account\n- name: web_search_calls\n  description: Web search tool invocations.\n  unit: calls\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use the Balance API and console usage exports to track recharge balance and consumption.\n- name: Allocation\n  description: Tag API keys per workload/team to attribute model spend.\n- name: Optimization\n  description: Prefer prompt caching, batch endpoints (50% off), shorter contexts, and right-sized models.\n- name: Accountability\n  description: Monitor tier ceiling utilization and renegotiate at $3K/$10K cumulative-recharge tier breaks.\nmaintainers:\n- FN: Kin\
  \ Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moonshot-ai/refs/heads/main/finops/moonshot-ai-finops.yml
sources:
- https://platform.kimi.ai/docs/pricing/chat
- https://platform.kimi.ai/docs/pricing/batch
- https://platform.kimi.ai/docs/pricing/limits
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Inference
- Long Context
- Kimi
- FinOps
- Cost Management
- FOCUS
---
