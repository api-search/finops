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
description: FinOps framework definition for the Checkout.com API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Checkout.com
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Checkout.com
  PublisherName: Checkout.com
  ServiceCategory: Developer Tools / API
  ServiceName: Checkout.com
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
name: Checkout Com Finops
provider_name: Checkout.com
provider_slug: checkout-com
publisher_name: Checkout.com
service_category: API
slug: checkout-com-finops
source_filename: checkout-com-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Checkout.com\nproviderId: checkout-com\npublisherName: Checkout.com\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Fintech\n  - Payments\n  - Cards\n  - Acquiring\n  - Cross-Border\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Checkout.com API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Checkout.com\n  ServiceCategory: Developer Tools / API\n  ProviderName: Checkout.com\n  PublisherName: Checkout.com\n  InvoiceIssuerName: Checkout.com\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Checkout.com Payments API\n    baseURL: https://api.checkout.com\n    tags:\n      - Payments\n      - Cards\n    serviceName: Checkout.com Payments API\n    serviceCategory: API\n  - name: Checkout.com Payouts API\n    baseURL: https://api.checkout.com\n    tags:\n      - Payouts\n    serviceName: Checkout.com Payouts API\n    serviceCategory: API\n  - name: Checkout.com Payment Sessions & Flow API\n    baseURL: https://api.checkout.com\n    tags:\n      - Sessions\n      - Flow\n      - SCA\n    serviceName: Checkout.com Payment Sessions & Flow API\n    serviceCategory: API\n  - name: Checkout.com Payment Links & Hosted Payments API\n    baseURL: https://api.checkout.com\n    tags:\n      - Payment\
  \ Links\n      - Hosted\n    serviceName: Checkout.com Payment Links & Hosted Payments API\n    serviceCategory: API\n  - name: Checkout.com Issuing API\n    baseURL: https://api.checkout.com\n    tags:\n      - Issuing\n      - Cards\n    serviceName: Checkout.com Issuing API\n    serviceCategory: API\n  - name: Checkout.com Tokenization & Instruments API\n    baseURL: https://api.checkout.com\n    tags:\n      - Tokenization\n      - Vault\n    serviceName: Checkout.com Tokenization & Instruments API\n    serviceCategory: API\n  - name: Checkout.com Disputes & Risk API\n    baseURL: https://api.checkout.com\n    tags:\n      - Disputes\n      - Fraud\n      - Risk\n    serviceName: Checkout.com Disputes & Risk API\n    serviceCategory: API\n  - name: Checkout.com Forex API\n    baseURL: https://api.checkout.com\n    tags:\n      - FX\n      - Forex\n    serviceName: Checkout.com Forex API\n    serviceCategory: API\n  - name: Checkout.com Apple Pay & Google Pay API\n    baseURL: https://api.checkout.com\n\
  \    tags:\n      - Wallets\n      - Apple Pay\n      - Google Pay\n    serviceName: Checkout.com Apple Pay & Google Pay API\n    serviceCategory: API\n  - name: Checkout.com Network Tokens API\n    baseURL: https://api.checkout.com\n    tags:\n      - Network Tokens\n    serviceName: Checkout.com Network Tokens API\n    serviceCategory: API\n  - name: Checkout.com Transfers & Balances API\n    baseURL: https://api.checkout.com\n    tags:\n      - Transfers\n      - Balances\n    serviceName: Checkout.com Transfers & Balances API\n    serviceCategory: API\n  - name: Checkout.com Reporting & Financial Actions API\n    baseURL: https://api.checkout.com\n    tags:\n      - Reporting\n      - Reconciliation\n    serviceName: Checkout.com Reporting & Financial Actions API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/checkout-com/refs/heads/main/finops/checkout-com-finops.yml
sources: []
specification: FinOps Framework
tags:
- Fintech
- Payments
- Cards
- Acquiring
- Cross-Border
- FinOps
- Cost Management
- FOCUS
---
