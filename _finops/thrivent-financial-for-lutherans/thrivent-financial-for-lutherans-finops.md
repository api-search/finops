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
description: FinOps framework definition for the Thrivent Financial API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Thrivent Financial
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Thrivent Financial
  PublisherName: Thrivent Financial
  ServiceCategory: Developer Tools / API
  ServiceName: Thrivent Financial
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
name: Thrivent Financial For Lutherans Finops
provider_name: Thrivent Financial
provider_slug: thrivent-financial-for-lutherans
publisher_name: Thrivent Financial
service_category: API
slug: thrivent-financial-for-lutherans-finops
source_filename: thrivent-financial-for-lutherans-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Thrivent Financial\nproviderId: thrivent-financial-for-lutherans\npublisherName: Thrivent Financial\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Annuities\n  - Banking\n  - ETFs\n  - Financial Advice\n  - Financial Planning\n  - Fortune 500\n  - Generosity\n  - Insurance\n  - Investments\n  - Mutual Funds\n  - Non Profit\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Thrivent Financial API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs\
  \ visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n   \
  \   - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Thrivent Financial\n  ServiceCategory: Developer Tools / API\n  ProviderName: Thrivent Financial\n  PublisherName: Thrivent Financial\n  InvoiceIssuerName: Thrivent Financial\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Thrivent Financial Planning\n    baseURL: https://www.thrivent.com/\n    tags:\n      - Annuities\n      - Banking\n      - Financial Advice\n      - Financial Planning\n      - Insurance\n      - Investments\n      - Retirement\n    serviceName: Thrivent Financial Planning\n    serviceCategory: API\n  - name: Thrivent Insurance\n    baseURL: ''\n    tags:\n      - Disability Income Insurance\n      - Insurance\n      - Life Insurance\n      - Long Term Care\n    serviceName: Thrivent Insurance\n    serviceCategory:\
  \ API\n  - name: Thrivent Investments\n    baseURL: ''\n    tags:\n      - Annuities\n      - ETFs\n      - Investments\n      - Managed Accounts\n      - Mutual Funds\n    serviceName: Thrivent Investments\n    serviceCategory: API\n  - name: Thrivent Bank\n    baseURL: ''\n    tags:\n      - Banking\n      - Church Loans\n      - Savings\n    serviceName: Thrivent Bank\n    serviceCategory: API\n  - name: Thrivent Charitable\n    baseURL: ''\n    tags:\n      - Charitable Giving\n      - Community Impact\n      - Donations\n      - Generosity\n      - Non Profit\n    serviceName: Thrivent Charitable\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/thrivent-financial-for-lutherans/refs/heads/main/finops/thrivent-financial-for-lutherans-finops.yml
sources: []
specification: FinOps Framework
tags:
- Annuities
- Banking
- ETFs
- Financial Advice
- Financial Planning
- Fortune 500
- Generosity
- Insurance
- Investments
- Mutual Funds
- Non Profit
- FinOps
- Cost Management
- FOCUS
---
