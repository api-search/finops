---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: appium-server-openapi.yaml
  format: yaml
  label: Appium Server API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appium/refs/heads/main/openapi/appium-server-openapi.yaml
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
description: FinOps framework definition for the Appium API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Appium
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Appium
  PublisherName: Appium
  ServiceCategory: Developer Tools / API
  ServiceName: Appium
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
name: Appium Finops
provider_name: Appium
provider_slug: appium
publisher_name: Appium
service_category: API
slug: appium-finops
source_filename: appium-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Appium\nproviderId: appium\npublisherName: Appium\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Android\n  - Cross-Platform\n  - iOS\n  - Mobile Testing\n  - Open Source\n  - OpenJS Foundation\n  - Test Automation\n  - WebDriver\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Appium API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Appium\n  ServiceCategory: Developer Tools / API\n  ProviderName: Appium\n  PublisherName: Appium\n  InvoiceIssuerName: Appium\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Appium Server API\n    baseURL: http://localhost:4723\n    tags:\n      - Android\n      - Automation\n      - iOS\n      - Mobile Testing\n      - WebDriver\n    serviceName: Appium Server API\n    serviceCategory: API\n  - name: Appium Inspector\n    baseURL: https://github.com/appium/appium-inspector/releases\n    tags:\n      - Debugging\n      - GUI\n      - Inspector\n      - Mobile Testing\n    serviceName: Appium Inspector\n    serviceCategory: API\n  - name: Appium UiAutomator2 Driver\n    baseURL: http://localhost:4723\n    tags:\n      - Android\n      - Automation\n      - Driver\n      - Mobile Testing\n    serviceName: Appium UiAutomator2 Driver\n    serviceCategory:\
  \ API\n  - name: Appium XCUITest Driver\n    baseURL: http://localhost:4723\n    tags:\n      - Automation\n      - Driver\n      - iOS\n      - Mobile Testing\n      - tvOS\n    serviceName: Appium XCUITest Driver\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Appium Contributors\n    email: appium@googlegroups.com\n    url: https://github.com/appium/appium/graphs/contributors\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appium/refs/heads/main/finops/appium-finops.yml
sources: []
specification: FinOps Framework
tags:
- Android
- Cross-Platform
- iOS
- Mobile Testing
- Open Source
- OpenJS Foundation
- Test Automation
- WebDriver
- FinOps
- Cost Management
- FOCUS
---
