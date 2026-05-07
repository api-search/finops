---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api.github.com.json
  format: json
  label: GitHub Actions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: openapi.json
  format: json
  label: CircleCI API
  slug: ''
  spec_type: OpenAPI
  url: https://circleci.com/api/v2/openapi.json
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
description: FinOps framework definition for the Test-Driven Development API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Test-Driven Development
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Test-Driven Development
  PublisherName: Test-Driven Development
  ServiceCategory: Developer Tools / API
  ServiceName: Test-Driven Development
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
name: Test Driven Development Finops
provider_name: Test-Driven Development
provider_slug: test-driven-development
publisher_name: Test-Driven Development
service_category: API
slug: test-driven-development-finops
source_filename: test-driven-development-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Test-Driven Development\nproviderId: test-driven-development\npublisherName: Test-Driven Development\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Agile\n  - Best Practices\n  - Continuous Integration\n  - Extreme Programming\n  - Methodology\n  - Software Development\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Test-Driven Development API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Test-Driven Development\n  ServiceCategory: Developer Tools / API\n  ProviderName: Test-Driven Development\n  PublisherName: Test-Driven Development\n  InvoiceIssuerName: Test-Driven Development\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: GitHub Actions API\n    baseURL: https://api.github.com\n    tags:\n      - CI/CD\n      - Continuous Integration\n      - GitHub\n      - Test Automation\n    serviceName: GitHub Actions API\n    serviceCategory: API\n  - name: CircleCI API\n    baseURL: https://circleci.com/api/v2\n    tags:\n      - CI/CD\n      - Continuous Integration\n      - Pipelines\n      - Test Automation\n    serviceName: CircleCI API\n    serviceCategory: API\n  - name: Jenkins API\n    baseURL: https://your-jenkins.example.com\n    tags:\n      - Automation\n\
  \      - Build Management\n      - CI/CD\n      - Continuous Integration\n    serviceName: Jenkins API\n    serviceCategory: API\n  - name: SonarQube API\n    baseURL: https://your-sonar.example.com/api\n    tags:\n      - Code Coverage\n      - Code Quality\n      - Static Analysis\n      - Testing\n    serviceName: SonarQube API\n    serviceCategory: API\n  - name: Codecov API\n    baseURL: https://api.codecov.io/api/v2\n    tags:\n      - Code Coverage\n      - Reporting\n      - Testing\n    serviceName: Codecov API\n    serviceCategory: API\n  - name: Coveralls API\n    baseURL: https://coveralls.io\n    tags:\n      - Code Coverage\n      - Reporting\n      - Testing\n    serviceName: Coveralls API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n\
  \    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/test-driven-development/refs/heads/main/finops/test-driven-development-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agile
- Best Practices
- Continuous Integration
- Extreme Programming
- Methodology
- Software Development
- Testing
- FinOps
- Cost Management
- FOCUS
---
