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
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Together AI API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Together AI
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Together AI
  PublisherName: Together AI
  ServiceCategory: Developer Tools / API
  ServiceName: Together AI
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
name: Together Ai Finops
provider_name: Together AI
provider_slug: together-ai
publisher_name: Together AI
service_category: API
slug: together-ai-finops
source_filename: together-ai-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Together AI\nproviderId: together-ai\npublisherName: Together AI\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - LLM\n  - Inference\n  - Foundation Models\n  - GPU\n  - Open Source AI\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Together AI API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Together AI\n  ServiceCategory: Developer Tools / API\n  ProviderName: Together AI\n  PublisherName: Together AI\n  InvoiceIssuerName: Together AI\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Together Chat Completions API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Chat\n      - Completions\n      - LLM\n    serviceName: Together Chat Completions API\n    serviceCategory: API\n  - name: Together Completions API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Completions\n      - LLM\n    serviceName: Together Completions API\n    serviceCategory: API\n  - name: Together Embeddings API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Embeddings\n      - Vector\n      - Retrieval\n    serviceName: Together Embeddings API\n    serviceCategory: API\n  - name: Together Rerank API\n    baseURL: https://api.together.ai/v1\n   \
  \ tags:\n      - Rerank\n      - Retrieval\n      - RAG\n    serviceName: Together Rerank API\n    serviceCategory: API\n  - name: Together Images API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Images\n      - Generation\n      - Diffusion\n    serviceName: Together Images API\n    serviceCategory: API\n  - name: Together Video API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Video\n      - Generation\n      - Multimodal\n    serviceName: Together Video API\n    serviceCategory: API\n  - name: Together Audio API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Audio\n      - Speech\n      - TTS\n      - STT\n    serviceName: Together Audio API\n    serviceCategory: API\n  - name: Together Vision API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Vision\n      - Multimodal\n      - Documents\n    serviceName: Together Vision API\n    serviceCategory: API\n  - name: Together Fine-Tuning API\n    baseURL: https://api.together.ai/v1\n\
  \    tags:\n      - Fine-Tuning\n      - LoRA\n      - Training\n    serviceName: Together Fine-Tuning API\n    serviceCategory: API\n  - name: Together Files API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Files\n      - Storage\n    serviceName: Together Files API\n    serviceCategory: API\n  - name: Together Models API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Models\n      - Catalog\n    serviceName: Together Models API\n    serviceCategory: API\n  - name: Together Batch API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Batch\n      - Async\n    serviceName: Together Batch API\n    serviceCategory: API\n  - name: Together Code Interpreter API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Code\n      - Execution\n      - Sandbox\n    serviceName: Together Code Interpreter API\n    serviceCategory: API\n  - name: Together Evaluations API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Evaluations\n      -\
  \ Quality\n    serviceName: Together Evaluations API\n    serviceCategory: API\n  - name: Together Dedicated Endpoints API\n    baseURL: https://api.together.ai/v1\n    tags:\n      - Dedicated\n      - Endpoints\n      - Deployment\n    serviceName: Together Dedicated Endpoints API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/together-ai/refs/heads/main/finops/together-ai-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- LLM
- Inference
- Foundation Models
- GPU
- Open Source AI
- FinOps
- Cost Management
- FOCUS
---
