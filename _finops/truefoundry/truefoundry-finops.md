---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: truefoundry-ai-gateway-openapi.yml
  format: yaml
  label: TrueFoundry AI Gateway API
  slug: truefoundry-ai-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truefoundry/refs/heads/main/openapi/truefoundry-ai-gateway-openapi.yml
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
description: FinOps framework definition for the TrueFoundry API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: TrueFoundry
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: TrueFoundry
  PublisherName: TrueFoundry
  ServiceCategory: Developer Tools / API
  ServiceName: TrueFoundry
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
name: Truefoundry Finops
provider_name: TrueFoundry
provider_slug: truefoundry
publisher_name: TrueFoundry
service_category: API
slug: truefoundry-finops
source_filename: truefoundry-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TrueFoundry\nproviderId: truefoundry\npublisherName: TrueFoundry\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI Platform\n  - Enterprise AI\n  - Kubernetes\n  - LLM Gateway\n  - MLOps\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the TrueFoundry API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: TrueFoundry\n  ServiceCategory: Developer Tools / API\n  ProviderName: TrueFoundry\n  PublisherName: TrueFoundry\n  InvoiceIssuerName: TrueFoundry\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: TrueFoundry AI Gateway API\n    baseURL: https://gateway.truefoundry.ai/api/llm\n    tags:\n      - AI Gateway\n      - Chat Completions\n      - Embeddings\n      - LLM\n    serviceName: TrueFoundry AI Gateway API\n    serviceCategory: API\n  - name: TrueFoundry MCP Gateway API\n    baseURL: https://gateway.truefoundry.ai\n    tags:\n      - Agent Tools\n      - AI Agents\n      - MCP\n      - Tool Registry\n    serviceName: TrueFoundry MCP Gateway API\n    serviceCategory: API\n  - name: TrueFoundry Platform API\n    baseURL: https://app.truefoundry.com/api\n    tags:\n      - Deployments\n      - Management\n      - MLOps\n      - Platform\n    serviceName: TrueFoundry Platform\
  \ API\n    serviceCategory: API\n  - name: TrueFoundry Model Serving API\n    baseURL: https://app.truefoundry.com\n    tags:\n      - Kubernetes\n      - LLM Inference\n      - MLOps\n      - Model Serving\n    serviceName: TrueFoundry Model Serving API\n    serviceCategory: API\n  - name: TrueFoundry Model Registry API\n    baseURL: https://app.truefoundry.com\n    tags:\n      - Machine Learning\n      - MLOps\n      - Model Registry\n      - Versioning\n    serviceName: TrueFoundry Model Registry API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/truefoundry/refs/heads/main/finops/truefoundry-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI Platform
- Enterprise AI
- Kubernetes
- LLM Gateway
- MLOps
- FinOps
- Cost Management
- FOCUS
---
