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
description: FinOps framework definition for the Connect-RPC API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Connect-RPC
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Connect-RPC
  PublisherName: Connect-RPC
  ServiceCategory: Developer Tools / API
  ServiceName: Connect-RPC
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
name: Connect Rpc Finops
provider_name: Connect-RPC
provider_slug: connect-rpc
publisher_name: Connect-RPC
service_category: API
slug: connect-rpc-finops
source_filename: connect-rpc-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Connect-RPC\nproviderId: connect-rpc\npublisherName: Connect-RPC\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Apache 2.0\n  - Buf\n  - Code Generation\n  - Connect Protocol\n  - gRPC\n  - gRPC-Web\n  - HTTP\n  - Open Source\n  - Protocol Buffers\n  - RPC\n  - SDKs\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Connect-RPC API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n   \
  \   real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      -\
  \ Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Connect-RPC\n  ServiceCategory: Developer Tools / API\n  ProviderName: Connect-RPC\n  PublisherName: Connect-RPC\n  InvoiceIssuerName: Connect-RPC\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: connect-go\n    baseURL: ''\n    tags:\n      - Go\n      - SDK\n    serviceName: connect-go\n    serviceCategory: API\n  - name: connect-es (Connect for ECMAScript)\n    baseURL: ''\n    tags:\n      - JavaScript\n      - SDK\n      - TypeScript\n    serviceName: connect-es (Connect for ECMAScript)\n    serviceCategory: API\n  - name: connect-swift\n    baseURL: ''\n    tags:\n      - iOS\n      - SDK\n      - Swift\n    serviceName: connect-swift\n    serviceCategory: API\n  - name: connect-kotlin\n    baseURL: ''\n    tags:\n      - Android\n      - JVM\n      - Kotlin\n      - SDK\n    serviceName:\
  \ connect-kotlin\n    serviceCategory: API\n  - name: connect-python\n    baseURL: ''\n    tags:\n      - Python\n      - SDK\n    serviceName: connect-python\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/connect-rpc/refs/heads/main/finops/connect-rpc-finops.yml
sources: []
specification: FinOps Framework
tags:
- Apache 2.0
- Buf
- Code Generation
- Connect Protocol
- gRPC
- gRPC-Web
- HTTP
- Open Source
- Protocol Buffers
- RPC
- SDKs
- FinOps
- Cost Management
- FOCUS
---
