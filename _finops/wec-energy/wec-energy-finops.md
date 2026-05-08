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
description: FinOps framework definition for the WEC Energy Group API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: WEC Energy Group
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: WEC Energy Group
  PublisherName: WEC Energy Group
  ServiceCategory: Developer Tools / API
  ServiceName: WEC Energy Group
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
name: Wec Energy Finops
provider_name: WEC Energy Group
provider_slug: wec-energy
publisher_name: WEC Energy Group
service_category: API
slug: wec-energy-finops
source_filename: wec-energy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: WEC Energy Group\nproviderId: wec-energy\npublisherName: WEC Energy Group\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Energy\n  - Electric Utility\n  - Fortune 500\n  - Green Button\n  - Illinois\n  - Michigan\n  - Minnesota\n  - Natural Gas\n  - NYSE\n  - Utility\n  - Wisconsin\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the WEC Energy Group API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: WEC Energy Group\n  ServiceCategory: Developer Tools / API\n  ProviderName: WEC Energy Group\n  PublisherName: WEC Energy Group\n  InvoiceIssuerName: WEC Energy Group\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: WEC Energy Group Customer Portal API\n    baseURL: ''\n    tags:\n      - Account Management\n      - Bill Payment\n      - Customer Portal\n      - Energy Usage\n      - Outage Reporting\n    serviceName: WEC Energy Group Customer Portal API\n    serviceCategory: API\n  - name: Green Button Energy Usage Data API\n    baseURL: ''\n    tags:\n      - Energy Data\n      - Green Button\n      - ESPI\n      - OAuth2\n      - Smart Meter\n      - Usage Data\n    serviceName: Green Button Energy Usage Data API\n    serviceCategory: API\n  - name: We Energies Outage Map API\n    baseURL:\
  \ ''\n    tags:\n      - Electricity\n      - GIS\n      - Outage Map\n      - Real-Time\n      - Wisconsin\n    serviceName: We Energies Outage Map API\n    serviceCategory: API\n  - name: Peoples Gas Customer Service API\n    baseURL: ''\n    tags:\n      - Account Management\n      - Bill Payment\n      - Chicago\n      - Illinois\n      - Natural Gas\n    serviceName: Peoples Gas Customer Service API\n    serviceCategory: API\n  - name: WEC Energy Group Investor Relations API\n    baseURL: ''\n    tags:\n      - Financial Data\n      - Investor Relations\n      - NYSE\n      - SEC Filings\n      - Stock Data\n    serviceName: WEC Energy Group Investor Relations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wec-energy/refs/heads/main/finops/wec-energy-finops.yml
sources: []
specification: FinOps Framework
tags:
- Energy
- Electric Utility
- Fortune 500
- Green Button
- Illinois
- Michigan
- Minnesota
- Natural Gas
- NYSE
- Utility
- Wisconsin
- FinOps
- Cost Management
- FOCUS
---
