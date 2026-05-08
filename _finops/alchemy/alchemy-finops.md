---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alchemy-token-api-openapi.yml
  format: yaml
  label: Alchemy Token API
  slug: token-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-token-api-openapi.yml
- filename: alchemy-transfers-api-openapi.yml
  format: yaml
  label: Alchemy Transfers API
  slug: transfers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-transfers-api-openapi.yml
- filename: alchemy-gas-manager-api-openapi.yml
  format: yaml
  label: Alchemy Gas Manager API
  slug: gas-manager
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-gas-manager-api-openapi.yml
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
description: FinOps framework definition for the Alchemy API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Alchemy
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Alchemy
  PublisherName: Alchemy
  ServiceCategory: Developer Tools / API
  ServiceName: Alchemy
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
name: Alchemy Finops
provider_name: Alchemy
provider_slug: alchemy
publisher_name: Alchemy
service_category: API
slug: alchemy-finops
source_filename: alchemy-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alchemy\nproviderId: alchemy\npublisherName: Alchemy\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Web3\n  - Blockchain\n  - RPC\n  - NFT\n  - Indexing\n  - Account Abstraction\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Alchemy API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Alchemy\n  ServiceCategory: Developer Tools / API\n  ProviderName: Alchemy\n  PublisherName: Alchemy\n  InvoiceIssuerName: Alchemy\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Alchemy Node API (JSON-RPC)\n    baseURL: https://{network}.g.alchemy.com/v2/{apiKey}\n    tags:\n      - JSON-RPC\n      - WebSocket\n      - Multi-chain\n    serviceName: Alchemy Node API (JSON-RPC)\n    serviceCategory: API\n  - name: Alchemy NFT API\n    baseURL: https://{network}.g.alchemy.com/nft/v3/{apiKey}\n    tags:\n      - REST\n      - NFT\n    serviceName: Alchemy NFT API\n    serviceCategory: API\n  - name: Alchemy Token API\n    baseURL: https://{network}.g.alchemy.com/v2/{apiKey}\n    tags:\n      - REST\n      - Token\n    serviceName: Alchemy Token API\n    serviceCategory: API\n  - name: Alchemy Transfers API\n    baseURL: https://{network}.g.alchemy.com/v2/{apiKey}\n    tags:\n      - REST\n     \
  \ - Transfers\n    serviceName: Alchemy Transfers API\n    serviceCategory: API\n  - name: Alchemy Portfolio API\n    baseURL: https://api.g.alchemy.com/data/v1/{apiKey}\n    tags:\n      - REST\n      - Portfolio\n    serviceName: Alchemy Portfolio API\n    serviceCategory: API\n  - name: Alchemy Prices API\n    baseURL: https://api.g.alchemy.com/prices/v1/{apiKey}\n    tags:\n      - REST\n      - Prices\n    serviceName: Alchemy Prices API\n    serviceCategory: API\n  - name: Alchemy Webhooks (Notify)\n    baseURL: https://dashboard.alchemy.com/api\n    tags:\n      - REST\n      - Webhooks\n    serviceName: Alchemy Webhooks (Notify)\n    serviceCategory: API\n  - name: Alchemy Bundler API (ERC-4337)\n    baseURL: https://{network}.g.alchemy.com/v2/{apiKey}\n    tags:\n      - JSON-RPC\n      - ERC-4337\n      - Account Abstraction\n    serviceName: Alchemy Bundler API (ERC-4337)\n    serviceCategory: API\n  - name: Alchemy Gas Manager API\n    baseURL: https://manage.g.alchemy.com/api/gasManager/policy\n\
  \    tags:\n      - JSON-RPC\n      - Paymaster\n      - Account Abstraction\n    serviceName: Alchemy Gas Manager API\n    serviceCategory: API\n  - name: Alchemy Simulation API\n    baseURL: https://{network}.g.alchemy.com/v2/{apiKey}\n    tags:\n      - JSON-RPC\n      - Simulation\n    serviceName: Alchemy Simulation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/finops/alchemy-finops.yml
sources: []
specification: FinOps Framework
tags:
- Web3
- Blockchain
- RPC
- NFT
- Indexing
- Account Abstraction
- FinOps
- Cost Management
- FOCUS
---
