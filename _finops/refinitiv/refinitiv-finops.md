---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: refinitiv-data-platform-openapi.yml
  format: yaml
  label: Refinitiv Data Platform (RDP) API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-data-platform-openapi.yml
- filename: refinitiv-real-time-websocket-asyncapi.yml
  format: yaml
  label: Refinitiv Real-Time WebSocket API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/asyncapi/refinitiv-real-time-websocket-asyncapi.yml
- filename: refinitiv-datascope-select-openapi.yml
  format: yaml
  label: LSEG DataScope Select - REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-datascope-select-openapi.yml
- filename: refinitiv-world-check-one-openapi.yml
  format: yaml
  label: World-Check One API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-world-check-one-openapi.yml
- filename: refinitiv-qual-id-openapi.yml
  format: yaml
  label: Qual-ID API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-qual-id-openapi.yml
- filename: refinitiv-permid-entity-search-openapi.yml
  format: yaml
  label: PermID Entity Search API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/openapi/refinitiv-permid-entity-search-openapi.yml
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
description: FinOps framework definition for the Refinitiv API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Refinitiv
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Refinitiv
  PublisherName: Refinitiv
  ServiceCategory: Developer Tools / API
  ServiceName: Refinitiv
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
name: Refinitiv Finops
provider_name: Refinitiv
provider_slug: refinitiv
publisher_name: Refinitiv
service_category: API
slug: refinitiv-finops
source_filename: refinitiv-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Refinitiv\nproviderId: refinitiv\npublisherName: Refinitiv\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Refinitiv API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be\
  \ allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Refinitiv\n  ServiceCategory: Developer Tools / API\n  ProviderName: Refinitiv\n  PublisherName: Refinitiv\n  InvoiceIssuerName: Refinitiv\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n\
  \    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Refinitiv Data Platform (RDP) API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Analytics\n      - Financial Data\n      - Market Data\n      - Streaming\n    serviceName: Refinitiv Data Platform (RDP) API\n    serviceCategory: API\n  - name: Refinitiv Data Library for Python\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Data Library\n      - Financial Data\n      - Python\n      - SDK\n    serviceName: Refinitiv Data Library for Python\n    serviceCategory: API\n  - name: Refinitiv Data Library for .NET\n    baseURL: https://api.refinitiv.com\n    tags:\n      - .NET\n      - Data Library\n      - Financial Data\n      - SDK\n    serviceName: Refinitiv Data Library for .NET\n    serviceCategory: API\n  - name: Refinitiv Data Platform Libraries\n    baseURL: https://api.refinitiv.com\n\
  \    tags:\n      - Financial Data\n      - JavaScript\n      - Libraries\n      - SDK\n    serviceName: Refinitiv Data Platform Libraries\n    serviceCategory: API\n  - name: Eikon Data API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Desktop\n      - Eikon\n      - Financial Data\n      - Python\n    serviceName: Eikon Data API\n    serviceCategory: API\n  - name: Refinitiv Real-Time WebSocket API\n    baseURL: wss://api.refinitiv.com\n    tags:\n      - Market Data\n      - Real-Time\n      - Streaming\n      - WebSocket\n    serviceName: Refinitiv Real-Time WebSocket API\n    serviceCategory: API\n  - name: Refinitiv Real-Time SDK - Java\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Java\n      - Real-Time\n      - SDK\n      - Streaming\n    serviceName: Refinitiv Real-Time SDK - Java\n    serviceCategory: API\n  - name: Refinitiv Real-Time SDK - C/C++\n    baseURL: https://api.refinitiv.com\n    tags:\n      - C++\n      - Real-Time\n      - SDK\n   \
  \   - Streaming\n    serviceName: Refinitiv Real-Time SDK - C/C++\n    serviceCategory: API\n  - name: Refinitiv News API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Content\n      - Media\n      - News\n      - Research\n    serviceName: Refinitiv News API\n    serviceCategory: API\n  - name: Refinitiv ESG API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Analytics\n      - Environmental\n      - ESG\n      - Sustainability\n    serviceName: Refinitiv ESG API\n    serviceCategory: API\n  - name: LSEG DataScope Select - REST API\n    baseURL: https://selectapi.datascope.lseg.com/RestApi/v1\n    tags:\n      - Data Extraction\n      - Historical Data\n      - Pricing\n      - Reference Data\n    serviceName: LSEG DataScope Select - REST API\n    serviceCategory: API\n  - name: LSEG DataScope Select - SOAP API\n    baseURL: https://selectapi.datascope.lseg.com\n    tags:\n      - Data Extraction\n      - Legacy\n      - Reference Data\n      - SOAP\n    serviceName:\
  \ LSEG DataScope Select - SOAP API\n    serviceCategory: API\n  - name: LSEG Tick History REST API\n    baseURL: https://selectapi.datascope.lseg.com/RestApi/v1\n    tags:\n      - High Frequency\n      - Historical Data\n      - Tick Data\n      - Trading\n    serviceName: LSEG Tick History REST API\n    serviceCategory: API\n  - name: Datastream Web Service API\n    baseURL: https://product.datastream.com\n    tags:\n      - Datastream\n      - Economic Data\n      - Historical Data\n      - Time Series\n    serviceName: Datastream Web Service API\n    serviceCategory: API\n  - name: World-Check One API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Compliance\n      - KYC\n      - Risk Intelligence\n      - Screening\n    serviceName: World-Check One API\n    serviceCategory: API\n  - name: Qual-ID API\n    baseURL: https://api.refinitiv.com/verification/v1\n    tags:\n      - Compliance\n      - Document Verification\n      - Identity Verification\n      - KYC\n    serviceName:\
  \ Qual-ID API\n    serviceCategory: API\n  - name: LSEG Due Diligence Portal API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Compliance\n      - Due Diligence\n      - Risk\n      - Screening\n    serviceName: LSEG Due Diligence Portal API\n    serviceCategory: API\n  - name: Refinitiv Knowledge Direct API (RKD)\n    baseURL: https://api.rkd.refinitiv.com\n    tags:\n      - Financial Data\n      - News\n      - Pricing\n      - Wealth Management\n    serviceName: Refinitiv Knowledge Direct API (RKD)\n    serviceCategory: API\n  - name: PermID Entity Search API\n    baseURL: https://api-eit.refinitiv.com\n    tags:\n      - Entity Search\n      - Open Data\n      - PermID\n      - Symbology\n    serviceName: PermID Entity Search API\n    serviceCategory: API\n  - name: Intelligent Tagging RESTful API\n    baseURL: https://api-eit.refinitiv.com\n    tags:\n      - Entity Recognition\n      - NLP\n      - Tagging\n      - Text Analytics\n    serviceName: Intelligent Tagging\
  \ RESTful API\n    serviceCategory: API\n  - name: Workspace SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Application Development\n      - Desktop\n      - SDK\n      - Workspace\n    serviceName: Workspace SDK\n    serviceCategory: API\n  - name: Workspace Web Side by Side API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Desktop\n      - Interoperability\n      - Web\n      - Workspace\n    serviceName: Workspace Web Side by Side API\n    serviceCategory: API\n  - name: FX Trading - Spot and Forwards Matching API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - FIX Protocol\n      - Forwards\n      - FX Trading\n      - Spot\n    serviceName: FX Trading - Spot and Forwards Matching API\n    serviceCategory: API\n  - name: FX Trading - NDF Matching API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Derivatives\n      - FIX Protocol\n      - FX Trading\n      - NDF\n    serviceName: FX Trading - NDF Matching API\n    serviceCategory:\
  \ API\n  - name: FX Market Data - NDF Matching API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - FX Market Data\n      - NDF\n      - Real-Time\n      - Trading\n    serviceName: FX Market Data - NDF Matching API\n    serviceCategory: API\n  - name: FX Reference Data API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - FX\n      - Reference Data\n      - Trading\n      - Venue\n    serviceName: FX Reference Data API\n    serviceCategory: API\n  - name: FX Participant Insight Reporting API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Analytics\n      - FX\n      - Reporting\n      - Trading\n    serviceName: FX Participant Insight Reporting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/refinitiv/refs/heads/main/finops/refinitiv-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
