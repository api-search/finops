---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: unified-to-accounting-openapi.yaml
  format: yaml
  label: Unified.to Accounting API
  slug: accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-accounting-openapi.yaml
- filename: unified-to-marketing-openapi.yaml
  format: yaml
  label: Unified.to Advertising API
  slug: ads-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-marketing-openapi.yaml
- filename: unified-to-hr-talent-openapi.yaml
  format: yaml
  label: Unified.to Assessment API
  slug: assessment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-hr-talent-openapi.yaml
- filename: unified-to-ats-openapi.yaml
  format: yaml
  label: Unified.to ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-ats-openapi.yaml
- filename: unified-to-productivity-openapi.yaml
  format: yaml
  label: Unified.to Calendar & Meetings API
  slug: calendar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-productivity-openapi.yaml
- filename: unified-to-it-ops-openapi.yaml
  format: yaml
  label: Unified.to Call Center API
  slug: call-center-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-it-ops-openapi.yaml
- filename: unified-to-crm-openapi.yaml
  format: yaml
  label: Unified.to CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-crm-openapi.yaml
- filename: unified-to-commerce-openapi.yaml
  format: yaml
  label: Unified.to E-Commerce API
  slug: ecommerce-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-commerce-openapi.yaml
- filename: unified-to-hris-openapi.yaml
  format: yaml
  label: Unified.to HR & Directory API
  slug: hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-hris-openapi.yaml
- filename: unified-to-productivity-openapi.yaml
  format: yaml
  label: Unified.to Messaging API
  slug: messaging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-productivity-openapi.yaml
- filename: unified-to-it-ops-openapi.yaml
  format: yaml
  label: Unified.to Payments API
  slug: payment-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-it-ops-openapi.yaml
- filename: unified-to-it-ops-openapi.yaml
  format: yaml
  label: Unified.to Ticketing API
  slug: ticketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/openapi/unified-to-it-ops-openapi.yaml
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
description: FinOps framework definition for the Unified.to API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Unified.to
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Unified.to
  PublisherName: Unified.to
  ServiceCategory: Developer Tools / API
  ServiceName: Unified.to
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
name: Unified To Finops
provider_name: Unified.to
provider_slug: unified-to
publisher_name: Unified.to
service_category: API
slug: unified-to-finops
source_filename: unified-to-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Unified.to\nproviderId: unified-to\npublisherName: Unified.to\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Integrations\n  - Unified API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Unified.to API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application,\
  \ and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education\
  \ and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Unified.to\n  ServiceCategory: Developer Tools / API\n  ProviderName: Unified.to\n  PublisherName: Unified.to\n  InvoiceIssuerName: Unified.to\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      -\
  \ region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Unified.to\n    baseURL: ''\n    tags:\n      - Integrations\n      - Unified API\n    serviceName: Unified.to\n    serviceCategory: API\n  - name: Unified.to Accounting API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Financial\n      - Invoices\n      - Payments\n    serviceName: Unified.to Accounting API\n    serviceCategory: API\n  - name: Unified.to Advertising API\n    baseURL: ''\n    tags:\n      - Ads\n      - Advertising\n      - Marketing\n    serviceName: Unified.to Advertising API\n    serviceCategory: API\n  - name: Unified.to Assessment API\n    baseURL: ''\n    tags:\n      - Assessment\n      - Evaluation\n      - Testing\n    serviceName: Unified.to Assessment API\n    serviceCategory: API\n  - name: Unified.to\
  \ ATS API\n    baseURL: ''\n    tags:\n      - Applicant Tracking\n      - ATS\n      - Hiring\n      - Recruiting\n    serviceName: Unified.to ATS API\n    serviceCategory: API\n  - name: Unified.to Authentication API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Identity\n      - Login\n      - OAuth\n    serviceName: Unified.to Authentication API\n    serviceCategory: API\n  - name: Unified.to Calendar & Meetings API\n    baseURL: ''\n    tags:\n      - Calendar\n      - Meetings\n      - Scheduling\n    serviceName: Unified.to Calendar & Meetings API\n    serviceCategory: API\n  - name: Unified.to Call Center API\n    baseURL: ''\n    tags:\n      - Call Center\n      - Communications\n      - Voice\n    serviceName: Unified.to Call Center API\n    serviceCategory: API\n  - name: Unified.to CRM API\n    baseURL: ''\n    tags:\n      - Contacts\n      - CRM\n      - Deals\n      - Sales\n    serviceName: Unified.to CRM API\n    serviceCategory: API\n  - name: Unified.to\
  \ E-Commerce API\n    baseURL: ''\n    tags:\n      - E-Commerce\n      - Orders\n      - Products\n      - Shopping\n    serviceName: Unified.to E-Commerce API\n    serviceCategory: API\n  - name: Unified.to HR & Directory API\n    baseURL: ''\n    tags:\n      - Directory\n      - HR\n      - HRIS\n      - Payroll\n    serviceName: Unified.to HR & Directory API\n    serviceCategory: API\n  - name: Unified.to Messaging API\n    baseURL: ''\n    tags:\n      - Chat\n      - Communication\n      - Messaging\n    serviceName: Unified.to Messaging API\n    serviceCategory: API\n  - name: Unified.to Payments API\n    baseURL: ''\n    tags:\n      - Billing\n      - Payments\n      - Transactions\n    serviceName: Unified.to Payments API\n    serviceCategory: API\n  - name: Unified.to Ticketing API\n    baseURL: ''\n    tags:\n      - Help Desk\n      - Support\n      - Ticketing\n    serviceName: Unified.to Ticketing API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unified-to/refs/heads/main/finops/unified-to-finops.yml
sources: []
specification: FinOps Framework
tags:
- Integrations
- Unified API
- FinOps
- Cost Management
- FOCUS
---
