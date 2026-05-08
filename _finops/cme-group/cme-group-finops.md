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
description: FinOps framework definition for the CME Group API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CME Group
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CME Group
  PublisherName: CME Group
  ServiceCategory: Developer Tools / API
  ServiceName: CME Group
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
name: Cme Group Finops
provider_name: CME Group
provider_slug: cme-group
publisher_name: CME Group
service_category: API
slug: cme-group-finops
source_filename: cme-group-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CME Group\nproviderId: cme-group\npublisherName: CME Group\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Capital Markets\n  - Derivatives\n  - Exchange\n  - Financial Markets\n  - Futures\n  - Market Data\n  - Options\n  - Reference Data\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CME Group API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  -\
  \ name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CME Group\n  ServiceCategory: Developer Tools / API\n  ProviderName: CME Group\n  PublisherName: CME Group\n  InvoiceIssuerName: CME Group\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CME Reference Data API\n    baseURL: ''\n    tags:\n      - Instruments\n      - OAuth\n      - Products\n      - Reference Data\n      - REST\n    serviceName: CME Reference Data API\n    serviceCategory: API\n  - name: Real-Time Futures and Options Data API\n    baseURL: ''\n    tags:\n      - Futures\n      - Market Data\n      - Options\n      - Real-Time\n      - REST\n    serviceName: Real-Time Futures and Options Data API\n    serviceCategory: API\n  - name: CME Term SOFR API\n    baseURL: ''\n    tags:\n      - Benchmarks\n      - Interest Rates\n      - REST\n      - SOFR\n    serviceName: CME Term SOFR API\n    serviceCategory:\
  \ API\n  - name: CME FedWatch API\n    baseURL: ''\n    tags:\n      - Fed Funds\n      - Market-Implied Probabilities\n      - Monetary Policy\n      - REST\n    serviceName: CME FedWatch API\n    serviceCategory: API\n  - name: Greeks and Implied Volatility API\n    baseURL: ''\n    tags:\n      - Greeks\n      - Implied Volatility\n      - Options\n      - REST\n    serviceName: Greeks and Implied Volatility API\n    serviceCategory: API\n  - name: EUR/USD Cross Currency Basis Index API\n    baseURL: ''\n    tags:\n      - FX\n      - Index\n      - REST\n    serviceName: EUR/USD Cross Currency Basis Index API\n    serviceCategory: API\n  - name: CME ClearPort API\n    baseURL: ''\n    tags:\n      - Clearing\n      - OTC\n      - Trade Submission\n    serviceName: CME ClearPort API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost /\
  \ active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cme-group/refs/heads/main/finops/cme-group-finops.yml
sources: []
specification: FinOps Framework
tags:
- Capital Markets
- Derivatives
- Exchange
- Financial Markets
- Futures
- Market Data
- Options
- Reference Data
- Trading
- FinOps
- Cost Management
- FOCUS
---
