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
description: FinOps framework definition for the Authorize.net API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Authorize.net
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Authorize.net
  PublisherName: Authorize.net
  ServiceCategory: Developer Tools / API
  ServiceName: Authorize.net
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
name: Authorize Net Finops
provider_name: Authorize.net
provider_slug: authorize-net
publisher_name: Authorize.net
service_category: API
slug: authorize-net-finops
source_filename: authorize-net-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Authorize.net\nproviderId: authorize-net\npublisherName: Authorize.net\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accept.js\n  - Credit Cards\n  - eChecks\n  - Fraud Detection\n  - Payment Gateway\n  - Payments\n  - Recurring Billing\n  - Transactions\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Authorize.net API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Authorize.net\n  ServiceCategory: Developer Tools / API\n  ProviderName: Authorize.net\n  PublisherName: Authorize.net\n  InvoiceIssuerName: Authorize.net\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n   \
  \ description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Authorize.net Payment API\n    baseURL: https://api.authorize.net/xml/v1/request.api\n    tags:\n      - Credit Cards\n      - eChecks\n      - Payment Gateway\n      - Transactions\n    serviceName: Authorize.net Payment API\n    serviceCategory: API\n  - name: Authorize.net Recurring Billing API\n    baseURL: https://api.authorize.net/xml/v1/request.api\n    tags:\n      - Payment Gateway\n      - Recurring Billing\n      - Subscriptions\n    serviceName: Authorize.net Recurring Billing API\n    serviceCategory: API\n  - name: Authorize.net Customer Profiles API\n    baseURL: https://api.authorize.net/xml/v1/request.api\n\
  \    tags:\n      - Customer Profiles\n      - Payment Gateway\n      - Tokenization\n    serviceName: Authorize.net Customer Profiles API\n    serviceCategory: API\n  - name: Authorize.net Webhooks\n    baseURL: https://api.authorize.net/rest/v1\n    tags:\n      - Events\n      - Payment Gateway\n      - Webhooks\n    serviceName: Authorize.net Webhooks\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/authorize-net/refs/heads/main/finops/authorize-net-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accept.js
- Credit Cards
- eChecks
- Fraud Detection
- Payment Gateway
- Payments
- Recurring Billing
- Transactions
- FinOps
- Cost Management
- FOCUS
---
