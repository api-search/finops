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
description: FinOps framework definition for the Test Cases API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Test Cases
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Test Cases
  PublisherName: Test Cases
  ServiceCategory: Developer Tools / API
  ServiceName: Test Cases
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
name: Test Cases Finops
provider_name: Test Cases
provider_slug: test-cases
publisher_name: Test Cases
service_category: API
slug: test-cases-finops
source_filename: test-cases-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Test Cases\nproviderId: test-cases\npublisherName: Test Cases\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - API Testing\n  - Automation\n  - Quality Assurance\n  - Software Development\n  - Software Testing\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Test Cases API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Test Cases\n  ServiceCategory: Developer Tools / API\n  ProviderName: Test Cases\n  PublisherName: Test Cases\n  InvoiceIssuerName: Test Cases\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Postman API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Testing\n      - Collections\n      - Environments\n      - Test Automation\n    serviceName: Postman API\n    serviceCategory: API\n  - name: TestRail API\n    baseURL: https://yourproject.testrail.io/index.php?/api/v2\n    tags:\n      - Test Case Management\n      - Test Management\n      - Test Runs\n      - Testing\n    serviceName: TestRail API\n    serviceCategory: API\n  - name: Zephyr Scale API\n    baseURL: https://api.zephyrscale.smartbear.com/v2\n    tags:\n      - Jira\n      - Test Case Management\n      - Test Management\n      - Testing\n    serviceName: Zephyr Scale API\n\
  \    serviceCategory: API\n  - name: Xray Test Management API\n    baseURL: https://xray.cloud.getxray.app/api/v2\n    tags:\n      - Behavior-Driven Development\n      - Jira\n      - Test Case Management\n      - Test Execution\n    serviceName: Xray Test Management API\n    serviceCategory: API\n  - name: PractiTest API\n    baseURL: https://api.practitest.com/api/v2\n    tags:\n      - Quality Management\n      - Requirements\n      - Test Case Management\n      - Testing\n    serviceName: PractiTest API\n    serviceCategory: API\n  - name: Katalon TestOps API\n    baseURL: https://testops.katalon.io/api/v1\n    tags:\n      - CI/CD Integration\n      - Test Automation\n      - Test Case Management\n      - Testing\n    serviceName: Katalon TestOps API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target:\
  \ TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/test-cases/refs/heads/main/finops/test-cases-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Testing
- Automation
- Quality Assurance
- Software Development
- Software Testing
- Testing
- FinOps
- Cost Management
- FOCUS
---
