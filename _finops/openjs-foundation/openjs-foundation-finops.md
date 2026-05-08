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
description: FinOps framework definition for the OpenJS Foundation API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenJS Foundation
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: OpenJS Foundation
  PublisherName: OpenJS Foundation
  ServiceCategory: Developer Tools / API
  ServiceName: OpenJS Foundation
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
name: Openjs Foundation Finops
provider_name: OpenJS Foundation
provider_slug: openjs-foundation
publisher_name: OpenJS Foundation
service_category: API
slug: openjs-foundation-finops
source_filename: openjs-foundation-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: OpenJS Foundation\nproviderId: openjs-foundation\npublisherName: OpenJS Foundation\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - JavaScript\n  - Linux Foundation\n  - Node.js\n  - Web\n  - API Frameworks\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the OpenJS Foundation API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: OpenJS Foundation\n  ServiceCategory: Developer Tools / API\n  ProviderName: OpenJS Foundation\n  PublisherName: OpenJS Foundation\n  InvoiceIssuerName: OpenJS Foundation\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Node.js\n    baseURL: ''\n    tags:\n      - Runtime\n      - JavaScript\n      - Server-side\n    serviceName: Node.js\n    serviceCategory: API\n  - name: Express\n    baseURL: ''\n    tags:\n      - Web Framework\n      - HTTP\n      - APIs\n    serviceName: Express\n    serviceCategory: API\n  - name: Fastify\n    baseURL: ''\n    tags:\n      - Web Framework\n      - JSON Schema\n      - APIs\n    serviceName: Fastify\n    serviceCategory: API\n  - name: LoopBack\n    baseURL: ''\n    tags:\n      - API Framework\n      - TypeScript\n      - OpenAPI\n    serviceName: LoopBack\n    serviceCategory: API\n  - name: Electron\n    baseURL:\
  \ ''\n    tags:\n      - Desktop\n      - Cross-platform\n    serviceName: Electron\n    serviceCategory: API\n  - name: Appium\n    baseURL: ''\n    tags:\n      - Test Automation\n      - WebDriver\n      - Mobile\n    serviceName: Appium\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openjs-foundation/refs/heads/main/finops/openjs-foundation-finops.yml
sources: []
specification: FinOps Framework
tags:
- JavaScript
- Linux Foundation
- Node.js
- Web
- API Frameworks
- FinOps
- Cost Management
- FOCUS
---
