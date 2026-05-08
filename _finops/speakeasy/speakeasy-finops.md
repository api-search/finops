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
  label: Speakeasy
  slug: speakeasy
  spec_type: OpenAPI
  url: https://www.speakeasy.com/openapi.yaml
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
description: FinOps framework definition for the Speakeasy API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Speakeasy
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Speakeasy
  PublisherName: Speakeasy
  ServiceCategory: Developer Tools / API
  ServiceName: Speakeasy
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
name: Speakeasy Finops
provider_name: Speakeasy
provider_slug: speakeasy
publisher_name: Speakeasy
service_category: API
slug: speakeasy-finops
source_filename: speakeasy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Speakeasy\nproviderId: speakeasy\npublisherName: Speakeasy\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Documentation\n  - MCP\n  - Platform\n  - SDKs\n  - Terraform\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Speakeasy API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Speakeasy\n  ServiceCategory: Developer Tools / API\n  ProviderName: Speakeasy\n  PublisherName: Speakeasy\n  InvoiceIssuerName: Speakeasy\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Speakeasy\n    baseURL: https://api.prod.speakeasy.com\n    tags:\n      - AI\n      - Documentation\n      - MCP\n      - Platform\n      - SDKs\n      - Terraform\n      - Testing\n    serviceName: Speakeasy\n    serviceCategory: API\n  - name: Speakeasy SDK Generation\n    baseURL: ''\n    tags:\n      - Code Generation\n      - OpenAPI\n      - SDKs\n    serviceName: Speakeasy SDK Generation\n    serviceCategory: API\n  - name: Speakeasy Terraform Generation\n    baseURL: ''\n    tags:\n      - Code Generation\n      - Infrastructure as Code\n      - OpenAPI\n      - Terraform\n    serviceName: Speakeasy Terraform Generation\n    serviceCategory: API\n  - name: Speakeasy MCP Server Generation\n\
  \    baseURL: ''\n    tags:\n      - Agents\n      - AI\n      - Code Generation\n      - MCP\n      - OpenAPI\n    serviceName: Speakeasy MCP Server Generation\n    serviceCategory: API\n  - name: Speakeasy DocsMD\n    baseURL: ''\n    tags:\n      - API Reference\n      - Documentation\n      - OpenAPI\n    serviceName: Speakeasy DocsMD\n    serviceCategory: API\n  - name: Speakeasy Contract Testing\n    baseURL: ''\n    tags:\n      - Contract Testing\n      - OpenAPI\n      - SDKs\n      - Testing\n    serviceName: Speakeasy Contract Testing\n    serviceCategory: API\n  - name: Speakeasy React Query Hooks\n    baseURL: ''\n    tags:\n      - Frontend\n      - React\n      - SDKs\n      - TypeScript\n    serviceName: Speakeasy React Query Hooks\n    serviceCategory: API\n  - name: Speakeasy Gram\n    baseURL: ''\n    tags:\n      - Agents\n      - AI\n      - Cloud\n      - MCP\n      - Platform\n    serviceName: Speakeasy Gram\n    serviceCategory: API\nunitEconomics:\n  - name: Cost\
  \ per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/speakeasy/refs/heads/main/finops/speakeasy-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Documentation
- MCP
- Platform
- SDKs
- Terraform
- Testing
- FinOps
- Cost Management
- FOCUS
---
