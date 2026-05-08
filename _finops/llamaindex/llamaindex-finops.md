---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: llamaindex-llamacloud-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaCloud API
  slug: llamacloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamacloud-api-openapi.yml
- filename: llamaindex-llamaparse-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaParse API
  slug: llamaparse-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamaparse-api-openapi.yml
- filename: llamaindex-llamaextract-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaExtract API
  slug: llamaextract-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamaextract-api-openapi.yml
- filename: llamaindex-llamacloud-index-api-openapi.yml
  format: yaml
  label: LlamaIndex LlamaCloud Index API
  slug: llamacloud-index-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/openapi/llamaindex-llamacloud-index-api-openapi.yml
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
description: FinOps framework definition for the llamaindex API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: llamaindex
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: llamaindex
  PublisherName: llamaindex
  ServiceCategory: Developer Tools / API
  ServiceName: llamaindex
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
name: Llamaindex Finops
provider_name: llamaindex
provider_slug: llamaindex
publisher_name: llamaindex
service_category: API
slug: llamaindex-finops
source_filename: llamaindex-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: llamaindex\nproviderId: llamaindex\npublisherName: llamaindex\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the llamaindex API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can\
  \ be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: llamaindex\n  ServiceCategory: Developer Tools / API\n  ProviderName: llamaindex\n  PublisherName: llamaindex\n  InvoiceIssuerName: llamaindex\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name:\
  \ compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: LlamaIndex LlamaCloud API\n    baseURL: https://api.cloud.llamaindex.ai\n    tags:\n      - Agents\n      - Artificial Intelligence\n      - Cloud\n      - Documents\n      - LLM\n      - RAG\n    serviceName: LlamaIndex LlamaCloud API\n    serviceCategory: API\n  - name: LlamaIndex LlamaParse API\n    baseURL: https://api.cloud.llamaindex.ai\n    tags:\n      - Artificial Intelligence\n      - Document Parsing\n      - LLM\n      - OCR\n      - PDF\n    serviceName: LlamaIndex LlamaParse API\n    serviceCategory: API\n  - name: LlamaIndex LlamaExtract API\n    baseURL: https://api.cloud.llamaindex.ai\n    tags:\n      - Artificial Intelligence\n      - Data Extraction\n      - Documents\n      - JSON\n      - Structured Data\n    serviceName: LlamaIndex LlamaExtract API\n\
  \    serviceCategory: API\n  - name: LlamaIndex LlamaCloud Index API\n    baseURL: https://api.cloud.llamaindex.ai\n    tags:\n      - Document Ingestion\n      - Indexing\n      - RAG\n      - Retrieval\n      - Vector Store\n    serviceName: LlamaIndex LlamaCloud Index API\n    serviceCategory: API\n  - name: LlamaIndex Python Framework\n    baseURL: https://api.example.com\n    tags:\n      - Agents\n      - Framework\n      - LLM\n      - Open Source\n      - Python\n      - RAG\n      - SDK\n    serviceName: LlamaIndex Python Framework\n    serviceCategory: API\n  - name: LlamaIndex TypeScript Framework\n    baseURL: https://api.example.com\n    tags:\n      - Agents\n      - Framework\n      - JavaScript\n      - LLM\n      - Open Source\n      - RAG\n      - SDK\n      - TypeScript\n    serviceName: LlamaIndex TypeScript Framework\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name:\
  \ Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/llamaindex/refs/heads/main/finops/llamaindex-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
