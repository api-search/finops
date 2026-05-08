---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lucidworks-ai-platform-openapi.yml
  format: yaml
  label: Lucidworks AI Platform API
  slug: ai-platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-ai-platform-openapi.yml
- filename: lucidworks-embeddings-openapi.yml
  format: yaml
  label: Lucidworks Embeddings and Classification API
  slug: embeddings
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-embeddings-openapi.yml
- filename: lucidworks-signals-openapi.yml
  format: yaml
  label: Lucidworks Signals API
  slug: signals
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-signals-openapi.yml
- filename: lucidworks-rules-openapi.yml
  format: yaml
  label: Lucidworks Rules and Query Rewrites API
  slug: rules
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-rules-openapi.yml
- filename: lucidworks-chunking-openapi.yml
  format: yaml
  label: Lucidworks Content Chunking API
  slug: chunking
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-chunking-openapi.yml
- filename: lucidworks-models-openapi.yml
  format: yaml
  label: Lucidworks Model Management API
  slug: models
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/openapi/lucidworks-models-openapi.yml
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
description: FinOps framework definition for the Lucidworks API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lucidworks
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Lucidworks
  PublisherName: Lucidworks
  ServiceCategory: Developer Tools / API
  ServiceName: Lucidworks
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
name: Lucidworks Finops
provider_name: Lucidworks
provider_slug: lucidworks
publisher_name: Lucidworks
service_category: API
slug: lucidworks-finops
source_filename: lucidworks-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Lucidworks\nproviderId: lucidworks\npublisherName: Lucidworks\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Search\n  - Artificial Intelligence\n  - Enterprise Search\n  - Vector Search\n  - RAG\n  - Commerce\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Lucidworks API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Lucidworks\n  ServiceCategory: Developer Tools / API\n  ProviderName: Lucidworks\n  PublisherName: Lucidworks\n  InvoiceIssuerName: Lucidworks\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Lucidworks AI Platform API\n    baseURL: https://api.lucidworks.ai\n    tags:\n      - Artificial Intelligence\n      - Predictions\n      - RAG\n      - Summarization\n      - NER\n      - LLM\n    serviceName: Lucidworks AI Platform API\n    serviceCategory: API\n  - name: Lucidworks Embeddings and Classification API\n    baseURL: https://api.lucidworks.ai\n    tags:\n      - Embeddings\n      - Vector Search\n      - Classification\n      - Tokenization\n      - Machine Learning\n    serviceName: Lucidworks Embeddings and Classification API\n    serviceCategory: API\n  - name: Lucidworks Signals API\n    baseURL: https://api.lucidworks.ai\n    tags:\n      - Signals\n\
  \      - Analytics\n      - Click Tracking\n      - Commerce\n    serviceName: Lucidworks Signals API\n    serviceCategory: API\n  - name: Lucidworks Rules and Query Rewrites API\n    baseURL: https://api.lucidworks.ai\n    tags:\n      - Business Rules\n      - Query Rewrites\n      - Search Tuning\n      - Commerce\n    serviceName: Lucidworks Rules and Query Rewrites API\n    serviceCategory: API\n  - name: Lucidworks Content Chunking API\n    baseURL: https://api.lucidworks.ai\n    tags:\n      - Chunking\n      - Content Processing\n      - RAG\n      - Indexing\n    serviceName: Lucidworks Content Chunking API\n    serviceCategory: API\n  - name: Lucidworks Model Management API\n    baseURL: https://api.lucidworks.ai\n    tags:\n      - Model Management\n      - MLOps\n      - Deployment\n    serviceName: Lucidworks Model Management API\n    serviceCategory: API\n  - name: Lucidworks Fusion REST API\n    baseURL: ''\n    tags:\n      - Fusion\n      - Enterprise Search\n      - Indexing\n\
  \      - Pipelines\n      - Connectors\n    serviceName: Lucidworks Fusion REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lucidworks/refs/heads/main/finops/lucidworks-finops.yml
sources: []
specification: FinOps Framework
tags:
- Search
- Artificial Intelligence
- Enterprise Search
- Vector Search
- RAG
- Commerce
- FinOps
- Cost Management
- FOCUS
---
