---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: split-admin-api-openapi.yml
  format: yaml
  label: Split Admin API
  slug: split-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/openapi/split-admin-api-openapi.yml
- filename: split-feature-flag-api-openapi.yml
  format: yaml
  label: Split Feature Flag API
  slug: split-feature-flag-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/openapi/split-feature-flag-api-openapi.yml
- filename: split-evaluator-api-openapi.yml
  format: yaml
  label: Split Evaluator API
  slug: split-evaluator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/openapi/split-evaluator-api-openapi.yml
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
description: FinOps framework definition for the Split API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Split
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Split
  PublisherName: Split
  ServiceCategory: Developer Tools / API
  ServiceName: Split
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
name: Split Finops
provider_name: Split
provider_slug: split
publisher_name: Split
service_category: API
slug: split-finops
source_filename: split-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Split\nproviderId: split\npublisherName: Split\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Experimentation\n  - Feature Flags\n  - Feature Management\n  - Rollouts\n  - SDKs\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Split API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Split\n  ServiceCategory: Developer Tools / API\n  ProviderName: Split\n  PublisherName: Split\n  InvoiceIssuerName: Split\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n  \
  \    - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Split Admin API\n    baseURL: ''\n    tags:\n      - Administration\n      - Experimentation\n      - Feature Flags\n      - Feature Management\n    serviceName: Split Admin API\n    serviceCategory: API\n  - name: Split Feature Flag API\n    baseURL: ''\n    tags:\n      - Feature Flags\n      - Rollouts\n      - Targeting\n      - Treatments\n    serviceName: Split Feature Flag API\n    serviceCategory: API\n  - name: Split Evaluator API\n    baseURL: ''\n    tags:\n      - Evaluation\n      - Feature Flags\n      - Microservices\n      - Treatments\n    serviceName: Split Evaluator API\n    serviceCategory: API\n  - name: Split JavaScript SDK\n    baseURL: ''\n    tags:\n      - Browser\n      - Feature Flags\n    \
  \  - JavaScript\n      - SDK\n    serviceName: Split JavaScript SDK\n    serviceCategory: API\n  - name: Split Node.js SDK\n    baseURL: ''\n    tags:\n      - Feature Flags\n      - Node.js\n      - SDK\n      - Server Side\n    serviceName: Split Node.js SDK\n    serviceCategory: API\n  - name: Split Java SDK\n    baseURL: ''\n    tags:\n      - Feature Flags\n      - Java\n      - SDK\n      - Server Side\n    serviceName: Split Java SDK\n    serviceCategory: API\n  - name: Split Python SDK\n    baseURL: ''\n    tags:\n      - Feature Flags\n      - Python\n      - SDK\n      - Server Side\n    serviceName: Split Python SDK\n    serviceCategory: API\n  - name: Split React SDK\n    baseURL: ''\n    tags:\n      - Feature Flags\n      - Frontend\n      - JavaScript\n      - React\n      - SDK\n    serviceName: Split React SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active\
  \ Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/finops/split-finops.yml
sources: []
specification: FinOps Framework
tags:
- Experimentation
- Feature Flags
- Feature Management
- Rollouts
- SDKs
- FinOps
- Cost Management
- FOCUS
---
