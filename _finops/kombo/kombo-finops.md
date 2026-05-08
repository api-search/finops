---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Kombo Unified API
  slug: unified-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified HRIS API
  slug: hris-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified ATS API
  slug: ats-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified ATS-Assessment API
  slug: ats-assessment-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
- filename: openapi.json
  format: json
  label: Kombo Unified LMS API
  slug: lms-api
  spec_type: OpenAPI
  url: https://api.kombo.dev/openapi.json
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
description: FinOps framework definition for the Kombo API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Kombo
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Kombo
  PublisherName: Kombo
  ServiceCategory: Developer Tools / API
  ServiceName: Kombo
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
name: Kombo Finops
provider_name: Kombo
provider_slug: kombo
publisher_name: Kombo
service_category: API
slug: kombo-finops
source_filename: kombo-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Kombo\nproviderId: kombo\npublisherName: Kombo\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - ATS\n  - Embedded iPaaS\n  - HRIS\n  - LMS\n  - Payroll\n  - Unified API\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Kombo API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Kombo\n  ServiceCategory: Developer Tools / API\n  ProviderName: Kombo\n  PublisherName: Kombo\n  InvoiceIssuerName: Kombo\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n  \
  \    - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Kombo Unified API\n    baseURL: https://api.kombo.dev\n    tags:\n      - ATS\n      - HRIS\n      - Payroll\n      - Unified API\n    serviceName: Kombo Unified API\n    serviceCategory: API\n  - name: Kombo Unified HRIS API\n    baseURL: ''\n    tags:\n      - HRIS\n      - Employees\n      - Time Off\n    serviceName: Kombo Unified HRIS API\n    serviceCategory: API\n  - name: Kombo Unified ATS API\n    baseURL: ''\n    tags:\n      - ATS\n      - Recruiting\n    serviceName: Kombo Unified ATS API\n    serviceCategory: API\n  - name: Kombo Unified ATS-Assessment API\n    baseURL: ''\n    tags:\n      - ATS\n      - Assessments\n    serviceName: Kombo Unified ATS-Assessment API\n    serviceCategory: API\n  - name: Kombo Unified LMS\
  \ API\n    baseURL: ''\n    tags:\n      - LMS\n      - Learning\n    serviceName: Kombo Unified LMS API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kombo/refs/heads/main/finops/kombo-finops.yml
sources: []
specification: FinOps Framework
tags:
- ATS
- Embedded iPaaS
- HRIS
- LMS
- Payroll
- Unified API
- FinOps
- Cost Management
- FOCUS
---
