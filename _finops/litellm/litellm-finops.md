---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: litellm-openapi.yml
  format: yaml
  label: LiteLLM Chat Completions API
  slug: chat-completions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/litellm/refs/heads/main/openapi/litellm-openapi.yml
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
description: FinOps framework definition for the LiteLLM API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: LiteLLM
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: LiteLLM
  PublisherName: LiteLLM
  ServiceCategory: Developer Tools / API
  ServiceName: LiteLLM
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
name: Litellm Finops
provider_name: LiteLLM
provider_slug: litellm
publisher_name: LiteLLM
service_category: API
slug: litellm-finops
source_filename: litellm-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: LiteLLM\nproviderId: litellm\npublisherName: LiteLLM\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Gateways\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the LiteLLM API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can\
  \ be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: LiteLLM\n  ServiceCategory: Developer Tools / API\n  ProviderName: LiteLLM\n  PublisherName: LiteLLM\n  InvoiceIssuerName: LiteLLM\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n\
  \    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: LiteLLM Chat Completions API\n    baseURL: ''\n    tags:\n      - AI\n      - Chat\n      - Completions\n      - LLM\n    serviceName: LiteLLM Chat Completions API\n    serviceCategory: API\n  - name: LiteLLM Completions API\n    baseURL: ''\n    tags:\n      - Completions\n      - LLM\n      - Text\n    serviceName: LiteLLM Completions API\n    serviceCategory: API\n  - name: LiteLLM Responses API\n    baseURL: ''\n    tags:\n      - AI\n      - LLM\n      - Responses\n    serviceName: LiteLLM Responses API\n    serviceCategory: API\n  - name: LiteLLM Embeddings API\n    baseURL: ''\n    tags:\n      - AI\n      - Embeddings\n      - Vectors\n    serviceName: LiteLLM Embeddings API\n    serviceCategory: API\n  - name: LiteLLM Image Generation API\n    baseURL: ''\n    tags:\n      - AI\n\
  \      - Generation\n      - Images\n    serviceName: LiteLLM Image Generation API\n    serviceCategory: API\n  - name: LiteLLM Audio API\n    baseURL: ''\n    tags:\n      - AI\n      - Audio\n      - Speech\n      - Transcription\n    serviceName: LiteLLM Audio API\n    serviceCategory: API\n  - name: LiteLLM Moderations API\n    baseURL: ''\n    tags:\n      - Content\n      - Moderation\n      - Safety\n    serviceName: LiteLLM Moderations API\n    serviceCategory: API\n  - name: LiteLLM Batches API\n    baseURL: ''\n    tags:\n      - Batches\n      - Bulk\n      - Processing\n    serviceName: LiteLLM Batches API\n    serviceCategory: API\n  - name: LiteLLM Files API\n    baseURL: ''\n    tags:\n      - Files\n      - Management\n    serviceName: LiteLLM Files API\n    serviceCategory: API\n  - name: LiteLLM Fine-Tuning API\n    baseURL: ''\n    tags:\n      - Fine-Tuning\n      - Models\n      - Training\n    serviceName: LiteLLM Fine-Tuning API\n    serviceCategory: API\n  - name:\
  \ LiteLLM Rerank API\n    baseURL: ''\n    tags:\n      - Relevance\n      - Rerank\n      - Search\n    serviceName: LiteLLM Rerank API\n    serviceCategory: API\n  - name: LiteLLM Vector Stores API\n    baseURL: ''\n    tags:\n      - RAG\n      - Search\n      - Storage\n      - Vectors\n    serviceName: LiteLLM Vector Stores API\n    serviceCategory: API\n  - name: LiteLLM Anthropic Messages API\n    baseURL: ''\n    tags:\n      - AI\n      - Anthropic\n      - Messages\n    serviceName: LiteLLM Anthropic Messages API\n    serviceCategory: API\n  - name: LiteLLM Realtime API\n    baseURL: ''\n    tags:\n      - Realtime\n      - Streaming\n      - WebSocket\n    serviceName: LiteLLM Realtime API\n    serviceCategory: API\n  - name: LiteLLM MCP API\n    baseURL: ''\n    tags:\n      - MCP\n      - Protocols\n      - Tools\n    serviceName: LiteLLM MCP API\n    serviceCategory: API\n  - name: LiteLLM OCR API\n    baseURL: ''\n    tags:\n      - Images\n      - OCR\n      - Text Extraction\n\
  \    serviceName: LiteLLM OCR API\n    serviceCategory: API\n  - name: LiteLLM Guardrails API\n    baseURL: ''\n    tags:\n      - Content Filtering\n      - Guardrails\n      - Safety\n    serviceName: LiteLLM Guardrails API\n    serviceCategory: API\n  - name: LiteLLM Evals API\n    baseURL: ''\n    tags:\n      - Benchmarks\n      - Evaluations\n      - Performance\n    serviceName: LiteLLM Evals API\n    serviceCategory: API\n  - name: LiteLLM A2A Agent Gateway API\n    baseURL: ''\n    tags:\n      - A2A\n      - Agents\n      - Gateway\n    serviceName: LiteLLM A2A Agent Gateway API\n    serviceCategory: API\n  - name: LiteLLM Videos API\n    baseURL: ''\n    tags:\n      - AI\n      - Generation\n      - Videos\n    serviceName: LiteLLM Videos API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/litellm/refs/heads/main/finops/litellm-finops.yml
sources: []
specification: FinOps Framework
tags:
- Gateways
- FinOps
- Cost Management
- FOCUS
---
