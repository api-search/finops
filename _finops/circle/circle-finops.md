---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: developer-controlled-wallets.yaml
  format: yaml
  label: Developer-Controlled Wallets
  slug: developer-controlled-wallets
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/developer-controlled-wallets.yaml
- filename: user-controlled-wallets.yaml
  format: yaml
  label: User-Controlled Wallets
  slug: user-controlled-wallets
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/user-controlled-wallets.yaml
- filename: cctp.yaml
  format: yaml
  label: Cross-Chain Transfer Protocol (CCTP)
  slug: cctp
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/cctp.yaml
- filename: gateway.yaml
  format: yaml
  label: Circle Gateway
  slug: gateway
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/gateway.yaml
- filename: smart-contract-platform.yaml
  format: yaml
  label: Smart Contract Platform
  slug: smart-contract-platform
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/smart-contract-platform.yaml
- filename: cpn-ofi.yaml
  format: yaml
  label: Circle Payments Network (CPN)
  slug: cpn
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/cpn-ofi.yaml
- filename: compliance.yaml
  format: yaml
  label: Compliance Engine
  slug: compliance-engine
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/compliance.yaml
- filename: stablefx.yaml
  format: yaml
  label: StableFX
  slug: stablefx
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/stablefx.yaml
- filename: xreserve.yaml
  format: yaml
  label: xReserve
  slug: xreserve
  spec_type: OpenAPI
  url: https://developers.circle.com/openapi/xreserve.yaml
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
description: FinOps framework definition for the Circle API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Circle
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Circle
  PublisherName: Circle
  ServiceCategory: Developer Tools / API
  ServiceName: Circle
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
name: Circle Finops
provider_name: Circle
provider_slug: circle
publisher_name: Circle
service_category: API
slug: circle-finops
source_filename: circle-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Circle\nproviderId: circle\npublisherName: Circle\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Blockchain\n  - Compliance\n  - Cross-Chain\n  - Currency\n  - Money\n  - Payments\n  - Stablecoin\n  - Transfers\n  - USDC\n  - Wallets\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Circle API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n \
  \   description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Circle\n  ServiceCategory: Developer Tools / API\n  ProviderName: Circle\n  PublisherName: Circle\n  InvoiceIssuerName: Circle\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API\
  \ responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Developer-Controlled Wallets\n    baseURL: https://api.circle.com/v1/w3s\n    tags:\n      - Custody\n      - USDC\n      - Wallets\n    serviceName: Developer-Controlled Wallets\n    serviceCategory: API\n  - name: User-Controlled Wallets\n    baseURL: https://api.circle.com/v1/w3s\n    tags:\n      - Custody\n      - End-User\n      - USDC\n      - Wallets\n    serviceName: User-Controlled Wallets\n    serviceCategory: API\n  - name: Gas Station and Paymaster\n    baseURL: https://api.circle.com/v1/w3s\n    tags:\n      - Gas Sponsorship\n      - Paymaster\n      - USDC\n    serviceName: Gas Station and Paymaster\n    serviceCategory: API\n  - name: Cross-Chain\
  \ Transfer Protocol (CCTP)\n    baseURL: ''\n    tags:\n      - Bridging\n      - Cross-Chain\n      - USDC\n    serviceName: Cross-Chain Transfer Protocol (CCTP)\n    serviceCategory: API\n  - name: Circle Gateway\n    baseURL: ''\n    tags:\n      - Cross-Chain\n      - Liquidity\n      - USDC\n    serviceName: Circle Gateway\n    serviceCategory: API\n  - name: Smart Contract Platform\n    baseURL: https://api.circle.com/v1/w3s\n    tags:\n      - Contracts\n      - EVM\n      - Web3\n    serviceName: Smart Contract Platform\n    serviceCategory: API\n  - name: Circle Payments Network (CPN)\n    baseURL: ''\n    tags:\n      - Cross-Border\n      - Payments\n      - Settlement\n    serviceName: Circle Payments Network (CPN)\n    serviceCategory: API\n  - name: Compliance Engine\n    baseURL: ''\n    tags:\n      - AML\n      - Compliance\n      - Risk\n    serviceName: Compliance Engine\n    serviceCategory: API\n  - name: StableFX\n    baseURL: ''\n    tags:\n      - Arc\n      - FX\n\
  \      - Trading\n    serviceName: StableFX\n    serviceCategory: API\n  - name: xReserve\n    baseURL: ''\n    tags:\n      - Issuance\n      - Reserves\n      - Stablecoin\n    serviceName: xReserve\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circle/refs/heads/main/finops/circle-finops.yml
sources: []
specification: FinOps Framework
tags:
- Blockchain
- Compliance
- Cross-Chain
- Currency
- Money
- Payments
- Stablecoin
- Transfers
- USDC
- Wallets
- FinOps
- Cost Management
- FOCUS
---
