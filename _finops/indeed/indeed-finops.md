---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: indeed-employer-api-openapi.yml
  format: yaml
  label: Indeed Job Sync API
  slug: job-sync
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/indeed/refs/heads/main/openapi/indeed-employer-api-openapi.yml
- filename: indeed-employer-api-openapi.yml
  format: yaml
  label: Indeed Employer API
  slug: employer
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/indeed/refs/heads/main/openapi/indeed-employer-api-openapi.yml
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
description: FinOps framework definition for the Indeed API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Indeed
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Indeed
  PublisherName: Indeed
  ServiceCategory: Developer Tools / API
  ServiceName: Indeed
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
name: Indeed Finops
provider_name: Indeed
provider_slug: indeed
publisher_name: Indeed
service_category: API
slug: indeed-finops
source_filename: indeed-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Indeed\nproviderId: indeed\npublisherName: Indeed\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Careers\n  - Employment\n  - Hiring\n  - Job Search\n  - Jobs\n  - Recruiting\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Indeed API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Indeed\n  ServiceCategory: Developer Tools / API\n  ProviderName: Indeed\n  PublisherName: Indeed\n  InvoiceIssuerName: Indeed\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Indeed Job Search API\n    baseURL: https://api.indeed.com\n    tags:\n      - Deprecated\n      - Jobs\n      - Listings\n      - Search\n    serviceName: Indeed Job Search API\n    serviceCategory: API\n  - name: Indeed Publisher API\n    baseURL: https://api.indeed.com/ads\n    tags:\n      - Advertising\n      - Monetization\n      - Publisher\n    serviceName: Indeed Publisher API\n    serviceCategory: API\n  - name: Indeed Apply API\n    baseURL: https://api.indeed.com/apply\n    tags:\n      - Applications\n      - Apply\n      - Hiring\n    serviceName: Indeed Apply API\n    serviceCategory: API\n  - name: Indeed Job Sync API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - ATS\n      - GraphQL\n\
  \      - Jobs\n      - Postings\n    serviceName: Indeed Job Sync API\n    serviceCategory: API\n  - name: Indeed Disposition Sync API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - Applications\n      - ATS\n      - Disposition\n      - GraphQL\n      - Tracking\n    serviceName: Indeed Disposition Sync API\n    serviceCategory: API\n  - name: Indeed Sponsored Jobs API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - Advertising\n      - Campaigns\n      - GraphQL\n      - Sponsored\n    serviceName: Indeed Sponsored Jobs API\n    serviceCategory: API\n  - name: Indeed Job Update API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - GraphQL\n      - Jobs\n      - Updates\n      - Webhooks\n    serviceName: Indeed Job Update API\n    serviceCategory: API\n  - name: Indeed Real-time API\n    baseURL: https://apis.indeed.com\n    tags:\n      - Events\n      - Real-Time\n      - SSE\n      - Streaming\n    serviceName: Indeed Real-time\
  \ API\n    serviceCategory: API\n  - name: Indeed Interview API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - Deprecated\n      - GraphQL\n      - Interviews\n      - Scheduling\n      - Virtual\n    serviceName: Indeed Interview API\n    serviceCategory: API\n  - name: Indeed Employer API\n    baseURL: https://apis.indeed.com\n    tags:\n      - ATS\n      - Candidates\n      - Employers\n      - Jobs\n    serviceName: Indeed Employer API\n    serviceCategory: API\n  - name: Indeed Employer Data API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - ATS\n      - Employers\n      - GraphQL\n    serviceName: Indeed Employer Data API\n    serviceCategory: API\n  - name: Indeed Conversion Tracking API\n    baseURL: https://apis.indeed.com\n    tags:\n      - Analytics\n      - Conversion\n      - Reporting\n      - Tracking\n    serviceName: Indeed Conversion Tracking API\n    serviceCategory: API\n  - name: Indeed Employer Registration API\n    baseURL:\
  \ https://apis.indeed.com/graphql\n    tags:\n      - ATS\n      - Candidate Sync\n      - Employers\n      - Registration\n    serviceName: Indeed Employer Registration API\n    serviceCategory: API\n  - name: Indeed Retrieve Candidates API\n    baseURL: https://apis.indeed.com/graphql\n    tags:\n      - Applications\n      - ATS\n      - Candidate Sync\n      - Candidates\n    serviceName: Indeed Retrieve Candidates API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/indeed/refs/heads/main/finops/indeed-finops.yml
sources: []
specification: FinOps Framework
tags:
- Careers
- Employment
- Hiring
- Job Search
- Jobs
- Recruiting
- FinOps
- Cost Management
- FOCUS
---
