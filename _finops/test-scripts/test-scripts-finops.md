---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 72a32ca1-f3a2-4a5e-91f2-token
  format: yaml
  label: Postman API
  slug: ''
  spec_type: OpenAPI
  url: https://www.postman.com/postman/postman-public-workspace/api/72a32ca1-f3a2-4a5e-91f2-token
- filename: openapi.yaml
  format: yaml
  label: k6 Performance Testing
  slug: ''
  spec_type: OpenAPI
  url: https://grafana.com/docs/k6/latest/misc/k6-rest-api/
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
description: FinOps framework definition for the Test Scripts API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Test Scripts
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Test Scripts
  PublisherName: Test Scripts
  ServiceCategory: Developer Tools / API
  ServiceName: Test Scripts
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
name: Test Scripts Finops
provider_name: Test Scripts
provider_slug: test-scripts
publisher_name: Test Scripts
service_category: API
slug: test-scripts-finops
source_filename: test-scripts-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Test Scripts\nproviderId: test-scripts\npublisherName: Test Scripts\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Automation\n  - CI/CD\n  - Contract Testing\n  - Quality Assurance\n  - Software Development\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Test Scripts API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Test Scripts\n  ServiceCategory: Developer Tools / API\n  ProviderName: Test Scripts\n  PublisherName: Test Scripts\n  InvoiceIssuerName: Test Scripts\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API\
  \ responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Postman API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Testing\n      - Collections\n      - Test Execution\n    serviceName: Postman API\n    serviceCategory: API\n  - name: Newman CLI\n    baseURL: https://github.com/postmanlabs/newman\n    tags:\n      - CLI\n      - CI/CD\n      - Test Execution\n    serviceName: Newman CLI\n    serviceCategory: API\n  - name: Karate API Testing Framework\n    baseURL: https://karatelabs.github.io/karate/\n    tags:\n      - BDD\n      - Gherkin\n      - API Testing\n      - Test Automation\n    serviceName: Karate API Testing Framework\n    serviceCategory: API\n  - name: REST Assured\n    baseURL:\
  \ https://rest-assured.io/\n    tags:\n      - Java\n      - BDD\n      - REST\n      - Test Automation\n    serviceName: REST Assured\n    serviceCategory: API\n  - name: Dredd API Testing Framework\n    baseURL: https://dredd.org/\n    tags:\n      - Contract Testing\n      - OpenAPI\n      - Test Automation\n    serviceName: Dredd API Testing Framework\n    serviceCategory: API\n  - name: k6 Performance Testing\n    baseURL: https://api.k6.io\n    tags:\n      - Load Testing\n      - Performance Testing\n      - JavaScript\n      - Test Automation\n    serviceName: k6 Performance Testing\n    serviceCategory: API\n  - name: Playwright Test\n    baseURL: https://playwright.dev/\n    tags:\n      - End-to-End Testing\n      - Browser Automation\n      - JavaScript\n      - Test Automation\n    serviceName: Playwright Test\n    serviceCategory: API\n  - name: Cypress\n    baseURL: https://www.cypress.io/\n    tags:\n      - End-to-End Testing\n      - JavaScript\n      - Test Automation\n\
  \    serviceName: Cypress\n    serviceCategory: API\n  - name: Schemathesis\n    baseURL: https://schemathesis.io/\n    tags:\n      - Property-Based Testing\n      - OpenAPI\n      - Fuzz Testing\n    serviceName: Schemathesis\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/test-scripts/refs/heads/main/finops/test-scripts-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- CI/CD
- Contract Testing
- Quality Assurance
- Software Development
- Testing
- FinOps
- Cost Management
- FOCUS
---
