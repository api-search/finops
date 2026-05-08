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
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Responses API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Embeddings API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Images API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Audio API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Moderations API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Fine-Tuning API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Files API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Batch API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Uploads API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Vector Stores API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Realtime API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: OpenAI Models API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/openai/openai-openapi/blob/master/openapi.yaml
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
description: FinOps framework definition for the ChatGPT API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: ChatGPT
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: ChatGPT
  PublisherName: ChatGPT
  ServiceCategory: Developer Tools / API
  ServiceName: ChatGPT
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
name: Chatgpt Finops
provider_name: ChatGPT
provider_slug: chatgpt
publisher_name: ChatGPT
service_category: API
slug: chatgpt-finops
source_filename: chatgpt-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: ChatGPT\nproviderId: chatgpt\npublisherName: ChatGPT\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agents\n  - AI\n  - ChatGPT\n  - Embeddings\n  - Fine-Tuning\n  - GPT-4\n  - GPT-5\n  - Language Model\n  - OpenAI\n  - Realtime\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the ChatGPT API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: ChatGPT\n  ServiceCategory: Developer Tools / API\n  ProviderName: ChatGPT\n  PublisherName: ChatGPT\n  InvoiceIssuerName: ChatGPT\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ChatGPT API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Chatbot\n      - Conversational AI\n      - Machine Learning\n      - Natural Language Processing\n    serviceName: ChatGPT API\n    serviceCategory: API\n  - name: OpenAI Responses API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Agents\n      - Artificial Intelligence\n      - Conversational AI\n      - Responses\n      - Tools\n    serviceName: OpenAI Responses API\n    serviceCategory: API\n  - name: OpenAI Embeddings API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Embeddings\n      - Machine Learning\n\
  \      - Search\n    serviceName: OpenAI Embeddings API\n    serviceCategory: API\n  - name: OpenAI Images API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Creative AI\n      - DALL-E\n      - Image Generation\n    serviceName: OpenAI Images API\n    serviceCategory: API\n  - name: OpenAI Audio API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Audio\n      - Speech\n      - Text-To-Speech\n      - Transcription\n    serviceName: OpenAI Audio API\n    serviceCategory: API\n  - name: OpenAI Moderations API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Content Safety\n      - Moderation\n      - Trust And Safety\n    serviceName: OpenAI Moderations API\n    serviceCategory: API\n  - name: OpenAI Fine-Tuning API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Fine-Tuning\n      - Machine Learning\n      -\
  \ Model Customization\n    serviceName: OpenAI Fine-Tuning API\n    serviceCategory: API\n  - name: OpenAI Files API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Files\n      - Storage\n      - Uploads\n    serviceName: OpenAI Files API\n    serviceCategory: API\n  - name: OpenAI Batch API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Asynchronous\n      - Batch Processing\n      - Cost Optimization\n    serviceName: OpenAI Batch API\n    serviceCategory: API\n  - name: OpenAI Uploads API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Files\n      - Large Files\n      - Uploads\n    serviceName: OpenAI Uploads API\n    serviceCategory: API\n  - name: OpenAI Vector Stores API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - File Search\n      - Retrieval\n      - Vector Stores\n    serviceName: OpenAI Vector\
  \ Stores API\n    serviceCategory: API\n  - name: OpenAI Realtime API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Audio\n      - Realtime\n      - Speech\n      - WebSocket\n    serviceName: OpenAI Realtime API\n    serviceCategory: API\n  - name: OpenAI Models API\n    baseURL: https://api.openai.com/v1\n    tags:\n      - Artificial Intelligence\n      - Models\n    serviceName: OpenAI Models API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: OpenAI\n    email: support@openai.com\n    url: https://openai.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chatgpt/refs/heads/main/finops/chatgpt-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agents
- AI
- ChatGPT
- Embeddings
- Fine-Tuning
- GPT-4
- GPT-5
- Language Model
- OpenAI
- Realtime
- FinOps
- Cost Management
- FOCUS
---
