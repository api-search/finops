---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lever-openapi.yml
  format: yaml
  label: Lever Opportunities API
  slug: lever-opportunities-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lever/refs/heads/main/openapi/lever-openapi.yml
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
description: FinOps framework definition for the Lever API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lever
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Lever
  PublisherName: Lever
  ServiceCategory: Developer Tools / API
  ServiceName: Lever
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
name: Lever Finops
provider_name: Lever
provider_slug: lever
publisher_name: Lever
service_category: API
slug: lever-finops
source_filename: lever-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Lever\nproviderId: lever\npublisherName: Lever\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - HR\n  - ATS\n  - Recruiting\n  - Talent Acquisition\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Lever API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Lever\n  ServiceCategory: Developer Tools / API\n  ProviderName: Lever\n  PublisherName: Lever\n  InvoiceIssuerName: Lever\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Lever Opportunities API\n    baseURL: ''\n    tags:\n      - Opportunities\n      - Candidates\n      - Pipeline\n    serviceName: Lever Opportunities API\n    serviceCategory: API\n  - name: Lever Candidates API\n    baseURL: ''\n    tags:\n      - Candidates\n      - Legacy\n    serviceName: Lever Candidates API\n    serviceCategory: API\n  - name: Lever Contacts API\n    baseURL: ''\n    tags:\n      - Contacts\n      - People\n    serviceName: Lever Contacts API\n    serviceCategory: API\n  - name: Lever Postings API\n    baseURL: ''\n    tags:\n      - Postings\n      - Jobs\n      - Public\n    serviceName: Lever Postings API\n    serviceCategory: API\n  - name: Lever Applications API\n    baseURL: ''\n    tags:\n      - Applications\n   \
  \   - Submissions\n    serviceName: Lever Applications API\n    serviceCategory: API\n  - name: Lever Stages API\n    baseURL: ''\n    tags:\n      - Stages\n      - Pipeline\n    serviceName: Lever Stages API\n    serviceCategory: API\n  - name: Lever Archive Reasons API\n    baseURL: ''\n    tags:\n      - Archive Reasons\n      - Disposition\n    serviceName: Lever Archive Reasons API\n    serviceCategory: API\n  - name: Lever Interviews API\n    baseURL: ''\n    tags:\n      - Interviews\n      - Panels\n      - Scheduling\n    serviceName: Lever Interviews API\n    serviceCategory: API\n  - name: Lever Feedback API\n    baseURL: ''\n    tags:\n      - Feedback\n      - Scorecards\n    serviceName: Lever Feedback API\n    serviceCategory: API\n  - name: Lever Feedback Templates API\n    baseURL: ''\n    tags:\n      - Feedback Templates\n      - Forms\n    serviceName: Lever Feedback Templates API\n    serviceCategory: API\n  - name: Lever Notes API\n    baseURL: ''\n    tags:\n  \
  \    - Notes\n    serviceName: Lever Notes API\n    serviceCategory: API\n  - name: Lever Offers API\n    baseURL: ''\n    tags:\n      - Offers\n      - Approvals\n    serviceName: Lever Offers API\n    serviceCategory: API\n  - name: Lever Requisitions API\n    baseURL: ''\n    tags:\n      - Requisitions\n      - Headcount\n    serviceName: Lever Requisitions API\n    serviceCategory: API\n  - name: Lever Tags API\n    baseURL: ''\n    tags:\n      - Tags\n      - Metadata\n    serviceName: Lever Tags API\n    serviceCategory: API\n  - name: Lever Sources API\n    baseURL: ''\n    tags:\n      - Sources\n      - Attribution\n    serviceName: Lever Sources API\n    serviceCategory: API\n  - name: Lever Files API\n    baseURL: ''\n    tags:\n      - Files\n      - Resumes\n    serviceName: Lever Files API\n    serviceCategory: API\n  - name: Lever Resumes API\n    baseURL: ''\n    tags:\n      - Resumes\n      - Parsing\n    serviceName: Lever Resumes API\n    serviceCategory: API\n \
  \ - name: Lever Users API\n    baseURL: ''\n    tags:\n      - Users\n      - Permissions\n    serviceName: Lever Users API\n    serviceCategory: API\n  - name: Lever Audit Events API\n    baseURL: ''\n    tags:\n      - Audit\n      - Security\n    serviceName: Lever Audit Events API\n    serviceCategory: API\n  - name: Lever EEO API\n    baseURL: ''\n    tags:\n      - EEO\n      - Compliance\n    serviceName: Lever EEO API\n    serviceCategory: API\n  - name: Lever Webhooks API\n    baseURL: ''\n    tags:\n      - Webhooks\n      - Events\n    serviceName: Lever Webhooks API\n    serviceCategory: API\n  - name: Lever Postings Public API\n    baseURL: ''\n    tags:\n      - Postings\n      - Public\n      - Jobs\n    serviceName: Lever Postings Public API\n    serviceCategory: API\n  - name: Lever XML Feed\n    baseURL: ''\n    tags:\n      - XML\n      - Job Boards\n      - Aggregators\n    serviceName: Lever XML Feed\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K\
  \ Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lever/refs/heads/main/finops/lever-finops.yml
sources: []
specification: FinOps Framework
tags:
- HR
- ATS
- Recruiting
- Talent Acquisition
- SaaS
- FinOps
- Cost Management
- FOCUS
---
