---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Mistral AI Chat API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.mistral.ai/openapi.json
- filename: mistral-embeddings-openapi.yml
  format: yaml
  label: Mistral Embeddings API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-embeddings-openapi.yml
- filename: mistral-moderation-openapi.yml
  format: yaml
  label: Mistral Moderation API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-moderation-openapi.yml
- filename: mistral-agents-openapi.yml
  format: yaml
  label: Mistral AI Agents API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-agents-openapi.yml
- filename: mistral-fim-openapi.yml
  format: yaml
  label: Mistral AI FIM API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-fim-openapi.yml
- filename: mistral-ocr-openapi.yml
  format: yaml
  label: Mistral AI OCR API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-ocr-openapi.yml
- filename: mistral-fine-tuning-openapi.yml
  format: yaml
  label: Mistral AI Fine-Tuning API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-fine-tuning-openapi.yml
- filename: mistral-files-openapi.yml
  format: yaml
  label: Mistral AI Files API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-files-openapi.yml
- filename: mistral-models-openapi.yml
  format: yaml
  label: Mistral AI Models API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-models-openapi.yml
- filename: mistral-batch-openapi.yml
  format: yaml
  label: Mistral AI Batch API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-batch-openapi.yml
- filename: mistral-audio-transcription-openapi.yml
  format: yaml
  label: Mistral AI Audio Transcription API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/openapi/mistral-audio-transcription-openapi.yml
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
description: FinOps framework definition for the Mistral AI API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mistral AI
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Mistral AI
  PublisherName: Mistral AI
  ServiceCategory: Developer Tools / API
  ServiceName: Mistral AI
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
name: Mistral Finops
provider_name: Mistral AI
provider_slug: mistral
publisher_name: Mistral AI
service_category: API
slug: mistral-finops
source_filename: mistral-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Mistral AI\nproviderId: mistral\npublisherName: Mistral AI\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Mistral AI API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be\
  \ allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Mistral AI\n  ServiceCategory: Developer Tools / API\n  ProviderName: Mistral AI\n  PublisherName: Mistral AI\n  InvoiceIssuerName: Mistral AI\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name:\
  \ compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Mistral AI Chat API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Artificial Intelligence\n      - Chat\n      - Conversational AI\n      - Large Language Models\n      - NLP\n    serviceName: Mistral AI Chat API\n    serviceCategory: API\n  - name: Mistral Embeddings API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Embeddings\n      - Machine Learning\n      - Semantic Search\n      - Vector Search\n    serviceName: Mistral Embeddings API\n    serviceCategory: API\n  - name: Mistral Moderation API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Classification\n      - Compliance\n      - Content Moderation\n      - Safety\n    serviceName: Mistral Moderation API\n    serviceCategory: API\n  - name: Mistral AI Agents API\n    baseURL:\
  \ https://api.mistral.ai/v1\n    tags:\n      - Agents\n      - Artificial Intelligence\n      - Automation\n      - Function Calling\n      - Tools\n    serviceName: Mistral AI Agents API\n    serviceCategory: API\n  - name: Mistral AI FIM API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Code Completion\n      - Code Generation\n      - Codestral\n      - Fill in the Middle\n      - Programming\n    serviceName: Mistral AI FIM API\n    serviceCategory: API\n  - name: Mistral AI OCR API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Document AI\n      - Document Understanding\n      - OCR\n      - PDF Processing\n      - Text Extraction\n    serviceName: Mistral AI OCR API\n    serviceCategory: API\n  - name: Mistral AI Fine-Tuning API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Fine-Tuning\n      - Machine Learning\n      - Model Customization\n      - Training\n    serviceName: Mistral AI Fine-Tuning API\n    serviceCategory: API\n  - name:\
  \ Mistral AI Files API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - File Management\n      - Files\n      - Storage\n      - Upload\n    serviceName: Mistral AI Files API\n    serviceCategory: API\n  - name: Mistral AI Models API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Artificial Intelligence\n      - Model Management\n      - Models\n    serviceName: Mistral AI Models API\n    serviceCategory: API\n  - name: Mistral AI Batch API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Async\n      - Batch Processing\n      - Bulk Operations\n      - Cost Optimization\n    serviceName: Mistral AI Batch API\n    serviceCategory: API\n  - name: Mistral AI Audio Transcription API\n    baseURL: https://api.mistral.ai/v1\n    tags:\n      - Audio\n      - Diarization\n      - Speech to Text\n      - Transcription\n      - Voxtral\n    serviceName: Mistral AI Audio Transcription API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mistral/refs/heads/main/finops/mistral-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
