---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Schema Stitching API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Schema Stitching
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Schema Stitching
  PublisherName: Schema Stitching
  ServiceCategory: Developer Tools / API
  ServiceName: Schema Stitching
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
name: Schema Stitching Finops
provider_name: Schema Stitching
provider_slug: schema-stitching
publisher_name: Schema Stitching
service_category: API
slug: schema-stitching-finops
source_filename: schema-stitching-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Schema Stitching\nproviderId: schema-stitching\npublisherName: Schema Stitching\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - API Composition\n  - API Gateway\n  - Federation\n  - GraphQL\n  - Microservices\n  - Schema Stitching\n  - Type Merging\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Schema Stitching API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Schema Stitching\n  ServiceCategory: Developer Tools / API\n  ProviderName: Schema Stitching\n  PublisherName: Schema Stitching\n  InvoiceIssuerName: Schema Stitching\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Schema Stitching\n    baseURL: ''\n    tags:\n      - API Composition\n      - GraphQL\n      - Schema Stitching\n      - Type Merging\n    serviceName: Schema Stitching\n    serviceCategory: API\n  - name: GraphQL Mesh\n    baseURL: ''\n    tags:\n      - API Gateway\n      - GraphQL\n      - Schema Stitching\n    serviceName: GraphQL Mesh\n    serviceCategory: API\n  - name: Hive Gateway\n    baseURL: ''\n    tags:\n      - API Gateway\n      - Federation\n      - GraphQL\n    serviceName: Hive Gateway\n    serviceCategory: API\n  - name: Apollo Federation\n    baseURL: ''\n    tags:\n      - API\
  \ Gateway\n      - Apollo\n      - Federation\n      - GraphQL\n    serviceName: Apollo Federation\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/schema-stitching/refs/heads/main/finops/schema-stitching-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Composition
- API Gateway
- Federation
- GraphQL
- Microservices
- Schema Stitching
- Type Merging
- FinOps
- Cost Management
- FOCUS
---
