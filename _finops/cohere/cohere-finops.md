---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cohere-chat-api-openapi.yml
  format: yaml
  label: Cohere Chat API
  slug: chat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-chat-api-openapi.yml
- filename: cohere-embed-api-openapi.yml
  format: yaml
  label: Cohere Embed API
  slug: embed-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-embed-api-openapi.yml
- filename: cohere-rerank-api-openapi.yml
  format: yaml
  label: Cohere Rerank API
  slug: rerank-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-rerank-api-openapi.yml
- filename: cohere-classify-api-openapi.yml
  format: yaml
  label: Cohere Classify API
  slug: classify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-classify-api-openapi.yml
- filename: cohere-embed-jobs-api-openapi.yml
  format: yaml
  label: Cohere Embed Jobs API
  slug: embed-jobs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-embed-jobs-api-openapi.yml
- filename: cohere-datasets-api-openapi.yml
  format: yaml
  label: Cohere Datasets API
  slug: datasets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-datasets-api-openapi.yml
- filename: cohere-models-api-openapi.yml
  format: yaml
  label: Cohere Models API
  slug: models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-models-api-openapi.yml
- filename: cohere-tokenize-api-openapi.yml
  format: yaml
  label: Cohere Tokenize API
  slug: tokenize-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-tokenize-api-openapi.yml
- filename: cohere-detokenize-api-openapi.yml
  format: yaml
  label: Cohere Detokenize API
  slug: detokenize-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/openapi/cohere-detokenize-api-openapi.yml
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
description: FinOps framework definition for the cohere API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: cohere
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: cohere
  PublisherName: cohere
  ServiceCategory: Developer Tools / API
  ServiceName: cohere
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
name: Cohere Finops
provider_name: cohere
provider_slug: cohere
publisher_name: cohere
service_category: API
slug: cohere-finops
source_filename: cohere-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: cohere\nproviderId: cohere\npublisherName: cohere\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the cohere API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: cohere\n  ServiceCategory: Developer Tools / API\n  ProviderName: cohere\n  PublisherName: cohere\n  InvoiceIssuerName: cohere\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cohere Chat API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Chat\n      - Conversational AI\n      - Large Language Models\n      - Text Generation\n    serviceName: Cohere Chat API\n    serviceCategory: API\n  - name: Cohere Embed API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Embeddings\n      - Natural Language Processing\n      - Semantic Search\n      - Vector Search\n    serviceName: Cohere Embed API\n    serviceCategory: API\n  - name: Cohere Rerank API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Information Retrieval\n      - Relevance\n      - Reranking\n      - Search\n    serviceName: Cohere Rerank API\n    serviceCategory: API\n  - name: Cohere Classify API\n\
  \    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Classification\n      - Natural Language Processing\n      - Text Analysis\n    serviceName: Cohere Classify API\n    serviceCategory: API\n  - name: Cohere Embed Jobs API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Batch Processing\n      - Embeddings\n      - Vector Search\n    serviceName: Cohere Embed Jobs API\n    serviceCategory: API\n  - name: Cohere Datasets API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Data Management\n      - Datasets\n      - Fine-Tuning\n    serviceName: Cohere Datasets API\n    serviceCategory: API\n  - name: Cohere Models API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Machine Learning\n      - Models\n    serviceName: Cohere Models API\n    serviceCategory: API\n  - name: Cohere Tokenize API\n    baseURL: https://api.cohere.com\n\
  \    tags:\n      - Artificial Intelligence\n      - Natural Language Processing\n      - Text Processing\n      - Tokenization\n    serviceName: Cohere Tokenize API\n    serviceCategory: API\n  - name: Cohere Detokenize API\n    baseURL: https://api.cohere.com\n    tags:\n      - Artificial Intelligence\n      - Natural Language Processing\n      - Text Processing\n      - Tokenization\n    serviceName: Cohere Detokenize API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cohere/refs/heads/main/finops/cohere-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
