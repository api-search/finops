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
  label: OpenRouter
  slug: openrouter
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Chat Completions API
  slug: chat-completions-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Models API
  slug: models-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Generation API
  slug: generation-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
- filename: openapi.json
  format: json
  label: OpenRouter Keys Management API
  slug: keys-api
  spec_type: OpenAPI
  url: https://openrouter.ai/openapi.json
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
description: FinOps framework definition for the OpenRouter API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenRouter
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: OpenRouter
  PublisherName: OpenRouter
  ServiceCategory: Developer Tools / API
  ServiceName: OpenRouter
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
name: Openrouter Finops
provider_name: OpenRouter
provider_slug: openrouter
publisher_name: OpenRouter
service_category: API
slug: openrouter-finops
source_filename: openrouter-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: OpenRouter\nproviderId: openrouter\npublisherName: OpenRouter\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Artificial Intelligence\n  - Gateway\n  - Large Language Models\n  - Router\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the OpenRouter API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: OpenRouter\n  ServiceCategory: Developer Tools / API\n  ProviderName: OpenRouter\n  PublisherName: OpenRouter\n  InvoiceIssuerName: OpenRouter\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpenRouter\n    baseURL: https://openrouter.ai/api/v1\n    tags:\n      - Artificial Intelligence\n      - Gateway\n      - Large Language Models\n      - Router\n    serviceName: OpenRouter\n    serviceCategory: API\n  - name: OpenRouter Chat Completions API\n    baseURL: https://openrouter.ai/api/v1\n    tags:\n      - Chat\n      - Completions\n      - Large Language Models\n    serviceName: OpenRouter Chat Completions API\n    serviceCategory: API\n  - name: OpenRouter Models API\n    baseURL: https://openrouter.ai/api/v1\n    tags:\n      - Discovery\n      - Models\n    serviceName: OpenRouter Models API\n    serviceCategory: API\n  - name: OpenRouter Generation API\n    baseURL:\
  \ https://openrouter.ai/api/v1\n    tags:\n      - Generation\n      - Stats\n      - Usage\n    serviceName: OpenRouter Generation API\n    serviceCategory: API\n  - name: OpenRouter Keys Management API\n    baseURL: https://openrouter.ai/api/v1\n    tags:\n      - API Keys\n      - Management\n      - Provisioning\n    serviceName: OpenRouter Keys Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openrouter/refs/heads/main/finops/openrouter-finops.yml
sources: []
specification: FinOps Framework
tags:
- Artificial Intelligence
- Gateway
- Large Language Models
- Router
- FinOps
- Cost Management
- FOCUS
---
