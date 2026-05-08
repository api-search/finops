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
description: FinOps framework definition for the UGI Corporation API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: UGI Corporation
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: UGI Corporation
  PublisherName: UGI Corporation
  ServiceCategory: Developer Tools / API
  ServiceName: UGI Corporation
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
name: Ugi Finops
provider_name: UGI Corporation
provider_slug: ugi
publisher_name: UGI Corporation
service_category: API
slug: ugi-finops
source_filename: ugi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: UGI Corporation\nproviderId: ugi\npublisherName: UGI Corporation\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Energy\n  - Utilities\n  - Natural Gas\n  - Propane\n  - Electric\n  - Fortune 500\n  - Pennsylvania\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the UGI Corporation API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: UGI Corporation\n  ServiceCategory: Developer Tools / API\n  ProviderName: UGI Corporation\n  PublisherName: UGI Corporation\n  InvoiceIssuerName: UGI Corporation\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: UGI Utilities\n    baseURL: ''\n    tags:\n      - Natural Gas\n      - Electric\n      - Utilities\n      - Pennsylvania\n      - Energy Distribution\n    serviceName: UGI Utilities\n    serviceCategory: API\n  - name: AmeriGas Propane\n    baseURL: ''\n    tags:\n      - Propane\n      - Energy\n      - Retail\n      - Distribution\n      - Delivery\n    serviceName: AmeriGas Propane\n    serviceCategory: API\n  - name: UGI Energy Services\n    baseURL: ''\n    tags:\n      - Natural Gas\n      - Electricity\n      - Energy Services\n      - Commercial\n      - Industrial\n    serviceName: UGI Energy Services\n    serviceCategory: API\n\
  \  - name: UGI International\n    baseURL: ''\n    tags:\n      - LPG\n      - Natural Gas\n      - Europe\n      - International\n      - Energy Distribution\n    serviceName: UGI International\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ugi/refs/heads/main/finops/ugi-finops.yml
sources: []
specification: FinOps Framework
tags:
- Energy
- Utilities
- Natural Gas
- Propane
- Electric
- Fortune 500
- Pennsylvania
- FinOps
- Cost Management
- FOCUS
---
