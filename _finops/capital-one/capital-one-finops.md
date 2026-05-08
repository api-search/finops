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
description: FinOps framework definition for the Capital One API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Capital One
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Capital One
  PublisherName: Capital One
  ServiceCategory: Developer Tools / API
  ServiceName: Capital One
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
name: Capital One Finops
provider_name: Capital One
provider_slug: capital-one
publisher_name: Capital One
service_category: API
slug: capital-one-finops
source_filename: capital-one-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Capital One\nproviderId: capital-one\npublisherName: Capital One\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Auto Finance\n  - Authorizations\n  - Banking\n  - Credit Cards\n  - Credit Offers\n  - DevExchange\n  - Financial Services\n  - OAuth 2.0\n  - Payments\n  - Rewards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Capital One API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in\
  \ near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Capital One\n  ServiceCategory: Developer Tools / API\n  ProviderName: Capital One\n  PublisherName: Capital One\n  InvoiceIssuerName: Capital One\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Capital One Account Lookup API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Account Lookup API\n    serviceCategory: API\n  - name: Capital One Authorizations API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Authorizations API\n    serviceCategory: API\n  - name: Capital One Credit Offers API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Credit Offers API\n    serviceCategory: API\n  - name: Capital One Customer Transactions\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Customer Transactions\n    serviceCategory: API\n  - name: Capital One\
  \ Data Protection and Client Authentication Public Key Sharing API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Data Protection and Client Authentication Public Key Sharing API\n    serviceCategory: API\n  - name: Capital One Digital Auto Financing Credit Application API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Digital Auto Financing Credit Application API\n    serviceCategory: API\n  - name: Capital One Enhanced Decisioning Data API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Enhanced Decisioning Data API\n    serviceCategory: API\n  - name: Capital One In-Store Credit Card Payments API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One In-Store Credit Card Payments API\n    serviceCategory: API\n  - name: Capital One POS Credit Card Application API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One POS Credit Card Application API\n    serviceCategory: API\n  - name: Capital One Partner Account Summary API\n    baseURL:\
  \ ''\n    tags: []\n    serviceName: Capital One Partner Account Summary API\n    serviceCategory: API\n  - name: Capital One Pre-Application Orchestrator API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Pre-Application Orchestrator API\n    serviceCategory: API\n  - name: Capital One Real-Time Proactive Prescreen API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Real-Time Proactive Prescreen API\n    serviceCategory: API\n  - name: Capital One Retrieve Consumer Bank Products API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Retrieve Consumer Bank Products API\n    serviceCategory: API\n  - name: Capital One Shop with Rewards API\n    baseURL: ''\n    tags: []\n    serviceName: Capital One Shop with Rewards API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target:\
  \ TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/capital-one/refs/heads/main/finops/capital-one-finops.yml
sources: []
specification: FinOps Framework
tags:
- Auto Finance
- Authorizations
- Banking
- Credit Cards
- Credit Offers
- DevExchange
- Financial Services
- OAuth 2.0
- Payments
- Rewards
- FinOps
- Cost Management
- FOCUS
---
