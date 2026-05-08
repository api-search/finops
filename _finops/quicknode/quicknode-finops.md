---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: quicknode-streams-openapi.yml
  format: yaml
  label: QuickNode Streams
  slug: streams
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-streams-openapi.yml
- filename: quicknode-ipfs-openapi.yml
  format: yaml
  label: QuickNode IPFS API
  slug: ipfs
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-ipfs-openapi.yml
- filename: quicknode-key-value-store-openapi.yml
  format: yaml
  label: QuickNode Key-Value Store
  slug: kv-store
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-key-value-store-openapi.yml
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
description: FinOps framework definition for the QuickNode API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: QuickNode
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: QuickNode
  PublisherName: QuickNode
  ServiceCategory: Developer Tools / API
  ServiceName: QuickNode
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
name: Quicknode Finops
provider_name: QuickNode
provider_slug: quicknode
publisher_name: QuickNode
service_category: API
slug: quicknode-finops
source_filename: quicknode-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: QuickNode\nproviderId: quicknode\npublisherName: QuickNode\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Web3\n  - Blockchain\n  - RPC\n  - Streams\n  - IPFS\n  - Multi-chain\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the QuickNode API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: QuickNode\n  ServiceCategory: Developer Tools / API\n  ProviderName: QuickNode\n  PublisherName: QuickNode\n  InvoiceIssuerName: QuickNode\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n   \
  \ dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: QuickNode Core RPC API\n    baseURL: https://{endpoint-name}.{network}.quiknode.pro/{token}\n    tags:\n      - JSON-RPC\n      - WebSocket\n      - gRPC\n      - Multi-chain\n    serviceName: QuickNode Core RPC API\n    serviceCategory: API\n  - name: QuickNode Streams\n    baseURL: https://api.quicknode.com/streams/rest/v1\n    tags:\n      - REST\n      - Streaming\n    serviceName: QuickNode Streams\n    serviceCategory: API\n  - name: QuickNode Webhooks\n    baseURL: https://api.quicknode.com/webhooks/rest/v1\n    tags:\n      - REST\n      - Webhooks\n    serviceName: QuickNode Webhooks\n    serviceCategory: API\n  - name: QuickNode IPFS API\n    baseURL: https://api.quicknode.com/ipfs/rest/v1\n \
  \   tags:\n      - REST\n      - IPFS\n    serviceName: QuickNode IPFS API\n    serviceCategory: API\n  - name: QuickNode Key-Value Store\n    baseURL: https://api.quicknode.com/kv/rest/v1\n    tags:\n      - REST\n      - Storage\n    serviceName: QuickNode Key-Value Store\n    serviceCategory: API\n  - name: QuickNode Marketplace Add-ons\n    baseURL: https://{endpoint}.quiknode.pro/{token}\n    tags:\n      - Marketplace\n      - Add-ons\n    serviceName: QuickNode Marketplace Add-ons\n    serviceCategory: API\n  - name: QuickNode Functions\n    baseURL: https://api.quicknode.com/functions/rest/v1\n    tags:\n      - REST\n      - Serverless\n    serviceName: QuickNode Functions\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/finops/quicknode-finops.yml
sources: []
specification: FinOps Framework
tags:
- Web3
- Blockchain
- RPC
- Streams
- IPFS
- Multi-chain
- FinOps
- Cost Management
- FOCUS
---
