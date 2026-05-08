---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: greenhouse-harvest-openapi.yml
  format: yaml
  label: Greenhouse Harvest API
  slug: harvest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-harvest-openapi.yml
- filename: greenhouse-job-board-openapi.yml
  format: yaml
  label: Greenhouse Job Board API
  slug: job-board
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-job-board-openapi.yml
- filename: greenhouse-ingestion-openapi.yml
  format: yaml
  label: Greenhouse Candidate Ingestion API
  slug: ingestion
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-ingestion-openapi.yml
- filename: greenhouse-onboarding-openapi.yml
  format: yaml
  label: Greenhouse Onboarding API
  slug: onboarding
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/openapi/greenhouse-onboarding-openapi.yml
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
description: FinOps framework definition for the Greenhouse API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Greenhouse
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Greenhouse
  PublisherName: Greenhouse
  ServiceCategory: Developer Tools / API
  ServiceName: Greenhouse
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
name: Greenhouse Finops
provider_name: Greenhouse
provider_slug: greenhouse
publisher_name: Greenhouse
service_category: API
slug: greenhouse-finops
source_filename: greenhouse-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Greenhouse\nproviderId: greenhouse\npublisherName: Greenhouse\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - ATS\n  - Recruiting\n  - Candidates\n  - Jobs\n  - Onboarding\n  - HR\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Greenhouse API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Greenhouse\n  ServiceCategory: Developer Tools / API\n  ProviderName: Greenhouse\n  PublisherName: Greenhouse\n  InvoiceIssuerName: Greenhouse\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Greenhouse Harvest API\n    baseURL: https://harvest.greenhouse.io/v1\n    tags:\n      - Harvest\n      - Candidates\n      - Jobs\n      - Applications\n    serviceName: Greenhouse Harvest API\n    serviceCategory: API\n  - name: Greenhouse Job Board API\n    baseURL: https://boards-api.greenhouse.io/v1/boards\n    tags:\n      - Job Board\n      - Careers\n      - Jobs\n    serviceName: Greenhouse Job Board API\n    serviceCategory: API\n  - name: Greenhouse Candidate Ingestion API\n    baseURL: https://api.greenhouse.io/v1/partner\n    tags:\n      - Ingestion\n      - Candidates\n      - Sourcing\n    serviceName: Greenhouse Candidate Ingestion API\n    serviceCategory: API\n  - name: Greenhouse\
  \ Onboarding API\n    baseURL: https://onboarding-api.greenhouse.io/graphql\n    tags:\n      - Onboarding\n      - GraphQL\n      - Employees\n    serviceName: Greenhouse Onboarding API\n    serviceCategory: API\n  - name: Greenhouse Assessment API\n    baseURL: ''\n    tags:\n      - Assessment\n      - Testing\n      - Candidates\n    serviceName: Greenhouse Assessment API\n    serviceCategory: API\n  - name: Greenhouse Audit Log API\n    baseURL: ''\n    tags:\n      - Audit\n      - Compliance\n      - Logging\n    serviceName: Greenhouse Audit Log API\n    serviceCategory: API\n  - name: Greenhouse Recruiting Webhooks\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Recruiting\n      - Events\n    serviceName: Greenhouse Recruiting Webhooks\n    serviceCategory: API\n  - name: Greenhouse Onboarding Webhooks\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Onboarding\n      - Events\n    serviceName: Greenhouse Onboarding Webhooks\n    serviceCategory: API\nunitEconomics:\n\
  \  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/greenhouse/refs/heads/main/finops/greenhouse-finops.yml
sources: []
specification: FinOps Framework
tags:
- ATS
- Recruiting
- Candidates
- Jobs
- Onboarding
- HR
- FinOps
- Cost Management
- FOCUS
---
