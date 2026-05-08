---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: anthropic-messages-api-openapi.yml
  format: yaml
  label: Anthropic Messages API
  slug: anthropic-messages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-messages-api-openapi.yml
- filename: anthropic-models-api-openapi.yml
  format: yaml
  label: Anthropic Models API
  slug: anthropic-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-models-api-openapi.yml
- filename: anthropic-message-batches-api-openapi.yml
  format: yaml
  label: Anthropic Message Batches API
  slug: anthropic-message-batches-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-message-batches-api-openapi.yml
- filename: anthropic-files-api-openapi.yml
  format: yaml
  label: Anthropic Files API
  slug: anthropic-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-files-api-openapi.yml
- filename: anthropic-admin-api-openapi.yml
  format: yaml
  label: Anthropic Admin API
  slug: anthropic-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-admin-api-openapi.yml
- filename: anthropic-prompts-api-openapi.yml
  format: yaml
  label: Anthropic Prompts API
  slug: anthropic-prompts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/openapi/anthropic-prompts-api-openapi.yml
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
description: FinOps framework definition for the Anthropic API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Anthropic
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Anthropic
  PublisherName: Anthropic
  ServiceCategory: Developer Tools / API
  ServiceName: Anthropic
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
name: Anthropic Finops
provider_name: Anthropic
provider_slug: anthropic
publisher_name: Anthropic
service_category: API
slug: anthropic-finops
source_filename: anthropic-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Anthropic\nproviderId: anthropic\npublisherName: Anthropic\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Artificial Intelligence\n  - Claude\n  - Foundation Models\n  - Large Language Models\n  - Machine Learning\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Anthropic API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Anthropic\n  ServiceCategory: Developer Tools / API\n  ProviderName: Anthropic\n  PublisherName: Anthropic\n  InvoiceIssuerName: Anthropic\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Anthropic Messages API\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Messages\n    serviceName: Anthropic Messages API\n    serviceCategory: API\n  - name: Anthropic Models API\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Models\n    serviceName: Anthropic Models API\n    serviceCategory: API\n  - name: Anthropic Message Batches API\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Batches\n      - Messages\n    serviceName: Anthropic Message Batches API\n    serviceCategory: API\n  - name: Anthropic Files API\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial\
  \ Intelligence\n      - Files\n    serviceName: Anthropic Files API\n    serviceCategory: API\n  - name: Anthropic Admin API\n    baseURL: ''\n    tags:\n      - Administrative\n      - AI\n      - Artificial Intelligence\n    serviceName: Anthropic Admin API\n    serviceCategory: API\n  - name: Anthropic Prompts API\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Prompts\n    serviceName: Anthropic Prompts API\n    serviceCategory: API\n  - name: Anthropic Token Counting API\n    baseURL: ''\n    tags:\n      - AI\n      - Artificial Intelligence\n      - Counting\n      - Tokens\n    serviceName: Anthropic Token Counting API\n    serviceCategory: API\n  - name: Anthropic Skills API\n    baseURL: ''\n    tags:\n      - Agents\n      - AI\n      - Artificial Intelligence\n      - Skills\n    serviceName: Anthropic Skills API\n    serviceCategory: API\n  - name: Anthropic Usage & Cost API\n    baseURL: ''\n    tags:\n      - Administration\n      - AI\n\
  \      - Artificial Intelligence\n      - Cost\n      - Usage\n    serviceName: Anthropic Usage & Cost API\n    serviceCategory: API\n  - name: Anthropic Claude Code Analytics API\n    baseURL: ''\n    tags:\n      - Administration\n      - AI\n      - Analytics\n      - Artificial Intelligence\n      - Claude Code\n    serviceName: Anthropic Claude Code Analytics API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n    X: apievangelist\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/anthropic/refs/heads/main/finops/anthropic-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Artificial Intelligence
- Claude
- Foundation Models
- Large Language Models
- Machine Learning
- FinOps
- Cost Management
- FOCUS
---
