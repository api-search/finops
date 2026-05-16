---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Postman Collections API
  slug: postman-collections-api
  spec_type: OpenAPI
  url: https://www.postman.com/postman/postman-public-workspace/
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
description: FinOps framework definition for the Test Suites API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Test Suites
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Test Suites
  PublisherName: Test Suites
  ServiceCategory: Developer Tools / API
  ServiceName: Test Suites
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
name: Test Suites Finops
provider_name: Test Suites
provider_slug: test-suites
publisher_name: Test Suites
service_category: API
slug: test-suites-finops
source_filename: test-suites-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Test Suites\nproviderId: test-suites\npublisherName: Test Suites\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - API Testing\n  - Collections\n  - Quality Assurance\n  - Software Development\n  - Test Management\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Test Suites API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Test Suites\n  ServiceCategory: Developer Tools / API\n  ProviderName: Test Suites\n  PublisherName: Test Suites\n  InvoiceIssuerName: Test Suites\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Postman Collections API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Collections\n      - API Testing\n      - Test Management\n    serviceName: Postman Collections API\n    serviceCategory: API\n  - name: JUnit 5\n    baseURL: https://junit.org/junit5/\n    tags:\n      - Java\n      - Test Suite\n      - Unit Testing\n    serviceName: JUnit 5\n    serviceCategory: API\n  - name: pytest\n    baseURL: https://pytest.org/\n    tags:\n      - Python\n      - Test Suite\n      - Testing\n    serviceName: pytest\n    serviceCategory: API\n  - name: Jasmine\n    baseURL: https://jasmine.github.io/\n    tags:\n      - BDD\n      - JavaScript\n      - Test\
  \ Suite\n    serviceName: Jasmine\n    serviceCategory: API\n  - name: Mocha\n    baseURL: https://mochajs.org/\n    tags:\n      - JavaScript\n      - Node.js\n      - Test Suite\n    serviceName: Mocha\n    serviceCategory: API\n  - name: Jest\n    baseURL: https://jestjs.io/\n    tags:\n      - JavaScript\n      - React\n      - Test Suite\n    serviceName: Jest\n    serviceCategory: API\n  - name: Bruno\n    baseURL: https://www.usebruno.com/\n    tags:\n      - API Testing\n      - Collections\n      - Open Source\n    serviceName: Bruno\n    serviceCategory: API\n  - name: Hurl\n    baseURL: https://hurl.dev/\n    tags:\n      - API Testing\n      - CLI\n      - Test Suite\n    serviceName: Hurl\n    serviceCategory: API\n  - name: TestNG\n    baseURL: https://testng.org/\n    tags:\n      - Java\n      - Test Suite\n      - Integration Testing\n    serviceName: TestNG\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests\
  \ / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/test-suites/refs/heads/main/finops/test-suites-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Testing
- Collections
- Quality Assurance
- Software Development
- Test Management
- Testing
- FinOps
- Cost Management
- FOCUS
---
