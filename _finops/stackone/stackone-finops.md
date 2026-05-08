---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stackone-openapi.yml
  format: yaml
  label: StackOne
  slug: stackone
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stackone/refs/heads/main/openapi/stackone-openapi.yml
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
description: FinOps framework definition for the StackOne API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: StackOne
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: StackOne
  PublisherName: StackOne
  ServiceCategory: Developer Tools / API
  ServiceName: StackOne
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
name: Stackone Finops
provider_name: StackOne
provider_slug: stackone
publisher_name: StackOne
service_category: API
slug: stackone-finops
source_filename: stackone-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: StackOne\nproviderId: stackone\npublisherName: StackOne\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Integrations\n  - iPaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the StackOne API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n   \
  \   feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and\
  \ Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: StackOne\n  ServiceCategory: Developer Tools / API\n  ProviderName: StackOne\n  PublisherName: StackOne\n  InvoiceIssuerName: StackOne\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n  \
  \    - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: StackOne\n    baseURL: ''\n    tags:\n      - Integrations\n      - iPaaS\n    serviceName: StackOne\n    serviceCategory: API\n  - name: StackOne Unified HRIS API\n    baseURL: ''\n    tags:\n      - Employees\n      - HRIS\n      - Human Resources\n      - Unified API\n    serviceName: StackOne Unified HRIS API\n    serviceCategory: API\n  - name: StackOne Unified ATS API\n    baseURL: ''\n    tags:\n      - Applicant Tracking\n      - ATS\n      - Recruitment\n      - Unified API\n    serviceName: StackOne Unified ATS API\n    serviceCategory: API\n  - name: StackOne Unified CRM API\n    baseURL: ''\n    tags:\n      - Contacts\n      - CRM\n      - Customer Relationship Management\n      - Unified API\n    serviceName: StackOne Unified CRM API\n\
  \    serviceCategory: API\n  - name: StackOne Unified LMS API\n    baseURL: ''\n    tags:\n      - Courses\n      - Learning Management\n      - LMS\n      - Unified API\n    serviceName: StackOne Unified LMS API\n    serviceCategory: API\n  - name: StackOne Unified IAM API\n    baseURL: ''\n    tags:\n      - Access Management\n      - IAM\n      - Identity\n      - Unified API\n    serviceName: StackOne Unified IAM API\n    serviceCategory: API\n  - name: StackOne Unified Documents API\n    baseURL: ''\n    tags:\n      - Documents\n      - Files\n      - Knowledge Management\n      - Unified API\n    serviceName: StackOne Unified Documents API\n    serviceCategory: API\n  - name: StackOne Unified Marketing API\n    baseURL: ''\n    tags:\n      - Campaigns\n      - Email\n      - Marketing\n      - SMS\n      - Unified API\n    serviceName: StackOne Unified Marketing API\n    serviceCategory: API\n  - name: StackOne Unified Ticketing API\n    baseURL: ''\n    tags:\n      - Helpdesk\n\
  \      - Support\n      - Ticketing\n      - Unified API\n    serviceName: StackOne Unified Ticketing API\n    serviceCategory: API\n  - name: StackOne Unified Messaging API\n    baseURL: ''\n    tags:\n      - Chat\n      - Communication\n      - Messaging\n      - Unified API\n    serviceName: StackOne Unified Messaging API\n    serviceCategory: API\n  - name: StackOne Unified Screening API\n    baseURL: ''\n    tags:\n      - Assessments\n      - Background Checks\n      - Screening\n      - Unified API\n    serviceName: StackOne Unified Screening API\n    serviceCategory: API\n  - name: StackOne Platform API\n    baseURL: ''\n    tags:\n      - Accounts\n      - Actions\n      - Administration\n      - Platform\n    serviceName: StackOne Platform API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\n\
  maintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stackone/refs/heads/main/finops/stackone-finops.yml
sources: []
specification: FinOps Framework
tags:
- Integrations
- iPaaS
- FinOps
- Cost Management
- FOCUS
---
