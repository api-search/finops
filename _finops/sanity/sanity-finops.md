---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sanity-openapi.yml
  format: yaml
  label: Sanity Query API
  slug: sanity-query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sanity/refs/heads/main/openapi/sanity-openapi.yml
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
description: FinOps framework definition for the Sanity API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Sanity
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Sanity
  PublisherName: Sanity
  ServiceCategory: Developer Tools / API
  ServiceName: Sanity
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
name: Sanity Finops
provider_name: Sanity
provider_slug: sanity
publisher_name: Sanity
service_category: API
slug: sanity-finops
source_filename: sanity-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sanity\nproviderId: sanity\npublisherName: Sanity\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Headless CMS\n  - Content Management\n  - GROQ\n  - Real-Time\n  - Structured Content\n  - Developer Platform\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Sanity API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Sanity\n  ServiceCategory: Developer Tools / API\n  ProviderName: Sanity\n  PublisherName: Sanity\n  InvoiceIssuerName: Sanity\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Sanity Query API\n    baseURL: ''\n    tags:\n      - GROQ\n      - Query\n      - Content Lake\n      - CDN\n    serviceName: Sanity Query API\n    serviceCategory: API\n  - name: Sanity Mutation API\n    baseURL: ''\n    tags:\n      - Mutation\n      - Documents\n      - CRUD\n      - Content Lake\n    serviceName: Sanity Mutation API\n    serviceCategory: API\n  - name: Sanity Assets API\n    baseURL: ''\n    tags:\n      - Assets\n      - Images\n      - Files\n      - Upload\n    serviceName: Sanity Assets API\n    serviceCategory: API\n  - name: Sanity Projects API\n    baseURL: ''\n    tags:\n      - Projects\n      - Datasets\n      - Access Control\n      - Tokens\n    serviceName: Sanity\
  \ Projects API\n    serviceCategory: API\n  - name: Sanity Webhooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n      - Notifications\n      - Real-Time\n    serviceName: Sanity Webhooks API\n    serviceCategory: API\n  - name: Sanity Listen API\n    baseURL: ''\n    tags:\n      - Real-Time\n      - SSE\n      - Events\n      - Streaming\n    serviceName: Sanity Listen API\n    serviceCategory: API\n  - name: Sanity Roles API\n    baseURL: ''\n    tags:\n      - Roles\n      - Permissions\n      - Access Control\n      - Security\n    serviceName: Sanity Roles API\n    serviceCategory: API\n  - name: Sanity Scheduling API\n    baseURL: ''\n    tags:\n      - Scheduling\n      - Publishing\n      - Content Calendar\n      - Workflow\n    serviceName: Sanity Scheduling API\n    serviceCategory: API\n  - name: Sanity Embeddings Index API\n    baseURL: ''\n    tags:\n      - Embeddings\n      - Vector Search\n      - AI\n      - Semantic Search\n    serviceName: Sanity\
  \ Embeddings Index API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sanity/refs/heads/main/finops/sanity-finops.yml
sources: []
specification: FinOps Framework
tags:
- Headless CMS
- Content Management
- GROQ
- Real-Time
- Structured Content
- Developer Platform
- FinOps
- Cost Management
- FOCUS
---
