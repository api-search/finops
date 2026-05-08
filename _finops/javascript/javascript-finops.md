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
description: FinOps framework definition for the JavaScript API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: JavaScript
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: JavaScript
  PublisherName: JavaScript
  ServiceCategory: Developer Tools / API
  ServiceName: JavaScript
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
name: Javascript Finops
provider_name: JavaScript
provider_slug: javascript
publisher_name: JavaScript
service_category: API
slug: javascript-finops
source_filename: javascript-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: JavaScript\nproviderId: javascript\npublisherName: JavaScript\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Browser\n  - ECMAScript\n  - JavaScript\n  - Programming Language\n  - Web APIs\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the JavaScript API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: JavaScript\n  ServiceCategory: Developer Tools / API\n  ProviderName: JavaScript\n  PublisherName: JavaScript\n  InvoiceIssuerName: JavaScript\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Fetch API\n    baseURL: ''\n    tags:\n      - AJAX\n      - Async\n      - HTTP\n      - Network\n    serviceName: Fetch API\n    serviceCategory: API\n  - name: Web Storage API\n    baseURL: ''\n    tags:\n      - Browser\n      - Client-side\n      - Storage\n    serviceName: Web Storage API\n    serviceCategory: API\n  - name: Web Audio API\n    baseURL: ''\n    tags:\n      - Audio\n      - Media\n      - Sound\n    serviceName: Web Audio API\n    serviceCategory: API\n  - name: Canvas API\n    baseURL: ''\n    tags:\n      - 2D\n      - Drawing\n      - Graphics\n    serviceName: Canvas API\n    serviceCategory: API\n  - name: WebSockets API\n    baseURL: ''\n    tags:\n   \
  \   - Bidirectional\n      - Communication\n      - Real-time\n      - WebSocket\n    serviceName: WebSockets API\n    serviceCategory: API\n  - name: Geolocation API\n    baseURL: ''\n    tags:\n      - GPS\n      - Location\n      - Position\n    serviceName: Geolocation API\n    serviceCategory: API\n  - name: Notifications API\n    baseURL: ''\n    tags:\n      - Alerts\n      - Notifications\n      - User Interface\n    serviceName: Notifications API\n    serviceCategory: API\n  - name: IndexedDB API\n    baseURL: ''\n    tags:\n      - Client-side\n      - Database\n      - NoSQL\n      - Storage\n    serviceName: IndexedDB API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/javascript/refs/heads/main/finops/javascript-finops.yml
sources: []
specification: FinOps Framework
tags:
- Browser
- ECMAScript
- JavaScript
- Programming Language
- Web APIs
- FinOps
- Cost Management
- FOCUS
---
