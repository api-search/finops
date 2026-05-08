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
description: FinOps framework definition for the Bloomberg Professional Service API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bloomberg Professional Service
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bloomberg Professional Service
  PublisherName: Bloomberg Professional Service
  ServiceCategory: Developer Tools / API
  ServiceName: Bloomberg Professional Service
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
name: Bloomberg Professional Service Finops
provider_name: Bloomberg Professional Service
provider_slug: bloomberg-professional-service
publisher_name: Bloomberg Professional Service
service_category: API
slug: bloomberg-professional-service-finops
source_filename: bloomberg-professional-service-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bloomberg Professional Service\nproviderId: bloomberg-professional-service\npublisherName: Bloomberg Professional Service\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Cloud\n  - Data Management\n  - Enterprise\n  - Financial Services\n  - Market Data\n  - Open Source\n  - Real-Time Data\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bloomberg Professional Service API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption\
  \ costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n\
  \      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bloomberg Professional Service\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bloomberg Professional Service\n  PublisherName: Bloomberg Professional Service\n  InvoiceIssuerName: Bloomberg Professional Service\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bloomberg Data License API\n    baseURL: https://www.bloomberg.com/professional/product/data-license/\n    tags:\n      - Cloud\n      - ESG\n      - Financial Data\n      - Fundamentals\n      - Historical Data\n      - Market Data\n      - Reference Data\n    serviceName: Bloomberg Data License API\n    serviceCategory: API\n  - name: Bloomberg API (BLPAPI)\n    baseURL: https://www.bloomberg.com/professional/support/api-library/\n    tags:\n      - Desktop API\n\
  \      - Real-Time Data\n      - SDK\n      - Terminal Integration\n      - Trading\n    serviceName: Bloomberg API (BLPAPI)\n    serviceCategory: API\n  - name: Bloomberg SAPI (Server API)\n    baseURL: https://www.bloomberg.com/professional/products/data/data-connectivity/server-api/\n    tags:\n      - Cloud\n      - Enterprise\n      - Integration\n      - Market Data\n      - Server API\n    serviceName: Bloomberg SAPI (Server API)\n    serviceCategory: API\n  - name: Bloomberg B-PIPE\n    baseURL: https://www.bloomberg.com/professional/product/b-pipe/\n    tags:\n      - Algorithmic Trading\n      - Cloud\n      - Low Latency\n      - Market Data Feed\n      - Real-Time\n      - Streaming\n    serviceName: Bloomberg B-PIPE\n    serviceCategory: API\n  - name: Bloomberg Hypermedia API (HAPI)\n    baseURL: https://www.bloomberg.com/professional/products/data/data-management/data-license/\n    tags:\n      - Alternative Data\n      - Data License\n      - Pricing Data\n      - Reference\
  \ Data\n      - Regulatory Data\n      - REST API\n    serviceName: Bloomberg Hypermedia API (HAPI)\n    serviceCategory: API\n  - name: Bloomberg HTTP API\n    baseURL: https://github.com/bloomberg/blpapi-http\n    tags:\n      - Historical Data\n      - HTTP\n      - Open Source\n      - Real-Time Data\n      - REST API\n      - WebSockets\n    serviceName: Bloomberg HTTP API\n    serviceCategory: API\n  - name: Bloomberg Terminal Connect API\n    baseURL: https://www.bloomberg.com/professional/support/api-library/\n    tags:\n      - Desktop\n      - Launchpad\n      - Synchronization\n      - Terminal Integration\n    serviceName: Bloomberg Terminal Connect API\n    serviceCategory: API\n  - name: Bloomberg App Portal\n    baseURL: https://www.bloomberg.com/professional/solutions/asset-management/developer/\n    tags:\n      - App Marketplace\n      - Developer Platform\n      - Terminal Extensions\n      - Third Party Apps\n    serviceName: Bloomberg App Portal\n    serviceCategory:\
  \ API\n  - name: Bloomberg Data License Plus (DL+)\n    baseURL: https://www.bloomberg.com/professional/products/data/data-management/dms/\n    tags:\n      - Cloud\n      - Data License\n      - Data Management\n      - Enterprise\n    serviceName: Bloomberg Data License Plus (DL+)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-professional-service/refs/heads/main/finops/bloomberg-professional-service-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Cloud
- Data Management
- Enterprise
- Financial Services
- Market Data
- Open Source
- Real-Time Data
- Trading
- FinOps
- Cost Management
- FOCUS
---
