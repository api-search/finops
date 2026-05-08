---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Chat Completions API
  slug: fireworks-chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Completions API
  slug: fireworks-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Vision API
  slug: fireworks-vision-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Embeddings API
  slug: fireworks-embeddings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Rerank API
  slug: fireworks-rerank-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Images API
  slug: fireworks-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Audio API
  slug: fireworks-audio-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Batch Inference API
  slug: fireworks-batch-inference-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Fine-Tuning API
  slug: fireworks-fine-tuning-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Files API
  slug: fireworks-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Models API
  slug: fireworks-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Deployments API
  slug: fireworks-deployments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
- filename: fireworks-ai-merged-openapi.yml
  format: yaml
  label: Fireworks Account API
  slug: fireworks-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/openapi/fireworks-ai-merged-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Fireworks AI API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Fireworks AI
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Fireworks AI
  PublisherName: Fireworks AI
  ServiceCategory: Developer Tools / API
  ServiceName: Fireworks AI
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Fireworks Ai Finops
provider_name: Fireworks AI
provider_slug: fireworks-ai
publisher_name: Fireworks AI
service_category: API
slug: fireworks-ai-finops
source_filename: fireworks-ai-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Fireworks AI\nproviderId: fireworks-ai\npublisherName: Fireworks AI\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - LLM\n  - Inference\n  - Multimodal\n  - Fine-tuning\n  - GPU\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Fireworks AI API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Fireworks AI\n  ServiceCategory: Developer Tools / API\n  ProviderName: Fireworks AI\n  PublisherName: Fireworks AI\n  InvoiceIssuerName: Fireworks AI\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Fireworks Chat Completions API\n    baseURL: https://api.fireworks.ai/inference/v1\n    tags:\n      - Chat\n      - Completions\n      - LLM\n    serviceName: Fireworks Chat Completions API\n    serviceCategory: API\n  - name: Fireworks Completions API\n    baseURL: https://api.fireworks.ai/inference/v1\n    tags:\n      - Completions\n      - LLM\n    serviceName: Fireworks Completions API\n    serviceCategory: API\n  - name: Fireworks Vision API\n    baseURL: https://api.fireworks.ai/inference/v1\n    tags:\n      - Vision\n      - Multimodal\n      - Documents\n    serviceName: Fireworks Vision API\n    serviceCategory: API\n  - name: Fireworks Embeddings API\n    baseURL:\
  \ https://api.fireworks.ai/inference/v1\n    tags:\n      - Embeddings\n      - Vector\n      - Retrieval\n    serviceName: Fireworks Embeddings API\n    serviceCategory: API\n  - name: Fireworks Rerank API\n    baseURL: https://api.fireworks.ai/inference/v1\n    tags:\n      - Rerank\n      - Retrieval\n      - RAG\n    serviceName: Fireworks Rerank API\n    serviceCategory: API\n  - name: Fireworks Images API\n    baseURL: https://api.fireworks.ai/inference/v1\n    tags:\n      - Images\n      - Generation\n      - Stable Diffusion\n    serviceName: Fireworks Images API\n    serviceCategory: API\n  - name: Fireworks Audio API\n    baseURL: https://audio-prod.us-virginia-1.direct.fireworks.ai/v1\n    tags:\n      - Audio\n      - Speech to Text\n      - Text to Speech\n      - Whisper\n    serviceName: Fireworks Audio API\n    serviceCategory: API\n  - name: Fireworks Batch Inference API\n    baseURL: https://api.fireworks.ai/inference/v1\n    tags:\n      - Batch\n      - Async\n   \
  \ serviceName: Fireworks Batch Inference API\n    serviceCategory: API\n  - name: Fireworks Fine-Tuning API\n    baseURL: https://api.fireworks.ai/v1\n    tags:\n      - Fine-Tuning\n      - LoRA\n      - RFT\n      - Training\n    serviceName: Fireworks Fine-Tuning API\n    serviceCategory: API\n  - name: Fireworks Files API\n    baseURL: https://api.fireworks.ai/v1\n    tags:\n      - Files\n      - Datasets\n    serviceName: Fireworks Files API\n    serviceCategory: API\n  - name: Fireworks Models API\n    baseURL: https://api.fireworks.ai/v1\n    tags:\n      - Models\n      - Catalog\n    serviceName: Fireworks Models API\n    serviceCategory: API\n  - name: Fireworks Deployments API\n    baseURL: https://api.fireworks.ai/v1\n    tags:\n      - Deployments\n      - On-Demand\n      - GPU\n    serviceName: Fireworks Deployments API\n    serviceCategory: API\n  - name: Fireworks Account API\n    baseURL: https://api.fireworks.ai/v1\n    tags:\n      - Account\n      - Usage\n      -\
  \ Billing\n    serviceName: Fireworks Account API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fireworks-ai/refs/heads/main/finops/fireworks-ai-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- LLM
- Inference
- Multimodal
- Fine-tuning
- GPU
- FinOps
- Cost Management
- FOCUS
---
