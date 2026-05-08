---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.v3.json
  format: json
  label: Jira Software API
  slug: ''
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/software/swagger.v3.json
- filename: vsts-rest-api-specs
  format: yaml
  label: Azure DevOps Test Plans API
  slug: ''
  spec_type: OpenAPI
  url: https://github.com/MicrosoftDocs/vsts-rest-api-specs
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
description: FinOps framework definition for the Test Plans API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Test Plans
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Test Plans
  PublisherName: Test Plans
  ServiceCategory: Developer Tools / API
  ServiceName: Test Plans
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
name: Test Plans Finops
provider_name: Test Plans
provider_slug: test-plans
publisher_name: Test Plans
service_category: API
slug: test-plans-finops
source_filename: test-plans-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Test Plans\nproviderId: test-plans\npublisherName: Test Plans\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Documentation\n  - Quality Assurance\n  - Software Development\n  - Test Management\n  - Testing\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Test Plans API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Test Plans\n  ServiceCategory: Developer Tools / API\n  ProviderName: Test Plans\n  PublisherName: Test Plans\n  InvoiceIssuerName: Test Plans\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: TestRail API\n    baseURL: https://yourproject.testrail.io/index.php?/api/v2\n    tags:\n      - Test Management\n      - Test Plans\n      - Test Runs\n      - Testing\n    serviceName: TestRail API\n    serviceCategory: API\n  - name: Jira Software API\n    baseURL: https://your-org.atlassian.net/rest/agile/1.0\n    tags:\n      - Agile\n      - Jira\n      - Project Management\n      - Test Planning\n    serviceName: Jira Software API\n    serviceCategory: API\n  - name: Azure DevOps Test Plans API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/testplan\n    tags:\n      - Azure DevOps\n      - CI/CD\n      - Microsoft\n      - Test Plans\n \
  \   serviceName: Azure DevOps Test Plans API\n    serviceCategory: API\n  - name: qTest API\n    baseURL: https://your-org.qtestnet.com/api/v3\n    tags:\n      - Agile Testing\n      - Test Management\n      - Test Plans\n      - Tricentis\n    serviceName: qTest API\n    serviceCategory: API\n  - name: ALM Octane API\n    baseURL: https://your-octane.example.com/api/shared_spaces\n    tags:\n      - ALM\n      - Enterprise Testing\n      - Quality Management\n      - Test Plans\n    serviceName: ALM Octane API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/test-plans/refs/heads/main/finops/test-plans-finops.yml
sources: []
specification: FinOps Framework
tags:
- Documentation
- Quality Assurance
- Software Development
- Test Management
- Testing
- FinOps
- Cost Management
- FOCUS
---
