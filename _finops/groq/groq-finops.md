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
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Groq API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Groq
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Groq
  PublisherName: Groq
  ServiceCategory: Developer Tools / API
  ServiceName: Groq
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
name: Groq Finops
provider_name: Groq
provider_slug: groq
publisher_name: Groq
service_category: API
slug: groq-finops
source_filename: groq-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Groq\nproviderId: groq\npublisherName: Groq\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - LLM\n  - Inference\n  - LPU\n  - Low Latency\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Groq API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application,\
  \ and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education\
  \ and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Groq\n  ServiceCategory: Developer Tools / API\n  ProviderName: Groq\n  PublisherName: Groq\n  InvoiceIssuerName: Groq\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n\
  \  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Groq Chat Completions API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Chat\n      - Completions\n      - LLM\n    serviceName: Groq Chat Completions API\n    serviceCategory: API\n  - name: Groq Reasoning API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Reasoning\n      - Chain of Thought\n    serviceName: Groq Reasoning API\n    serviceCategory: API\n  - name: Groq Vision API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Vision\n      - OCR\n      - Multimodal\n    serviceName: Groq Vision API\n    serviceCategory: API\n  - name: Groq Speech-to-Text API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Speech to Text\n      - Transcription\n      - Whisper\n    serviceName: Groq Speech-to-Text\
  \ API\n    serviceCategory: API\n  - name: Groq Text-to-Speech API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Text to Speech\n      - Audio\n      - Orpheus\n    serviceName: Groq Text-to-Speech API\n    serviceCategory: API\n  - name: Groq Content Moderation API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Moderation\n      - Safety\n      - Llama Guard\n    serviceName: Groq Content Moderation API\n    serviceCategory: API\n  - name: Groq Batch API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Batch\n      - Async\n    serviceName: Groq Batch API\n    serviceCategory: API\n  - name: Groq Flex Processing API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Flex\n      - Service Tier\n    serviceName: Groq Flex Processing API\n    serviceCategory: API\n  - name: Groq Files API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Files\n      - Storage\n    serviceName: Groq Files API\n    serviceCategory:\
  \ API\n  - name: Groq Models API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Models\n      - Catalog\n    serviceName: Groq Models API\n    serviceCategory: API\n  - name: Groq Tools API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Tools\n      - Web Search\n      - Code Execution\n    serviceName: Groq Tools API\n    serviceCategory: API\n  - name: Groq LoRA Inference API\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - LoRA\n      - Custom Models\n      - Fine-Tuning\n    serviceName: Groq LoRA Inference API\n    serviceCategory: API\n  - name: Groq Prompt Caching\n    baseURL: https://api.groq.com/openai/v1\n    tags:\n      - Prompt Caching\n      - Optimization\n    serviceName: Groq Prompt Caching\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target:\
  \ TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/groq/refs/heads/main/finops/groq-finops.yml
sources: []
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
