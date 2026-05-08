---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: inflection-openapi.json
  format: json
  label: Inflection Chat API
  slug: inflection-chat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/openapi/inflection-openapi.json
- filename: inflection-openapi.json
  format: json
  label: Inflection Models API
  slug: inflection-models-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/openapi/inflection-openapi.json
- filename: inflection-openapi.json
  format: json
  label: Inflection Playground
  slug: inflection-playground
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/openapi/inflection-openapi.json
- filename: inflection-openapi.json
  format: json
  label: Inflection Usage API
  slug: inflection-usage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/openapi/inflection-openapi.json
- filename: inflection-openapi.json
  format: json
  label: Pi Personal AI
  slug: inflection-pi-app
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/openapi/inflection-openapi.json
- filename: inflection-openapi.json
  format: json
  label: Inflection for Enterprise
  slug: inflection-enterprise
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/openapi/inflection-openapi.json
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
description: FinOps framework definition for the Inflection AI API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Inflection AI
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Inflection AI
  PublisherName: Inflection AI
  ServiceCategory: Developer Tools / API
  ServiceName: Inflection AI
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
name: Inflection Finops
provider_name: Inflection AI
provider_slug: inflection
publisher_name: Inflection AI
service_category: API
slug: inflection-finops
source_filename: inflection-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Inflection AI\nproviderId: inflection\npublisherName: Inflection AI\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - LLM\n  - Personal AI\n  - Pi\n  - Foundation Models\n  - Empathetic AI\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Inflection AI API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Inflection AI\n  ServiceCategory: Developer Tools / API\n  ProviderName: Inflection AI\n  PublisherName: Inflection AI\n  InvoiceIssuerName: Inflection AI\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Inflection Chat API\n    baseURL: https://layercake.pubwestus3.inf7ks8.com\n    tags:\n      - Chat\n      - Completions\n      - LLM\n    serviceName: Inflection Chat API\n    serviceCategory: API\n  - name: Inflection Models API\n    baseURL: https://layercake.pubwestus3.inf7ks8.com\n    tags:\n      - Models\n      - Catalog\n    serviceName: Inflection Models API\n    serviceCategory: API\n  - name: Inflection Playground\n    baseURL: https://developers.inflection.ai\n    tags:\n      - Playground\n      - Testing\n    serviceName: Inflection Playground\n    serviceCategory: API\n  - name: Inflection Usage API\n    baseURL: https://developers.inflection.ai\n  \
  \  tags:\n      - Usage\n      - Metrics\n    serviceName: Inflection Usage API\n    serviceCategory: API\n  - name: Pi Personal AI\n    baseURL: https://pi.ai/\n    tags:\n      - Pi\n      - Consumer\n      - Personal AI\n    serviceName: Pi Personal AI\n    serviceCategory: API\n  - name: Inflection for Enterprise\n    baseURL: https://inflection.ai/\n    tags:\n      - Enterprise\n      - On-Prem\n      - Sovereign AI\n    serviceName: Inflection for Enterprise\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/inflection/refs/heads/main/finops/inflection-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- LLM
- Personal AI
- Pi
- Foundation Models
- Empathetic AI
- FinOps
- Cost Management
- FOCUS
---
