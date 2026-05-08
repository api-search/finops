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
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the OpenAI API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenAI
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: OpenAI
  PublisherName: OpenAI
  ServiceCategory: Developer Tools / API
  ServiceName: OpenAI
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
name: Openai Finops
provider_name: OpenAI
provider_slug: openai
publisher_name: OpenAI
service_category: API
slug: openai-finops
source_filename: openai-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: OpenAI\nproviderId: openai\npublisherName: OpenAI\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Artificial Intelligence\n  - Large Language Models\n  - T1\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the OpenAI API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: OpenAI\n  ServiceCategory: Developer Tools / API\n  ProviderName: OpenAI\n  PublisherName: OpenAI\n  InvoiceIssuerName: OpenAI\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpenAI Assistants API\n    baseURL: https://api.openai.com\n    tags:\n      - Assistants\n    serviceName: OpenAI Assistants API\n    serviceCategory: API\n  - name: OpenAI Audio API\n    baseURL: https://api.openai.com\n    tags:\n      - Audio\n    serviceName: OpenAI Audio API\n    serviceCategory: API\n  - name: OpenAI Chat API\n    baseURL: https://api.openai.com\n    tags:\n      - Chat\n    serviceName: OpenAI Chat API\n    serviceCategory: API\n  - name: OpenAI Chat Completions API\n    baseURL: https://api.openai.com\n    tags:\n      - Chat\n      - Completions\n    serviceName: OpenAI Chat Completions API\n    serviceCategory: API\n  - name: OpenAI Embeddings API\n    baseURL: https://api.openai.com\n    tags:\n     \
  \ - Embedding\n      - Embeddings\n      - Inputs\n      - Representing\n      - Text\n      - Vectors\n    serviceName: OpenAI Embeddings API\n    serviceCategory: API\n  - name: OpenAI Files API\n    baseURL: https://api.openai.com\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Files\n    serviceName: OpenAI Files API\n    serviceCategory: API\n  - name: OpenAI Fine Tuning API\n    baseURL: https://api.openai.com\n    tags:\n      - Fine Tune\n      - Fine Tuning\n    serviceName: OpenAI Fine Tuning API\n    serviceCategory: API\n  - name: OpenAI Images API\n    baseURL: https://api.openai.com\n    tags:\n      - Images\n    serviceName: OpenAI Images API\n    serviceCategory: API\n  - name: OpenAI Models API\n    baseURL: https://api.openai.com\n    tags:\n      - Large Language Models\n      - Models\n    serviceName: OpenAI Models API\n    serviceCategory: API\n  - name: OpenAI Threads API\n    baseURL: https://api.openai.com\n    tags:\n      - Assistants\n    \
  \  - Threads\n    serviceName: OpenAI Threads API\n    serviceCategory: API\n  - name: OpenAI Responses API\n    baseURL: https://api.openai.com\n    tags:\n      - Agents\n      - Responses\n      - Text Generation\n    serviceName: OpenAI Responses API\n    serviceCategory: API\n  - name: OpenAI Moderations API\n    baseURL: https://api.openai.com\n    tags:\n      - Content Safety\n      - Moderation\n    serviceName: OpenAI Moderations API\n    serviceCategory: API\n  - name: OpenAI Batch API\n    baseURL: https://api.openai.com\n    tags:\n      - Async\n      - Batch\n    serviceName: OpenAI Batch API\n    serviceCategory: API\n  - name: OpenAI Vector Stores API\n    baseURL: https://api.openai.com\n    tags:\n      - Retrieval\n      - Search\n      - Vector Stores\n    serviceName: OpenAI Vector Stores API\n    serviceCategory: API\n  - name: OpenAI Uploads API\n    baseURL: https://api.openai.com\n    tags:\n      - Files\n      - Uploads\n    serviceName: OpenAI Uploads API\n\
  \    serviceCategory: API\n  - name: OpenAI Realtime API\n    baseURL: https://api.openai.com\n    tags:\n      - Audio\n      - Realtime\n      - Streaming\n      - Voice\n    serviceName: OpenAI Realtime API\n    serviceCategory: API\n  - name: OpenAI Evals API\n    baseURL: https://api.openai.com\n    tags:\n      - Evals\n      - Evaluation\n      - Testing\n    serviceName: OpenAI Evals API\n    serviceCategory: API\n  - name: OpenAI Completions API\n    baseURL: https://api.openai.com\n    tags:\n      - Completions\n      - Legacy\n    serviceName: OpenAI Completions API\n    serviceCategory: API\n  - name: OpenAI Videos API\n    baseURL: https://api.openai.com\n    tags:\n      - Sora\n      - Video Generation\n      - Videos\n    serviceName: OpenAI Videos API\n    serviceCategory: API\n  - name: OpenAI Conversations API\n    baseURL: https://api.openai.com\n    tags:\n      - Conversations\n      - State Management\n    serviceName: OpenAI Conversations API\n    serviceCategory:\
  \ API\n  - name: OpenAI Containers API\n    baseURL: https://api.openai.com\n    tags:\n      - Code Interpreter\n      - Containers\n      - Sandbox\n    serviceName: OpenAI Containers API\n    serviceCategory: API\n  - name: OpenAI ChatKit API\n    baseURL: https://api.openai.com\n    tags:\n      - Agents\n      - Chat\n      - ChatKit\n    serviceName: OpenAI ChatKit API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openai/refs/heads/main/finops/openai-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Artificial Intelligence
- Large Language Models
- T1
- FinOps
- Cost Management
- FOCUS
---
