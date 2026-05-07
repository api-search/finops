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
description: FinOps framework definition for the Angular 18 API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Angular 18
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Angular 18
  PublisherName: Angular 18
  ServiceCategory: Developer Tools / API
  ServiceName: Angular 18
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
name: Angular 18 Finops
provider_name: Angular 18
provider_slug: angular-18
publisher_name: Angular 18
service_category: API
slug: angular-18-finops
source_filename: angular-18-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Angular 18\nproviderId: angular-18\npublisherName: Angular 18\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Framework\n  - Frontend\n  - JavaScript\n  - Material 3\n  - Open Source\n  - Signals\n  - Single Page Application\n  - TypeScript\n  - Web Development\n  - Zoneless\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Angular 18 API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Angular 18\n  ServiceCategory: Developer Tools / API\n  ProviderName: Angular 18\n  PublisherName: Angular 18\n  InvoiceIssuerName: Angular 18\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Angular 18 Core API\n    baseURL: https://angular.dev/api/core\n    tags:\n      - Change Detection\n      - Components\n      - Decorators\n      - Dependency Injection\n      - Framework\n      - Signals\n      - Standalone Components\n      - TypeScript\n      - Zoneless\n    serviceName: Angular 18 Core API\n    serviceCategory: API\n  - name: Angular 18 Common API\n    baseURL: https://angular.dev/api/common\n    tags:\n      - Directives\n      - Pipes\n      - Utilities\n    serviceName: Angular 18 Common API\n    serviceCategory: API\n  - name: Angular 18 Router API\n    baseURL: https://angular.dev/api/router\n\
  \    tags:\n      - Guards\n      - Navigation\n      - Routing\n    serviceName: Angular 18 Router API\n    serviceCategory: API\n  - name: Angular 18 Forms API\n    baseURL: https://angular.dev/api/forms\n    tags:\n      - Forms\n      - Reactive Forms\n      - Typed Forms\n      - Validation\n    serviceName: Angular 18 Forms API\n    serviceCategory: API\n  - name: Angular 18 HTTP Client API\n    baseURL: https://angular.dev/api/common/http\n    tags:\n      - HTTP\n      - Interceptors\n      - REST\n    serviceName: Angular 18 HTTP Client API\n    serviceCategory: API\n  - name: Angular 18 Platform Server API\n    baseURL: https://angular.dev/api/platform-server\n    tags:\n      - Hydration\n      - SSR\n      - Server-Side Rendering\n    serviceName: Angular 18 Platform Server API\n    serviceCategory: API\n  - name: Angular 18 CDK API\n    baseURL: https://material.angular.io/cdk\n    tags:\n      - Accessibility\n      - CDK\n      - Components\n    serviceName: Angular 18 CDK\
  \ API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/angular-18/refs/heads/main/finops/angular-18-finops.yml
sources: []
specification: FinOps Framework
tags:
- Framework
- Frontend
- JavaScript
- Material 3
- Open Source
- Signals
- Single Page Application
- TypeScript
- Web Development
- Zoneless
- FinOps
- Cost Management
- FOCUS
---
