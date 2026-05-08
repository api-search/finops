---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: merge-hris-api-openapi.yaml
  format: yaml
  label: Merge HRIS API
  slug: hris-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-hris-api-openapi.yaml
- filename: merge-ats-api-openapi.yaml
  format: yaml
  label: Merge ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-ats-api-openapi.yaml
- filename: merge-accounting-api-openapi.yaml
  format: yaml
  label: Merge Accounting API
  slug: accounting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-accounting-api-openapi.yaml
- filename: merge-ticketing-api-openapi.yaml
  format: yaml
  label: Merge Ticketing API
  slug: ticketing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-ticketing-api-openapi.yaml
- filename: merge-crm-api-openapi.yaml
  format: yaml
  label: Merge CRM API
  slug: crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-crm-api-openapi.yaml
- filename: merge-file-storage-api-openapi.yaml
  format: yaml
  label: Merge File Storage API
  slug: file-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/openapi/merge-file-storage-api-openapi.yaml
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
description: FinOps framework definition for the Merge API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Merge
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Merge
  PublisherName: Merge
  ServiceCategory: Developer Tools / API
  ServiceName: Merge
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
name: Merge Finops
provider_name: Merge
provider_slug: merge
publisher_name: Merge
service_category: API
slug: merge-finops
source_filename: merge-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Merge\nproviderId: merge\npublisherName: Merge\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Integrations\n  - Platform\n  - Unified API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Merge API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n\
  \      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and\
  \ Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Merge\n  ServiceCategory: Developer Tools / API\n  ProviderName: Merge\n  PublisherName: Merge\n  InvoiceIssuerName: Merge\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n\
  \  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Merge\n    baseURL: ''\n    tags:\n      - Integrations\n      - Platform\n      - Unified API\n    serviceName: Merge\n    serviceCategory: API\n  - name: Merge HRIS API\n    baseURL: ''\n    tags:\n      - Directory\n      - HRIS\n      - Human Resources\n      - Payroll\n      - Unified API\n    serviceName: Merge HRIS API\n    serviceCategory: API\n  - name: Merge ATS API\n    baseURL: ''\n    tags:\n      - Applicant Tracking\n      - ATS\n      - Recruiting\n      - Unified API\n    serviceName: Merge ATS API\n    serviceCategory: API\n  - name: Merge Accounting API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Finance\n      - Unified API\n    serviceName: Merge Accounting API\n    serviceCategory: API\n  - name: Merge Ticketing API\n    baseURL:\
  \ ''\n    tags:\n      - Project Management\n      - Ticketing\n      - Unified API\n    serviceName: Merge Ticketing API\n    serviceCategory: API\n  - name: Merge CRM API\n    baseURL: ''\n    tags:\n      - CRM\n      - Customer Relationship Management\n      - Unified API\n    serviceName: Merge CRM API\n    serviceCategory: API\n  - name: Merge File Storage API\n    baseURL: ''\n    tags:\n      - Documents\n      - File Storage\n      - Unified API\n    serviceName: Merge File Storage API\n    serviceCategory: API\n  - name: Merge Knowledge Base API\n    baseURL: ''\n    tags:\n      - Content Management\n      - Knowledge Base\n      - Unified API\n    serviceName: Merge Knowledge Base API\n    serviceCategory: API\n  - name: Merge Chat API\n    baseURL: ''\n    tags:\n      - Chat\n      - Messaging\n      - Unified API\n    serviceName: Merge Chat API\n    serviceCategory: API\n  - name: Merge Agent Handler\n    baseURL: ''\n    tags:\n      - AI Agents\n      - Integrations\n\
  \      - MCP\n      - Tool Use\n    serviceName: Merge Agent Handler\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/merge/refs/heads/main/finops/merge-finops.yml
sources: []
specification: FinOps Framework
tags:
- Integrations
- Platform
- Unified API
- FinOps
- Cost Management
- FOCUS
---
