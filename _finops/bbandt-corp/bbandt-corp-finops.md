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
description: FinOps framework definition for the BB&T Corp (Truist) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: BB&T Corp (Truist)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: BB&T Corp (Truist)
  PublisherName: BB&T Corp (Truist)
  ServiceCategory: Developer Tools / API
  ServiceName: BB&T Corp (Truist)
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
name: Bbandt Corp Finops
provider_name: BB&T Corp (Truist)
provider_slug: bbandt-corp
publisher_name: BB&T Corp (Truist)
service_category: API
slug: bbandt-corp-finops
source_filename: bbandt-corp-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: BB&T Corp (Truist)\nproviderId: bbandt-corp\npublisherName: BB&T Corp (Truist)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Financial Services\n  - Open Banking\n  - Truist\n  - BB&T\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the BB&T Corp (Truist) API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: BB&T Corp (Truist)\n  ServiceCategory: Developer Tools / API\n  ProviderName: BB&T Corp (Truist)\n  PublisherName: BB&T Corp (Truist)\n  InvoiceIssuerName: BB&T Corp (Truist)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Truist Personal and Small Business Accounts API\n    baseURL: ''\n    tags:\n      - Banking\n      - Accounts\n      - Personal Banking\n      - Small Business\n    serviceName: Truist Personal and Small Business Accounts API\n    serviceCategory: API\n  - name: Truist Personal and Small Business Transactions API\n    baseURL: ''\n    tags:\n      - Banking\n      - Transactions\n      - Personal Banking\n      - Small Business\n    serviceName: Truist Personal and Small Business Transactions API\n    serviceCategory: API\n  - name: Truist Commercial Accounts API\n    baseURL: ''\n    tags:\n      - Banking\n      - Accounts\n \
  \     - Commercial Banking\n    serviceName: Truist Commercial Accounts API\n    serviceCategory: API\n  - name: Truist Commercial Account Transactions API\n    baseURL: ''\n    tags:\n      - Banking\n      - Transactions\n      - Commercial Banking\n    serviceName: Truist Commercial Account Transactions API\n    serviceCategory: API\n  - name: Truist Association Services API\n    baseURL: ''\n    tags:\n      - Banking\n      - Association Services\n      - Payments\n    serviceName: Truist Association Services API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bbandt-corp/refs/heads/main/finops/bbandt-corp-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Financial Services
- Open Banking
- Truist
- BB&T
- FinOps
- Cost Management
- FOCUS
---
