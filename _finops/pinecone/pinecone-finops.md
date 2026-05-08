---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pinecone-db-control-openapi.yaml
  format: yaml
  label: Pinecone Database Control API
  slug: pinecone-database-control
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-db-control-openapi.yaml
- filename: pinecone-db-data-openapi.yaml
  format: yaml
  label: Pinecone Database Data API
  slug: pinecone-database-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-db-data-openapi.yaml
- filename: pinecone-inference-openapi.yaml
  format: yaml
  label: Pinecone Inference API
  slug: pinecone-inference
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-inference-openapi.yaml
- filename: pinecone-assistant-control-openapi.yaml
  format: yaml
  label: Pinecone Assistant Control API
  slug: pinecone-assistant-control
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-assistant-control-openapi.yaml
- filename: pinecone-assistant-data-openapi.yaml
  format: yaml
  label: Pinecone Assistant Data API
  slug: pinecone-assistant-data
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-assistant-data-openapi.yaml
- filename: pinecone-admin-openapi.yaml
  format: yaml
  label: Pinecone Admin API
  slug: pinecone-admin
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/openapi/pinecone-admin-openapi.yaml
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
description: FinOps framework definition for the Pinecone API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Pinecone
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Pinecone
  PublisherName: Pinecone
  ServiceCategory: Developer Tools / API
  ServiceName: Pinecone
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
name: Pinecone Finops
provider_name: Pinecone
provider_slug: pinecone
publisher_name: Pinecone
service_category: API
slug: pinecone-finops
source_filename: pinecone-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Pinecone\nproviderId: pinecone\npublisherName: Pinecone\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Vector Databases\n  - AI\n  - Embeddings\n  - RAG\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Pinecone API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Pinecone\n  ServiceCategory: Developer Tools / API\n  ProviderName: Pinecone\n  PublisherName: Pinecone\n  InvoiceIssuerName: Pinecone\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Pinecone Database Control API\n    baseURL: https://api.pinecone.io\n    tags:\n      - Vector Databases\n      - Indexes\n      - Control Plane\n    serviceName: Pinecone Database Control API\n    serviceCategory: API\n  - name: Pinecone Database Data API\n    baseURL: https://{index_host}\n    tags:\n      - Vector Databases\n      - Vectors\n      - Data Plane\n    serviceName: Pinecone Database Data API\n    serviceCategory: API\n  - name: Pinecone Inference API\n    baseURL: https://api.pinecone.io\n    tags:\n      - Embeddings\n      - Reranking\n      - AI\n    serviceName: Pinecone Inference API\n    serviceCategory: API\n  - name: Pinecone Assistant Control API\n    baseURL: https://api.pinecone.io\n    tags:\n      - Assistants\n\
  \      - RAG\n      - Control Plane\n    serviceName: Pinecone Assistant Control API\n    serviceCategory: API\n  - name: Pinecone Assistant Data API\n    baseURL: https://prod-1-data.ke.pinecone.io\n    tags:\n      - Assistants\n      - RAG\n      - Data Plane\n    serviceName: Pinecone Assistant Data API\n    serviceCategory: API\n  - name: Pinecone Admin API\n    baseURL: https://api.pinecone.io\n    tags:\n      - Admin\n      - Organizations\n      - Projects\n    serviceName: Pinecone Admin API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pinecone/refs/heads/main/finops/pinecone-finops.yml
sources: []
specification: FinOps Framework
tags:
- Vector Databases
- AI
- Embeddings
- RAG
- FinOps
- Cost Management
- FOCUS
---
