---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cftc-cot-openapi.yml
  format: yaml
  label: CFTC Commitments of Traders SODA API
  slug: cftc-cot-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/commodity-futures-trading-commission/refs/heads/main/openapi/cftc-cot-openapi.yml
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
description: FinOps framework definition for the Commodity Futures Trading Commission API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Commodity Futures Trading Commission
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Commodity Futures Trading Commission
  PublisherName: Commodity Futures Trading Commission
  ServiceCategory: Developer Tools / API
  ServiceName: Commodity Futures Trading Commission
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
name: Commodity Futures Trading Commission Finops
provider_name: Commodity Futures Trading Commission
provider_slug: commodity-futures-trading-commission
publisher_name: Commodity Futures Trading Commission
service_category: API
slug: commodity-futures-trading-commission-finops
source_filename: commodity-futures-trading-commission-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Commodity Futures Trading Commission\nproviderId: commodity-futures-trading-commission\npublisherName: Commodity Futures Trading Commission\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - CFTC\n  - Commitments of Traders\n  - Federal Government\n  - Financial\n  - Futures\n  - Open Data\n  - SODA\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Commodity Futures Trading Commission API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Commodity Futures Trading Commission\n  ServiceCategory: Developer Tools / API\n  ProviderName: Commodity Futures Trading Commission\n  PublisherName: Commodity Futures Trading Commission\n  InvoiceIssuerName: Commodity Futures Trading Commission\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API\
  \ requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CFTC Commitments of Traders SODA API\n    baseURL: https://publicreporting.cftc.gov/resource\n    tags:\n      - COT\n      - Open Data\n      - SODA\n      - Trading\n    serviceName: CFTC Commitments of Traders SODA API\n    serviceCategory: API\n  - name: CFTC Swap Data Repositories\n    baseURL: https://www.cftc.gov\n    tags:\n      - Dodd-Frank\n      - Swaps\n      - SDR\n      - Reporting\n    serviceName: CFTC Swap Data Repositories\n\
  \    serviceCategory: API\n  - name: CFTC Bank Participation and Large Trader Reports\n    baseURL: https://www.cftc.gov\n    tags:\n      - Bank Participation\n      - Large Trader\n      - Reporting\n    serviceName: CFTC Bank Participation and Large Trader Reports\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/commodity-futures-trading-commission/refs/heads/main/finops/commodity-futures-trading-commission-finops.yml
sources: []
specification: FinOps Framework
tags:
- CFTC
- Commitments of Traders
- Federal Government
- Financial
- Futures
- Open Data
- SODA
- Trading
- FinOps
- Cost Management
- FOCUS
---
