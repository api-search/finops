---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: Helicone
  slug: helicone
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: ai-gateway.openapi.json
  format: json
  label: Helicone AI Gateway API
  slug: ai-gateway-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/ai-gateway.openapi.json
- filename: swagger.json
  format: json
  label: Helicone Request API
  slug: request-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Prompt API
  slug: prompt-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Experiment API
  slug: experiment-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Evals API
  slug: evals-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Session API
  slug: session-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone User API
  slug: user-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Webhook API
  slug: webhook-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Model Registry API
  slug: model-registry-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Trace API
  slug: trace-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Dashboard API
  slug: dashboard-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Property API
  slug: property-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
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
description: FinOps framework definition for the Helicone API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Helicone
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Helicone
  PublisherName: Helicone
  ServiceCategory: Developer Tools / API
  ServiceName: Helicone
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
name: Helicone Finops
provider_name: Helicone
provider_slug: helicone
publisher_name: Helicone
service_category: API
slug: helicone-finops
source_filename: helicone-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Helicone\nproviderId: helicone\npublisherName: Helicone\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI Gateways\n  - AI Monitoring\n  - Gateways\n  - LLM Observability\n  - LLM Routing\n  - Prompt Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Helicone API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Helicone\n  ServiceCategory: Developer Tools / API\n  ProviderName: Helicone\n  PublisherName: Helicone\n  InvoiceIssuerName: Helicone\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Helicone\n    baseURL: ''\n    tags:\n      - AI Gateways\n      - Gateways\n      - LLM Routing\n    serviceName: Helicone\n    serviceCategory: API\n  - name: Helicone AI Gateway API\n    baseURL: https://ai-gateway.helicone.ai\n    tags:\n      - AI Gateways\n      - AI Models\n      - Chat Completions\n      - LLM Routing\n    serviceName: Helicone AI Gateway API\n    serviceCategory: API\n  - name: Helicone Request API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Analytics\n      - LLM Observability\n      - Requests\n    serviceName: Helicone Request API\n    serviceCategory: API\n  - name: Helicone Prompt API\n    baseURL: https://api.helicone.ai\n    tags:\n\
  \      - Prompt Management\n      - Prompts\n      - Versioning\n    serviceName: Helicone Prompt API\n    serviceCategory: API\n  - name: Helicone Experiment API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Datasets\n      - Evaluations\n      - Experiments\n    serviceName: Helicone Experiment API\n    serviceCategory: API\n  - name: Helicone Evals API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Evaluations\n      - LLM Quality\n      - Scoring\n    serviceName: Helicone Evals API\n    serviceCategory: API\n  - name: Helicone Session API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Debugging\n      - Sessions\n      - Tracing\n    serviceName: Helicone Session API\n    serviceCategory: API\n  - name: Helicone User API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Analytics\n      - Metrics\n      - Users\n    serviceName: Helicone User API\n    serviceCategory: API\n  - name: Helicone Webhook API\n    baseURL: https://api.helicone.ai\n\
  \    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Helicone Webhook API\n    serviceCategory: API\n  - name: Helicone Model Registry API\n    baseURL: https://api.helicone.ai\n    tags:\n      - AI Models\n      - Models\n      - Registry\n    serviceName: Helicone Model Registry API\n    serviceCategory: API\n  - name: Helicone Trace API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Logging\n      - Observability\n      - Tracing\n    serviceName: Helicone Trace API\n    serviceCategory: API\n  - name: Helicone Dashboard API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Analytics\n      - Dashboard\n      - Scoring\n    serviceName: Helicone Dashboard API\n    serviceCategory: API\n  - name: Helicone Property API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Custom Properties\n      - Metadata\n      - Properties\n    serviceName: Helicone Property API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K\
  \ Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/helicone/refs/heads/main/finops/helicone-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI Gateways
- AI Monitoring
- Gateways
- LLM Observability
- LLM Routing
- Prompt Management
- FinOps
- Cost Management
- FOCUS
---
