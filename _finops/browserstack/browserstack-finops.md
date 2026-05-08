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
description: FinOps framework definition for the BrowserStack API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: BrowserStack
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: BrowserStack
  PublisherName: BrowserStack
  ServiceCategory: Developer Tools / API
  ServiceName: BrowserStack
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
name: Browserstack Finops
provider_name: BrowserStack
provider_slug: browserstack
publisher_name: BrowserStack
service_category: API
slug: browserstack-finops
source_filename: browserstack-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: BrowserStack\nproviderId: browserstack\npublisherName: BrowserStack\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Accessibility\n  - Appium\n  - Applications\n  - Automation\n  - CI/CD\n  - Cross-Browser Testing\n  - Enterprise\n  - JavaScript\n  - Low Code\n  - Mobile Testing\n  - QA\n  - Regression Testing\n  - Selenium\n  - Testing\n  - Unit Testing\n  - Visual Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the BrowserStack API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n\
  \    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting\
  \ for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: BrowserStack\n  ServiceCategory: Developer Tools / API\n  ProviderName: BrowserStack\n  PublisherName: BrowserStack\n  InvoiceIssuerName: BrowserStack\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: BrowserStack\n    baseURL: ''\n    tags: []\n    serviceName: BrowserStack\n    serviceCategory: API\n  - name: BrowserStack Automate API\n    baseURL: ''\n    tags:\n      - Automation\n      - Cross-Browser Testing\n      - Selenium\n      - Testing\n    serviceName: BrowserStack Automate API\n    serviceCategory: API\n  - name: BrowserStack App Automate API\n    baseURL: ''\n    tags:\n      - Appium\n      - Automation\n      - Espresso\n      - Mobile Testing\n      - XCUITest\n    serviceName:\
  \ BrowserStack App Automate API\n    serviceCategory: API\n  - name: BrowserStack Screenshots API\n    baseURL: ''\n    tags:\n      - Cross-Browser Testing\n      - Screenshots\n      - Visual Testing\n    serviceName: BrowserStack Screenshots API\n    serviceCategory: API\n  - name: BrowserStack App Live API\n    baseURL: ''\n    tags:\n      - Applications\n      - Mobile Testing\n    serviceName: BrowserStack App Live API\n    serviceCategory: API\n  - name: BrowserStack Local Testing API\n    baseURL: ''\n    tags:\n      - Debugging\n      - Local Testing\n      - Networking\n    serviceName: BrowserStack Local Testing API\n    serviceCategory: API\n  - name: BrowserStack Automate TurboScale API\n    baseURL: ''\n    tags:\n      - Automation\n      - Scaling\n      - Selenium\n    serviceName: BrowserStack Automate TurboScale API\n    serviceCategory: API\n  - name: BrowserStack Test Management API\n    baseURL: ''\n    tags:\n      - QA\n      - Test Management\n      - Testing\n\
  \    serviceName: BrowserStack Test Management API\n    serviceCategory: API\n  - name: BrowserStack Test Reporting and Analytics API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Observability\n      - Reporting\n      - Testing\n    serviceName: BrowserStack Test Reporting and Analytics API\n    serviceCategory: API\n  - name: BrowserStack Accessibility Testing API\n    baseURL: ''\n    tags:\n      - Accessibility\n      - Testing\n      - WCAG\n    serviceName: BrowserStack Accessibility Testing API\n    serviceCategory: API\n  - name: BrowserStack Percy API\n    baseURL: ''\n    tags:\n      - Regression Testing\n      - Screenshots\n      - Visual Testing\n    serviceName: BrowserStack Percy API\n    serviceCategory: API\n  - name: BrowserStack App Percy API\n    baseURL: ''\n    tags:\n      - Mobile Testing\n      - Regression Testing\n      - Visual Testing\n    serviceName: BrowserStack App Percy API\n    serviceCategory: API\n  - name: BrowserStack User Management\
  \ API\n    baseURL: ''\n    tags:\n      - Administration\n      - Enterprise\n      - User Management\n    serviceName: BrowserStack User Management API\n    serviceCategory: API\n  - name: BrowserStack JavaScript Testing API\n    baseURL: ''\n    tags:\n      - Cross-Browser Testing\n      - JavaScript\n      - Testing\n      - Unit Testing\n    serviceName: BrowserStack JavaScript Testing API\n    serviceCategory: API\n  - name: BrowserStack App Accessibility Testing API\n    baseURL: ''\n    tags:\n      - Accessibility\n      - Mobile Testing\n      - Testing\n    serviceName: BrowserStack App Accessibility Testing API\n    serviceCategory: API\n  - name: BrowserStack Low Code Automation API\n    baseURL: ''\n    tags:\n      - Automation\n      - CI/CD\n      - Low Code\n      - Testing\n    serviceName: BrowserStack Low Code Automation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n\
  \  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - name: BrowserStack\n    email: support@browserstack.com\n    url: https://www.browserstack.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/browserstack/refs/heads/main/finops/browserstack-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accessibility
- Appium
- Applications
- Automation
- CI/CD
- Cross-Browser Testing
- Enterprise
- JavaScript
- Low Code
- Mobile Testing
- QA
- Regression Testing
- Selenium
- Testing
- Unit Testing
- Visual Testing
- FinOps
- Cost Management
- FOCUS
---
