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
description: FinOps framework definition for the TIAA-CREF API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: TIAA-CREF
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: TIAA-CREF
  PublisherName: TIAA-CREF
  ServiceCategory: Developer Tools / API
  ServiceName: TIAA-CREF
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
name: Tiaa Cref Finops
provider_name: TIAA-CREF
provider_slug: tiaa-cref
publisher_name: TIAA-CREF
service_category: API
slug: tiaa-cref-finops
source_filename: tiaa-cref-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TIAA-CREF\nproviderId: tiaa-cref\npublisherName: TIAA-CREF\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - 403b\n  - Annuities\n  - Asset Management\n  - Fortune 100\n  - Higher Education\n  - Institutional\n  - Insurance\n  - Investments\n  - Non Profit\n  - Nuveen\n  - Retirement\n  - TIAA\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the TIAA-CREF API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: TIAA-CREF\n  ServiceCategory: Developer Tools / API\n  ProviderName: TIAA-CREF\n  PublisherName: TIAA-CREF\n  InvoiceIssuerName: TIAA-CREF\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: TIAA Retirement Plans\n    baseURL: https://www.tiaa.org/\n    tags:\n      - 403b\n      - 457b\n      - Annuities\n      - CREF\n      - IRA\n      - Mutual Funds\n      - Retirement\n      - TIAA\n    serviceName: TIAA Retirement Plans\n    serviceCategory: API\n  - name: TIAA Annuities\n    baseURL: ''\n    tags:\n      - Annuities\n      - Fixed Annuity\n      - Insurance\n      - Lifetime Income\n      - Retirement Income\n      - Variable Annuity\n    serviceName: TIAA Annuities\n    serviceCategory: API\n  - name: Nuveen Investments\n    baseURL: https://www.nuveen.com/\n    tags:\n      - Asset\
  \ Management\n      - ETFs\n      - Fixed Income\n      - Institutional\n      - Mutual Funds\n      - Nuveen\n      - Target Date\n    serviceName: Nuveen Investments\n    serviceCategory: API\n  - name: TIAA Wealth Management\n    baseURL: ''\n    tags:\n      - Banking\n      - Brokerage\n      - Financial Advice\n      - Insurance\n      - Investments\n      - Wealth Management\n    serviceName: TIAA Wealth Management\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tiaa-cref/refs/heads/main/finops/tiaa-cref-finops.yml
sources: []
specification: FinOps Framework
tags:
- 403b
- Annuities
- Asset Management
- Fortune 100
- Higher Education
- Institutional
- Insurance
- Investments
- Non Profit
- Nuveen
- Retirement
- TIAA
- FinOps
- Cost Management
- FOCUS
---
