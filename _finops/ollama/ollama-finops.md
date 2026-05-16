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
  label: Ollama API
  slug: ollama-api
  spec_type: OpenAPI
  url: https://docs.ollama.com/openapi.yaml
- filename: ollama-openai-compatibility-api-openapi.yml
  format: yaml
  label: Ollama OpenAI Compatibility API
  slug: ollama-openai-compatibility-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ollama/refs/heads/main/openapi/ollama-openai-compatibility-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Subscription (Tiered) + Self-Hosted Free
description: 'FOCUS-aligned FinOps for Ollama: local inference is free and self-hosted; Ollama Cloud is a tiered subscription priced on GPU utilization rather than tokens, with concurrency caps per tier.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Ollama Inc.
  PricingCategory: Subscription
  PricingUnit: month
  ProviderName: Ollama
  PublisherName: Ollama Inc.
  ServiceCategory: AI Infrastructure
  ServiceName: Ollama
layout: finops
meters:
- aggregation: sum
  description: Per-account Ollama Cloud subscription (Free, Pro, Max)
  dimensions:
  - tier
  - billing_cycle
  name: cloud_subscription
  unit: month
- aggregation: sum
  description: GPU time consumed on Ollama Cloud (the actual consumption meter)
  dimensions:
  - model
  - region
  name: cloud_gpu_time
  unit: gpu-second
- aggregation: max
  description: Peak concurrent cloud model count (used to size tier)
  dimensions:
  - account
  name: cloud_concurrent_models
  unit: model
- aggregation: sum
  description: Local Ollama requests (no charge from Ollama; cost is hardware/power)
  dimensions:
  - model
  - host
  name: local_inference_requests
  unit: request
name: Ollama Finops
provider_name: Ollama
provider_slug: ollama
publisher_name: Ollama Inc.
service_category: AI Infrastructure
slug: ollama-finops
source_filename: ollama-finops.yml
source_heading: FinOps Profile
source_url: https://ollama.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ollama\nproviderId: ollama\npublisherName: Ollama Inc.\nserviceCategory: AI Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Artificial Intelligence\n  - Large Language Models\n  - Models\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Ollama: local inference is free and self-hosted; Ollama Cloud is\n  a tiered subscription priced on GPU utilization rather than tokens, with concurrency caps per tier.'\nsources:\n  - https://ollama.com/pricing\n  - https://docs.ollama.com/cloud\n  - https://docs.ollama.com/api/authentication\nprinciples:\n  - name: Visibility\n    description:\
  \ For local Ollama, track GPU/CPU utilization and electricity cost as the unit cost. For\n      Ollama Cloud, track concurrent model count and weekly GPU-time budget on the ollama.com dashboard;\n      Ollama does not charge per token.\n  - name: Allocation\n    description: Allocate Ollama Cloud subscriptions per developer or team (one Pro/Max per active developer).\n      For self-hosted GPUs, allocate the inference server's amortized hardware + power cost across consuming\n      products by tagged request metadata.\n  - name: Optimization\n    description: Run common, latency-tolerant inference locally; reserve cloud (Pro/Max) for large models\n      that exceed local VRAM (e.g. gpt-oss:120b-cloud). Right-size the tier — Pro at $20/mo replaces ad-hoc\n      large-model rentals; Max at $100/mo only when sustained 10x concurrency is needed.\n  - name: Accountability\n    description: Designate a per-team owner for each Ollama Cloud account. Review weekly cloud GPU-time\n      consumption\
  \ against the tier; downgrade to Free if Cloud is dormant. For self-hosted, the platform\n      team owns hardware utilization targets.\nbillingModel:\n  pricingCategory: Subscription (Tiered) + Self-Hosted Free\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Ollama\n  ServiceCategory: AI Infrastructure\n  ProviderName: Ollama\n  PublisherName: Ollama Inc.\n  InvoiceIssuerName: Ollama Inc.\n  PricingCategory: Subscription\n  PricingUnit: month\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: cloud_subscription\n    description: Per-account Ollama Cloud subscription (Free, Pro, Max)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - billing_cycle\n  - name: cloud_gpu_time\n    description: GPU time consumed on Ollama Cloud (the actual consumption meter)\n    unit: gpu-second\n    aggregation:\
  \ sum\n    dimensions:\n      - model\n      - region\n  - name: cloud_concurrent_models\n    description: Peak concurrent cloud model count (used to size tier)\n    unit: model\n    aggregation: max\n    dimensions:\n      - account\n  - name: local_inference_requests\n    description: Local Ollama requests (no charge from Ollama; cost is hardware/power)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - model\n      - host\napis:\n  - name: Ollama API\n    baseURL: http://localhost:11434/api\n    tags:\n      - Inference\n      - Large Language Models\n      - Local AI\n    serviceName: Ollama API\n    serviceCategory: AI Infrastructure\n  - name: Ollama OpenAI Compatibility API\n    baseURL: http://localhost:11434/v1\n    tags:\n      - Chat\n      - Compatibility\n      - OpenAI\n    serviceName: Ollama OpenAI Compatibility API\n    serviceCategory: AI Infrastructure\n  - name: Ollama Anthropic Compatibility API\n    baseURL: http://localhost:11434\n    tags:\n    \
  \  - Anthropic\n      - Chat\n      - Compatibility\n    serviceName: Ollama Anthropic Compatibility API\n    serviceCategory: AI Infrastructure\n  - name: Ollama Cloud API\n    baseURL: https://ollama.com/api\n    tags:\n      - Cloud\n      - Inference\n    serviceName: Ollama Cloud API\n    serviceCategory: AI Infrastructure\nunitEconomics:\n  - name: Cloud cost per active developer\n    metric: cloud_subscription_cost / active_developers_using_cloud\n    target: '$20-100/mo per developer based on tier'\n  - name: Local cost per inference\n    metric: (gpu_amortization + electricity) / local_inference_requests\n    target: minimize via batching\n  - name: Cloud GPU-time efficiency\n    metric: cloud_gpu_time / cloud_useful_completions\n    target: monitor weekly against tier ceiling\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ollama/refs/heads/main/finops/ollama-finops.yml
sources:
- https://ollama.com/pricing
- https://docs.ollama.com/cloud
- https://docs.ollama.com/api/authentication
specification: FinOps Framework
tags:
- Artificial Intelligence
- Large Language Models
- Models
- FinOps
- Cost Management
- FOCUS
---
