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
description: FinOps framework definition for the Workable API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Workable
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Workable
  PublisherName: Workable
  ServiceCategory: Developer Tools / API
  ServiceName: Workable
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
name: Workable Finops
provider_name: Workable
provider_slug: workable
publisher_name: Workable
service_category: API
slug: workable-finops
source_filename: workable-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Workable\nproviderId: workable\npublisherName: Workable\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - HR\n  - ATS\n  - Recruiting\n  - Sourcing\n  - Video Interviews\n  - Assessments\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Workable API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Workable\n  ServiceCategory: Developer Tools / API\n  ProviderName: Workable\n  PublisherName: Workable\n  InvoiceIssuerName: Workable\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Workable Jobs API\n    baseURL: ''\n    tags:\n      - Jobs\n      - Postings\n    serviceName: Workable Jobs API\n    serviceCategory: API\n  - name: Workable Candidates API\n    baseURL: ''\n    tags:\n      - Candidates\n      - Applicants\n    serviceName: Workable Candidates API\n    serviceCategory: API\n  - name: Workable Stages API\n    baseURL: ''\n    tags:\n      - Stages\n      - Pipeline\n    serviceName: Workable Stages API\n    serviceCategory: API\n  - name: Workable Members API\n    baseURL: ''\n    tags:\n      - Members\n      - Recruiters\n      - Users\n    serviceName: Workable Members API\n    serviceCategory: API\n  - name: Workable Recruiters API\n    baseURL: ''\n    tags:\n\
  \      - Recruiters\n      - External\n    serviceName: Workable Recruiters API\n    serviceCategory: API\n  - name: Workable Departments API\n    baseURL: ''\n    tags:\n      - Departments\n      - Org Structure\n    serviceName: Workable Departments API\n    serviceCategory: API\n  - name: Workable Custom Attributes API\n    baseURL: ''\n    tags:\n      - Custom Attributes\n      - Metadata\n    serviceName: Workable Custom Attributes API\n    serviceCategory: API\n  - name: Workable Activities API\n    baseURL: ''\n    tags:\n      - Activities\n      - Audit\n    serviceName: Workable Activities API\n    serviceCategory: API\n  - name: Workable Comments API\n    baseURL: ''\n    tags:\n      - Comments\n      - Notes\n    serviceName: Workable Comments API\n    serviceCategory: API\n  - name: Workable Evaluations API\n    baseURL: ''\n    tags:\n      - Evaluations\n      - Scorecards\n      - Feedback\n    serviceName: Workable Evaluations API\n    serviceCategory: API\n  - name:\
  \ Workable Offers API\n    baseURL: ''\n    tags:\n      - Offers\n    serviceName: Workable Offers API\n    serviceCategory: API\n  - name: Workable Assessments API\n    baseURL: ''\n    tags:\n      - Assessments\n      - Tests\n    serviceName: Workable Assessments API\n    serviceCategory: API\n  - name: Workable Disqualification Reasons API\n    baseURL: ''\n    tags:\n      - Disqualification\n      - Rejection\n    serviceName: Workable Disqualification Reasons API\n    serviceCategory: API\n  - name: Workable Questions API\n    baseURL: ''\n    tags:\n      - Questions\n      - Application Forms\n    serviceName: Workable Questions API\n    serviceCategory: API\n  - name: Workable Events API\n    baseURL: ''\n    tags:\n      - Events\n      - Interviews\n      - Scheduling\n    serviceName: Workable Events API\n    serviceCategory: API\n  - name: Workable Webhooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Subscriptions\n    serviceName: Workable Webhooks API\n\
  \    serviceCategory: API\n  - name: Workable Public Jobs API\n    baseURL: ''\n    tags:\n      - Jobs\n      - Public\n    serviceName: Workable Public Jobs API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workable/refs/heads/main/finops/workable-finops.yml
sources: []
specification: FinOps Framework
tags:
- HR
- ATS
- Recruiting
- Sourcing
- Video Interviews
- Assessments
- SaaS
- FinOps
- Cost Management
- FOCUS
---
