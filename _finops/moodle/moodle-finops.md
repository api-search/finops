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
description: FinOps framework definition for the Moodle API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Moodle
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Moodle
  PublisherName: Moodle
  ServiceCategory: Developer Tools / API
  ServiceName: Moodle
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
name: Moodle Finops
provider_name: Moodle
provider_slug: moodle
publisher_name: Moodle
service_category: API
slug: moodle-finops
source_filename: moodle-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Moodle\nproviderId: moodle\npublisherName: Moodle\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - E-Learning\n  - EdTech\n  - LMS\n  - Moodle\n  - Open Source\n  - Web Services\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Moodle API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Moodle\n  ServiceCategory: Developer Tools / API\n  ProviderName: Moodle\n  PublisherName: Moodle\n  InvoiceIssuerName: Moodle\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Moodle Web Services API\n    baseURL: ''\n    tags:\n      - External\n      - Integration\n      - REST\n      - SOAP\n      - Web Services\n    serviceName: Moodle Web Services API\n    serviceCategory: API\n  - name: Moodle External Functions API\n    baseURL: ''\n    tags:\n      - External\n      - Functions\n      - Integration\n      - Web Services\n    serviceName: Moodle External Functions API\n    serviceCategory: API\n  - name: Moodle Access API\n    baseURL: ''\n    tags:\n      - Access\n      - Authorization\n      - Permissions\n      - Roles\n    serviceName: Moodle Access API\n    serviceCategory: API\n  - name: Moodle Roles API\n    baseURL: ''\n    tags:\n      - Access\n      - Capabilities\n    \
  \  - Permissions\n      - Roles\n    serviceName: Moodle Roles API\n    serviceCategory: API\n  - name: Moodle Data Manipulation API (DML)\n    baseURL: ''\n    tags:\n      - Database\n      - DML\n      - Persistence\n    serviceName: Moodle Data Manipulation API (DML)\n    serviceCategory: API\n  - name: Moodle File API\n    baseURL: ''\n    tags:\n      - Files\n      - Storage\n      - Uploads\n    serviceName: Moodle File API\n    serviceCategory: API\n  - name: Moodle Form API\n    baseURL: ''\n    tags:\n      - Forms\n      - UI\n      - Validation\n    serviceName: Moodle Form API\n    serviceCategory: API\n  - name: Moodle Events API\n    baseURL: ''\n    tags:\n      - Events\n      - Logging\n      - Observers\n    serviceName: Moodle Events API\n    serviceCategory: API\n  - name: Moodle Hooks API\n    baseURL: ''\n    tags:\n      - Extensibility\n      - Hooks\n      - Plugins\n    serviceName: Moodle Hooks API\n    serviceCategory: API\n  - name: Moodle Privacy API\n \
  \   baseURL: ''\n    tags:\n      - Compliance\n      - GDPR\n      - Privacy\n    serviceName: Moodle Privacy API\n    serviceCategory: API\n  - name: Moodle Task API\n    baseURL: ''\n    tags:\n      - Background Jobs\n      - Cron\n      - Scheduling\n    serviceName: Moodle Task API\n    serviceCategory: API\n  - name: Moodle Payment API\n    baseURL: ''\n    tags:\n      - Enrollment\n      - Gateways\n      - Payments\n    serviceName: Moodle Payment API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moodle/refs/heads/main/finops/moodle-finops.yml
sources: []
specification: FinOps Framework
tags:
- E-Learning
- EdTech
- LMS
- Moodle
- Open Source
- Web Services
- FinOps
- Cost Management
- FOCUS
---
