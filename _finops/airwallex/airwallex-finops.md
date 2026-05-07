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
description: FinOps framework definition for the Airwallex API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Airwallex
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Airwallex
  PublisherName: Airwallex
  ServiceCategory: Developer Tools / API
  ServiceName: Airwallex
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
name: Airwallex Finops
provider_name: Airwallex
provider_slug: airwallex
publisher_name: Airwallex
service_category: API
slug: airwallex-finops
source_filename: airwallex-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Airwallex\nproviderId: airwallex\npublisherName: Airwallex\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cross-Border Payments\n  - FinTech\n  - Foreign Exchange\n  - Payments\n  - Global\n  - Embedded Finance\n  - Multi-Currency\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Airwallex API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n \
  \   description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Airwallex\n  ServiceCategory: Developer Tools / API\n  ProviderName: Airwallex\n  PublisherName: Airwallex\n  InvoiceIssuerName: Airwallex\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Airwallex Payment Acceptance API\n    baseURL: https://api.airwallex.com/api/v1\n    tags:\n      - Payments\n      - Checkout\n      - Cards\n      - Online Payments\n    serviceName: Airwallex Payment Acceptance API\n    serviceCategory: API\n  - name: Airwallex Global Accounts API\n    baseURL: https://api.airwallex.com/api/v1\n    tags:\n      - Accounts\n      - Multi-Currency\n      - Banking\n      - FX\n    serviceName: Airwallex Global Accounts API\n    serviceCategory: API\n  - name: Airwallex Payouts API\n    baseURL: https://api.airwallex.com/api/v1\n    tags:\n      - Payouts\n      - Cross-Border Payments\n      - Transfers\n      -\
  \ International\n    serviceName: Airwallex Payouts API\n    serviceCategory: API\n  - name: Airwallex FX API\n    baseURL: https://api.airwallex.com/api/v1\n    tags:\n      - Foreign Exchange\n      - Currency Conversion\n      - FX\n    serviceName: Airwallex FX API\n    serviceCategory: API\n  - name: Airwallex Issuing API\n    baseURL: https://api.airwallex.com/api/v1\n    tags:\n      - Cards\n      - Corporate Cards\n      - Issuing\n      - Expense Management\n    serviceName: Airwallex Issuing API\n    serviceCategory: API\n  - name: Airwallex Platform API\n    baseURL: https://api.airwallex.com/api/v1\n    tags:\n      - Embedded Finance\n      - Platform\n      - Marketplace\n      - Split Payments\n    serviceName: Airwallex Platform API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/airwallex/refs/heads/main/finops/airwallex-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cross-Border Payments
- FinTech
- Foreign Exchange
- Payments
- Global
- Embedded Finance
- Multi-Currency
- FinOps
- Cost Management
- FOCUS
---
