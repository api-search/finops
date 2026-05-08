---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: smartrecruiters-posting-openapi.yml
  format: yaml
  label: SmartRecruiters Posting API
  slug: posting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/openapi/smartrecruiters-posting-openapi.yml
- filename: smartrecruiters-jobs-openapi.yml
  format: yaml
  label: SmartRecruiters Job API
  slug: job-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/openapi/smartrecruiters-jobs-openapi.yml
- filename: smartrecruiters-candidates-openapi.yml
  format: yaml
  label: SmartRecruiters Candidate API
  slug: candidate-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/openapi/smartrecruiters-candidates-openapi.yml
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
description: FinOps framework definition for the SmartRecruiters API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SmartRecruiters
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SmartRecruiters
  PublisherName: SmartRecruiters
  ServiceCategory: Developer Tools / API
  ServiceName: SmartRecruiters
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
name: Smartrecruiters Finops
provider_name: SmartRecruiters
provider_slug: smartrecruiters
publisher_name: SmartRecruiters
service_category: API
slug: smartrecruiters-finops
source_filename: smartrecruiters-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SmartRecruiters\nproviderId: smartrecruiters\npublisherName: SmartRecruiters\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Human Resources\n  - Recruiting\n  - Talent Acquisition\n  - Applicant Tracking\n  - HR Technology\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SmartRecruiters API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n   \
  \ description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the\
  \ FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SmartRecruiters\n  ServiceCategory: Developer Tools / API\n  ProviderName: SmartRecruiters\n  PublisherName: SmartRecruiters\n  InvoiceIssuerName: SmartRecruiters\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SmartRecruiters Posting API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Jobs\n      - Postings\n      - Career Sites\n    serviceName: SmartRecruiters Posting API\n    serviceCategory: API\n  - name: SmartRecruiters Job API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Jobs\n      - Hiring\n    serviceName: SmartRecruiters Job API\n    serviceCategory: API\n  - name: SmartRecruiters Candidate API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Candidates\n      - Applicants\n      - Talent\n    serviceName: SmartRecruiters Candidate API\n    serviceCategory: API\n\
  \  - name: SmartRecruiters Application API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Applications\n      - Candidates\n      - Screening\n    serviceName: SmartRecruiters Application API\n    serviceCategory: API\n  - name: SmartRecruiters Assessment API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Assessments\n      - Marketplace\n      - Partners\n    serviceName: SmartRecruiters Assessment API\n    serviceCategory: API\n  - name: SmartRecruiters Interview API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Interviews\n      - Scheduling\n    serviceName: SmartRecruiters Interview API\n    serviceCategory: API\n  - name: SmartRecruiters Reporting API\n    baseURL: https://api.smartrecruiters.com\n    tags:\n      - Reporting\n      - Analytics\n      - Data Export\n    serviceName: SmartRecruiters Reporting API\n    serviceCategory: API\n  - name: SmartRecruiters Job Board API\n    baseURL: https://api.smartrecruiters.com\n\
  \    tags:\n      - Job Boards\n      - Partners\n      - Jobs\n    serviceName: SmartRecruiters Job Board API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/smartrecruiters/refs/heads/main/finops/smartrecruiters-finops.yml
sources: []
specification: FinOps Framework
tags:
- Human Resources
- Recruiting
- Talent Acquisition
- Applicant Tracking
- HR Technology
- FinOps
- Cost Management
- FOCUS
---
