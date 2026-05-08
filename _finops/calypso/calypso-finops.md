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
description: FinOps framework definition for the Calypso API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Calypso
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Calypso
  PublisherName: Calypso
  ServiceCategory: Developer Tools / API
  ServiceName: Calypso
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
name: Calypso Finops
provider_name: Calypso
provider_slug: calypso
publisher_name: Calypso
service_category: API
slug: calypso-finops
source_filename: calypso-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Calypso\nproviderId: calypso\npublisherName: Calypso\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Capital Markets\n  - Collateral Management\n  - Enterprise Software\n  - Financial Technology\n  - Post-Trade Processing\n  - Risk Management\n  - Trading\n  - Treasury\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Calypso API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n     \
  \ real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing\
  \ and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Calypso\n  ServiceCategory: Developer Tools / API\n  ProviderName: Calypso\n  PublisherName: Calypso\n  InvoiceIssuerName: Calypso\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Calypso Core API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Capital Markets\n      - REST API\n      - Risk Management\n      - Trading\n    serviceName: Calypso Core API\n    serviceCategory: API\n  - name: Calypso Front Office API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Front Office\n      - Portfolio Management\n      - Pricing\n      - Trading\n    serviceName: Calypso Front Office API\n    serviceCategory: API\n  - name: Calypso Middle Office and Trading Risk API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Compliance\n      - Credit Risk\n      -\
  \ Market Risk\n      - Risk Management\n    serviceName: Calypso Middle Office and Trading Risk API\n    serviceCategory: API\n  - name: Calypso Treasury API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Asset Management\n      - Cash Management\n      - Liquidity\n      - Treasury\n    serviceName: Calypso Treasury API\n    serviceCategory: API\n  - name: Calypso Collateral, Margin and Securities Finance API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Collateral Management\n      - Margin\n      - Risk\n      - Securities Finance\n    serviceName: Calypso Collateral, Margin and Securities Finance API\n    serviceCategory: API\n  - name: Calypso Clearing API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Clearing\n      - Derivatives\n      - Exchange Traded\n      - OTC\n    serviceName: Calypso Clearing API\n    serviceCategory: API\n  - name: Calypso Post-Trade Processing API\n    baseURL: https://api.calypso.example.com/v1\n\
  \    tags:\n      - Accounting\n      - Back Office\n      - Post-Trade\n      - Settlement\n    serviceName: Calypso Post-Trade Processing API\n    serviceCategory: API\n  - name: Calypso Reserve and Monetary Policy Management API\n    baseURL: https://api.calypso.example.com/v1\n    tags:\n      - Central Banking\n      - Liquidity\n      - Monetary Policy\n      - Reserve Management\n    serviceName: Calypso Reserve and Monetary Policy Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/calypso/refs/heads/main/finops/calypso-finops.yml
sources: []
specification: FinOps Framework
tags:
- Capital Markets
- Collateral Management
- Enterprise Software
- Financial Technology
- Post-Trade Processing
- Risk Management
- Trading
- Treasury
- FinOps
- Cost Management
- FOCUS
---
