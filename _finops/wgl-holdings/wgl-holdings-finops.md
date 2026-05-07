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
description: FinOps framework definition for the WGL Holdings API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: WGL Holdings
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: WGL Holdings
  PublisherName: WGL Holdings
  ServiceCategory: Developer Tools / API
  ServiceName: WGL Holdings
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
name: Wgl Holdings Finops
provider_name: WGL Holdings
provider_slug: wgl-holdings
publisher_name: WGL Holdings
service_category: API
slug: wgl-holdings-finops
source_filename: wgl-holdings-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: WGL Holdings\nproviderId: wgl-holdings\npublisherName: WGL Holdings\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Energy\n  - Natural Gas\n  - Utilities\n  - Electricity\n  - Retail Energy\n  - Midstream\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the WGL Holdings API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: WGL Holdings\n  ServiceCategory: Developer Tools / API\n  ProviderName: WGL Holdings\n  PublisherName: WGL Holdings\n  InvoiceIssuerName: WGL Holdings\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API\
  \ responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Washington Gas\n    baseURL: ''\n    tags:\n      - Natural Gas\n      - Utilities\n      - Regulated\n      - Distribution\n    serviceName: Washington Gas\n    serviceCategory: API\n  - name: WGL Energy Services\n    baseURL: ''\n    tags:\n      - Retail Energy\n      - Natural Gas\n      - Electricity\n      - Renewable Energy\n      - Carbon Neutrality\n    serviceName: WGL Energy Services\n    serviceCategory: API\n  - name: WGL Midstream\n    baseURL: ''\n    tags:\n      - Midstream\n      - Natural Gas Storage\n      - Pipeline\n      - Energy Assets\n    serviceName: WGL Midstream\n    serviceCategory: API\n  - name: Hampshire Gas\n    baseURL:\
  \ ''\n    tags:\n      - Natural Gas Storage\n      - Underground Storage\n      - West Virginia\n      - Pipeline\n    serviceName: Hampshire Gas\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wgl-holdings/refs/heads/main/finops/wgl-holdings-finops.yml
sources: []
specification: FinOps Framework
tags:
- Energy
- Natural Gas
- Utilities
- Electricity
- Retail Energy
- Midstream
- FinOps
- Cost Management
- FOCUS
---
