---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coinbase-advanced-trade-openapi.yml
  format: yaml
  label: Coinbase Advanced Trade API
  slug: advanced-trade-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-advanced-trade-openapi.yml
- filename: coinbase-exchange-openapi.yml
  format: yaml
  label: Coinbase Exchange API
  slug: exchange-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-exchange-openapi.yml
- filename: coinbase-prime-openapi.yml
  format: yaml
  label: Coinbase Prime API
  slug: prime-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-prime-openapi.yml
- filename: coinbase-onramp-openapi.yml
  format: yaml
  label: Coinbase Onramp API
  slug: onramp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-onramp-openapi.yml
- filename: coinbase-commerce-openapi.yml
  format: yaml
  label: Coinbase Commerce API
  slug: commerce-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/openapi/coinbase-commerce-openapi.yml
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
description: FinOps framework definition for the Coinbase API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Coinbase
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Coinbase
  PublisherName: Coinbase
  ServiceCategory: Developer Tools / API
  ServiceName: Coinbase
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
name: Coinbase Finops
provider_name: Coinbase
provider_slug: coinbase
publisher_name: Coinbase
service_category: API
slug: coinbase-finops
source_filename: coinbase-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Coinbase\nproviderId: coinbase\npublisherName: Coinbase\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Blockchain\n  - Cryptocurrency\n  - Custody\n  - Exchange\n  - Onramp\n  - Payments\n  - Trading\n  - Wallet\n  - Web3\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Coinbase API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Coinbase\n  ServiceCategory: Developer Tools / API\n  ProviderName: Coinbase\n  PublisherName: Coinbase\n  InvoiceIssuerName: Coinbase\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n \
  \   unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Coinbase Advanced Trade API\n    baseURL: https://api.coinbase.com\n    tags:\n      - Automation\n      - Cryptocurrency\n      - Market Data\n      - Orders\n      - Trading\n    serviceName: Coinbase Advanced Trade API\n    serviceCategory: API\n  - name: Coinbase Exchange API\n    baseURL: https://api.exchange.coinbase.com\n    tags:\n      - Cryptocurrency\n      - Exchange\n      - FIX\n      - Market Data\n      - Trading\n      - WebSocket\n    serviceName: Coinbase Exchange API\n    serviceCategory: API\n  - name: Coinbase Prime API\n    baseURL: https://api.prime.coinbase.com\n    tags:\n      - Cryptocurrency\n      - Custody\n      - Institutional\n    \
  \  - Prime Brokerage\n      - Trading\n    serviceName: Coinbase Prime API\n    serviceCategory: API\n  - name: Coinbase Onramp API\n    baseURL: https://api.developer.coinbase.com\n    tags:\n      - Cryptocurrency\n      - Fiat\n      - Offramp\n      - Onramp\n      - Payments\n    serviceName: Coinbase Onramp API\n    serviceCategory: API\n  - name: Coinbase Commerce API\n    baseURL: https://api.commerce.coinbase.com\n    tags:\n      - Checkout\n      - Commerce\n      - Cryptocurrency\n      - Invoices\n      - Payments\n    serviceName: Coinbase Commerce API\n    serviceCategory: API\n  - name: Coinbase Wallet SDK\n    baseURL: ''\n    tags:\n      - Cryptocurrency\n      - DApps\n      - SDK\n      - Wallet\n      - Web3\n    serviceName: Coinbase Wallet SDK\n    serviceCategory: API\n  - name: Coinbase Data API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Blockchain\n      - Cryptocurrency\n      - Market Data\n    serviceName: Coinbase Data API\n    serviceCategory:\
  \ API\n  - name: Coinbase AgentKit\n    baseURL: ''\n    tags:\n      - Agents\n      - AI\n      - Blockchain\n      - SDK\n      - Wallet\n    serviceName: Coinbase AgentKit\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coinbase/refs/heads/main/finops/coinbase-finops.yml
sources: []
specification: FinOps Framework
tags:
- Blockchain
- Cryptocurrency
- Custody
- Exchange
- Onramp
- Payments
- Trading
- Wallet
- Web3
- FinOps
- Cost Management
- FOCUS
---
