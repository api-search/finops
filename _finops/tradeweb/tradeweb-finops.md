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
description: FinOps framework definition for the Tradeweb API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tradeweb
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Tradeweb
  PublisherName: Tradeweb
  ServiceCategory: Developer Tools / API
  ServiceName: Tradeweb
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
name: Tradeweb Finops
provider_name: Tradeweb
provider_slug: tradeweb
publisher_name: Tradeweb
service_category: API
slug: tradeweb-finops
source_filename: tradeweb-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tradeweb\nproviderId: tradeweb\npublisherName: Tradeweb\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Electronic Trading\n  - Financial Markets\n  - Fixed Income\n  - Market Data\n  - OTC Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Tradeweb API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Tradeweb\n  ServiceCategory: Developer Tools / API\n  ProviderName: Tradeweb\n  PublisherName: Tradeweb\n  InvoiceIssuerName: Tradeweb\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Tradeweb Trading API\n    baseURL: https://api.tradeweb.com\n    tags:\n      - Electronic Trading\n      - Execution\n      - Fixed Income\n      - RFQ\n    serviceName: Tradeweb Trading API\n    serviceCategory: API\n  - name: Tradeweb Python API\n    baseURL: https://api.tradeweb.com\n    tags:\n      - Automation\n      - Python\n      - Quantitative Trading\n      - SDK\n    serviceName: Tradeweb Python API\n    serviceCategory: API\n  - name: Tradeweb FIX API\n    baseURL: fix://tradeweb.com\n    tags:\n      - FIX Protocol\n      - Integration\n      - OMS\n      - STP\n    serviceName: Tradeweb FIX API\n    serviceCategory: API\n  - name: Tradeweb Market Data API\n    baseURL: https://api.tradeweb.com/data\n\
  \    tags:\n      - Benchmark Data\n      - Market Data\n      - OTC Pricing\n      - Real-Time Data\n    serviceName: Tradeweb Market Data API\n    serviceCategory: API\n  - name: Tradeweb APA Trade Reporting API\n    baseURL: https://apa.tradeweb.com/api\n    tags:\n      - APA\n      - Compliance\n      - MiFID II\n      - Trade Reporting\n      - Transparency\n    serviceName: Tradeweb APA Trade Reporting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tradeweb/refs/heads/main/finops/tradeweb-finops.yml
sources: []
specification: FinOps Framework
tags:
- Electronic Trading
- Financial Markets
- Fixed Income
- Market Data
- OTC Trading
- FinOps
- Cost Management
- FOCUS
---
