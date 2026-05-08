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
description: FinOps framework definition for the Redux API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Redux
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Redux
  PublisherName: Redux
  ServiceCategory: Developer Tools / API
  ServiceName: Redux
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
name: Redux Finops
provider_name: Redux
provider_slug: redux
publisher_name: Redux
service_category: API
slug: redux-finops
source_filename: redux-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Redux\nproviderId: redux\npublisherName: Redux\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Flux Architecture\n  - Frontend\n  - Javascript\n  - Predictable State\n  - React\n  - State Management\n  - Typescript\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Redux API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Redux\n  ServiceCategory: Developer Tools / API\n  ProviderName: Redux\n  PublisherName: Redux\n  InvoiceIssuerName: Redux\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Redux Core API\n    baseURL: https://redux.js.org\n    tags:\n      - Actions\n      - Middleware\n      - Reducers\n      - State Management\n      - Store\n    serviceName: Redux Core API\n    serviceCategory: API\n  - name: React Redux API\n    baseURL: https://react-redux.js.org\n    tags:\n      - Bindings\n      - Components\n      - Hooks\n      - React\n      - State Management\n    serviceName: React Redux API\n    serviceCategory: API\n  - name: Redux Toolkit API\n    baseURL: https://redux-toolkit.js.org\n    tags:\n      - Code Generation\n      - Immer\n      - Redux Toolkit\n      - Rtk Query\n      - Simplified Redux\n      - Toolkit\n    serviceName: Redux Toolkit\
  \ API\n    serviceCategory: API\n  - name: Redux DevTools API\n    baseURL: https://github.com/reduxjs/redux-devtools\n    tags:\n      - Browser Extension\n      - Debugging\n      - Devtools\n      - Time Travel\n    serviceName: Redux DevTools API\n    serviceCategory: API\n  - name: Redux Saga\n    baseURL: https://redux-saga.js.org\n    tags:\n      - Async\n      - Generators\n      - Middleware\n      - Side Effects\n    serviceName: Redux Saga\n    serviceCategory: API\n  - name: Redux Observable\n    baseURL: https://redux-observable.js.org\n    tags:\n      - Middleware\n      - Observables\n      - Reactive\n      - Rxjs\n    serviceName: Redux Observable\n    serviceCategory: API\n  - name: Redux Thunk\n    baseURL: https://github.com/reduxjs/redux-thunk\n    tags:\n      - Async\n      - Middleware\n      - Thunk\n    serviceName: Redux Thunk\n    serviceCategory: API\n  - name: Reselect\n    baseURL: https://github.com/reduxjs/reselect\n    tags:\n      - Memoization\n  \
  \    - Performance\n      - Selectors\n    serviceName: Reselect\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/redux/refs/heads/main/finops/redux-finops.yml
sources: []
specification: FinOps Framework
tags:
- Flux Architecture
- Frontend
- Javascript
- Predictable State
- React
- State Management
- Typescript
- FinOps
- Cost Management
- FOCUS
---
