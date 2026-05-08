---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: chroma-server-api-openapi.yml
  format: yaml
  label: Chroma Server API
  slug: server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chroma/refs/heads/main/openapi/chroma-server-api-openapi.yml
- filename: chroma-cloud-api-openapi.yml
  format: yaml
  label: Chroma Cloud API
  slug: cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/chroma/refs/heads/main/openapi/chroma-cloud-api-openapi.yml
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
description: FinOps framework definition for the Chroma API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Chroma
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Chroma
  PublisherName: Chroma
  ServiceCategory: Developer Tools / API
  ServiceName: Chroma
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
name: Chroma Finops
provider_name: Chroma
provider_slug: chroma
publisher_name: Chroma
service_category: API
slug: chroma-finops
source_filename: chroma-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Chroma\nproviderId: chroma\npublisherName: Chroma\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - AI Native\n  - Apache 2.0\n  - Cloud\n  - Embeddings\n  - Hybrid Search\n  - JavaScript\n  - LLM\n  - Machine Learning\n  - Multi-Modal\n  - Open Source\n  - Python\n  - RAG\n  - Retrieval\n  - SDK\n  - Search\n  - Serverless\n  - TypeScript\n  - Vector Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Chroma API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description:\
  \ Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n   \
  \   - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Chroma\n  ServiceCategory: Developer Tools / API\n  ProviderName: Chroma\n  PublisherName: Chroma\n  InvoiceIssuerName: Chroma\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Chroma Server API\n    baseURL: https://api.trychroma.com\n    tags:\n      - AI\n      - Embeddings\n      - Machine Learning\n      - Search\n      - Vector Database\n    serviceName: Chroma Server API\n    serviceCategory: API\n  - name: Chroma Cloud API\n    baseURL: https://api.trychroma.com\n    tags:\n      - AI\n      - Cloud\n      - Embeddings\n      - Serverless\n      - Vector Database\n    serviceName: Chroma Cloud API\n    serviceCategory: API\n  - name: Chroma Python Client\n    baseURL: ''\n    tags:\n      - Embeddings\n\
  \      - Python\n      - SDK\n      - Vector Database\n    serviceName: Chroma Python Client\n    serviceCategory: API\n  - name: Chroma JavaScript Client\n    baseURL: ''\n    tags:\n      - Embeddings\n      - JavaScript\n      - SDK\n      - TypeScript\n      - Vector Database\n    serviceName: Chroma JavaScript Client\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/chroma/refs/heads/main/finops/chroma-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- AI Native
- Apache 2.0
- Cloud
- Embeddings
- Hybrid Search
- JavaScript
- LLM
- Machine Learning
- Multi-Modal
- Open Source
- Python
- RAG
- Retrieval
- SDK
- Search
- Serverless
- TypeScript
- Vector Database
- FinOps
- Cost Management
- FOCUS
---
