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
description: FinOps framework definition for the Barclays API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Barclays
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Barclays
  PublisherName: Barclays
  ServiceCategory: Developer Tools / API
  ServiceName: Barclays
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
name: Barclays Finops
provider_name: Barclays
provider_slug: barclays
publisher_name: Barclays
service_category: API
slug: barclays-finops
source_filename: barclays-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Barclays\nproviderId: barclays\npublisherName: Barclays\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Credit Cards\n  - Finance\n  - Open Banking\n  - Payments\n  - PSD2\n  - UK Banking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Barclays API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Barclays\n  ServiceCategory: Developer Tools / API\n  ProviderName: Barclays\n  PublisherName: Barclays\n  InvoiceIssuerName: Barclays\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Barclays Smartpay Web Payment API\n    baseURL: ''\n    tags:\n      - E-Commerce\n      - Payments\n      - Smartpay\n    serviceName: Barclays Smartpay Web Payment API\n    serviceCategory: API\n  - name: Barclays Bank Ireland Confirmation of Funds API\n    baseURL: ''\n    tags:\n      - Confirmation of Funds\n      - Ireland\n      - Open Banking\n      - PSD2\n    serviceName: Barclays Bank Ireland Confirmation of Funds API\n    serviceCategory: API\n  - name: Barclays Account and Transactions API\n    baseURL: ''\n    tags:\n      - Accounts\n      - Open Banking\n      - Transactions\n    serviceName: Barclays Account and Transactions API\n    serviceCategory: API\n  - name: Barclays Bank\
  \ Ireland Account Information API\n    baseURL: ''\n    tags:\n      - Accounts\n      - Ireland\n      - Open Banking\n      - PSD2\n    serviceName: Barclays Bank Ireland Account Information API\n    serviceCategory: API\n  - name: Barclays Bank Ireland Payment Initiation API\n    baseURL: ''\n    tags:\n      - Ireland\n      - Open Banking\n      - Payment Initiation\n      - PSD2\n    serviceName: Barclays Bank Ireland Payment Initiation API\n    serviceCategory: API\n  - name: Barclays Confirmation of Funds API\n    baseURL: ''\n    tags:\n      - Confirmation of Funds\n      - Open Banking\n    serviceName: Barclays Confirmation of Funds API\n    serviceCategory: API\n  - name: Barclays Consent API\n    baseURL: ''\n    tags:\n      - Consent\n      - Open Banking\n      - Privacy\n    serviceName: Barclays Consent API\n    serviceCategory: API\n  - name: Barclays Dynamic Client Registration API\n    baseURL: ''\n    tags:\n      - Client Registration\n      - Open Banking\n   \
  \   - Security\n    serviceName: Barclays Dynamic Client Registration API\n    serviceCategory: API\n  - name: Barclays Event Notification API\n    baseURL: ''\n    tags:\n      - Events\n      - Notifications\n      - Open Banking\n      - Webhooks\n    serviceName: Barclays Event Notification API\n    serviceCategory: API\n  - name: Barclays Payment Initiation API\n    baseURL: ''\n    tags:\n      - Open Banking\n      - Payment Initiation\n      - Payments\n    serviceName: Barclays Payment Initiation API\n    serviceCategory: API\n  - name: Barclays ATM Locator API\n    baseURL: ''\n    tags:\n      - ATM\n      - Location\n      - Branch Finder\n    serviceName: Barclays ATM Locator API\n    serviceCategory: API\n  - name: Barclays Branch Locator API\n    baseURL: ''\n    tags:\n      - Branch Finder\n      - Location\n    serviceName: Barclays Branch Locator API\n    serviceCategory: API\n  - name: Barclays FCA Service Metrics API\n    baseURL: ''\n    tags:\n      - Compliance\n\
  \      - FCA\n      - Metrics\n      - Regulatory\n    serviceName: Barclays FCA Service Metrics API\n    serviceCategory: API\n  - name: Barclays Product Details API\n    baseURL: ''\n    tags:\n      - Open Banking\n      - Products\n    serviceName: Barclays Product Details API\n    serviceCategory: API\n  - name: Barclays Accounts API\n    baseURL: ''\n    tags:\n      - Accounts\n      - Open Banking\n    serviceName: Barclays Accounts API\n    serviceCategory: API\n  - name: Barclays Authentication API\n    baseURL: ''\n    tags:\n      - Authentication\n      - OAuth\n      - Security\n    serviceName: Barclays Authentication API\n    serviceCategory: API\n  - name: Barclays Card Application API\n    baseURL: ''\n    tags:\n      - Card Applications\n      - Credit Cards\n    serviceName: Barclays Card Application API\n    serviceCategory: API\n  - name: Barclays Cryptography Key Exchange API\n    baseURL: ''\n    tags:\n      - Cryptography\n      - Security\n    serviceName: Barclays\
  \ Cryptography Key Exchange API\n    serviceCategory: API\n  - name: Barclays Digital Wallet API\n    baseURL: ''\n    tags:\n      - Digital Wallet\n      - Mobile Payments\n      - Payments\n    serviceName: Barclays Digital Wallet API\n    serviceCategory: API\n  - name: Barclays Payments API\n    baseURL: ''\n    tags:\n      - Payments\n    serviceName: Barclays Payments API\n    serviceCategory: API\n  - name: Barclays Rewards Loyalty Sync API\n    baseURL: ''\n    tags:\n      - Loyalty\n      - Rewards\n    serviceName: Barclays Rewards Loyalty Sync API\n    serviceCategory: API\n  - name: Barclays Rewards Pay with Points API\n    baseURL: ''\n    tags:\n      - Loyalty\n      - Rewards\n    serviceName: Barclays Rewards Pay with Points API\n    serviceCategory: API\n  - name: Barclays Transactions API\n    baseURL: ''\n    tags:\n      - Open Banking\n      - Transactions\n    serviceName: Barclays Transactions API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per\
  \ 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/barclays/refs/heads/main/finops/barclays-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Credit Cards
- Finance
- Open Banking
- Payments
- PSD2
- UK Banking
- FinOps
- Cost Management
- FOCUS
---
