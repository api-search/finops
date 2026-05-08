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
description: FinOps framework definition for the CenterPoint Energy API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CenterPoint Energy
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CenterPoint Energy
  PublisherName: CenterPoint Energy
  ServiceCategory: Developer Tools / API
  ServiceName: CenterPoint Energy
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
name: Centerpoint Energy Finops
provider_name: CenterPoint Energy
provider_slug: centerpoint-energy
publisher_name: CenterPoint Energy
service_category: API
slug: centerpoint-energy-finops
source_filename: centerpoint-energy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CenterPoint Energy\nproviderId: centerpoint-energy\npublisherName: CenterPoint Energy\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Electricity\n  - Energy\n  - Fortune 500\n  - Green Button\n  - Natural Gas\n  - Smart Meter\n  - Usage Data\n  - Utility\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CenterPoint Energy API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CenterPoint Energy\n  ServiceCategory: Developer Tools / API\n  ProviderName: CenterPoint Energy\n  PublisherName: CenterPoint Energy\n  InvoiceIssuerName: CenterPoint Energy\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CenterPoint Energy Usage History Inquiry API\n    baseURL: ''\n    tags:\n      - Billing History\n      - Interval Data\n      - Smart Meter Texas\n      - Usage\n    serviceName: CenterPoint Energy Usage History Inquiry API\n    serviceCategory: API\n  - name: CenterPoint Energy Green Button Connect My Data\n    baseURL: ''\n    tags:\n      - Energy Usage\n      - Green Button\n      - Interval Data\n      - Open Data\n    serviceName: CenterPoint Energy Green Button Connect My Data\n    serviceCategory: API\n  - name: Centerpoint Connect Services API\n    baseURL: ''\n    tags:\n \
  \     - Field Service\n      - Integration\n      - Partner\n    serviceName: Centerpoint Connect Services API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centerpoint-energy/refs/heads/main/finops/centerpoint-energy-finops.yml
sources: []
specification: FinOps Framework
tags:
- Electricity
- Energy
- Fortune 500
- Green Button
- Natural Gas
- Smart Meter
- Usage Data
- Utility
- FinOps
- Cost Management
- FOCUS
---
