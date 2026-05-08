---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.yaml
  format: yaml
  label: Refinitiv Data Platform APIs
  slug: ''
  spec_type: OpenAPI
  url: https://api.refinitiv.com/streaming-pricing/docs/swagger.yaml
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
description: FinOps framework definition for the Refinitiv Eikon API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Refinitiv Eikon
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Refinitiv Eikon
  PublisherName: Refinitiv Eikon
  ServiceCategory: Developer Tools / API
  ServiceName: Refinitiv Eikon
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
name: Refinitiv Eikon Finops
provider_name: Refinitiv Eikon
provider_slug: refinitiv-eikon
publisher_name: Refinitiv Eikon
service_category: API
slug: refinitiv-eikon-finops
source_filename: refinitiv-eikon-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Refinitiv Eikon\nproviderId: refinitiv-eikon\npublisherName: Refinitiv Eikon\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Financial Data\n  - Financial News\n  - Market Data\n  - Real-Time Data\n  - Trading\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Refinitiv Eikon API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n  \
  \  description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the\
  \ FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Refinitiv Eikon\n  ServiceCategory: Developer Tools / API\n  ProviderName: Refinitiv Eikon\n  PublisherName: Refinitiv Eikon\n  InvoiceIssuerName: Refinitiv Eikon\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Eikon Data API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Financial Data\n      - Market Data\n      - Python\n      - Time Series\n    serviceName: Eikon Data API\n    serviceCategory: API\n  - name: Refinitiv Data Platform APIs\n    baseURL: https://api.refinitiv.com\n    tags:\n      - ESG\n      - Market Data\n      - News\n      - REST API\n    serviceName: Refinitiv Data Platform APIs\n    serviceCategory: API\n  - name: LSEG Messenger Bot SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Chatbot\n      - Collaboration\n      - Compliance\n      - Messaging\n    serviceName: LSEG Messenger\
  \ Bot SDK\n    serviceCategory: API\n  - name: Messenger Side by Side API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Collaboration\n      - Integration\n      - Messaging\n    serviceName: Messenger Side by Side API\n    serviceCategory: API\n  - name: Refinitiv Data Library for Python\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Data Library\n      - Financial Data\n      - Python\n      - SDK\n    serviceName: Refinitiv Data Library for Python\n    serviceCategory: API\n  - name: Refinitiv Data Library for TypeScript\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Data Library\n      - JavaScript\n      - SDK\n      - TypeScript\n    serviceName: Refinitiv Data Library for TypeScript\n    serviceCategory: API\n  - name: Refinitiv Data Library for .NET\n    baseURL: https://api.refinitiv.com\n    tags:\n      - .NET\n      - C#\n      - Data Library\n      - SDK\n    serviceName: Refinitiv Data Library for .NET\n    serviceCategory: API\n  -\
  \ name: Datastream Web Service API\n    baseURL: https://product.datastream.com\n    tags:\n      - Financial Data\n      - Historical Data\n      - SOAP\n      - Time Series\n    serviceName: Datastream Web Service API\n    serviceCategory: API\n  - name: LSEG WebSocket API\n    baseURL: wss://api.refinitiv.com\n    tags:\n      - Market Data\n      - Real-Time\n      - Streaming\n      - WebSocket\n    serviceName: LSEG WebSocket API\n    serviceCategory: API\n  - name: Real-Time Java SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Java\n      - Real-Time\n      - SDK\n      - Streaming\n    serviceName: Real-Time Java SDK\n    serviceCategory: API\n  - name: Real-Time C/C++ SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - C++\n      - Low Latency\n      - Real-Time\n      - SDK\n    serviceName: Real-Time C/C++ SDK\n    serviceCategory: API\n  - name: Real-Time C# SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - .NET\n      - C#\n      -\
  \ Real-Time\n      - SDK\n    serviceName: Real-Time C# SDK\n    serviceCategory: API\n  - name: Eikon Side by Side Interoperability API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Deprecated\n      - Desktop Integration\n      - Interoperability\n      - Workflow\n    serviceName: Eikon Side by Side Interoperability API\n    serviceCategory: API\n  - name: Workspace Web Side by Side API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Desktop Integration\n      - Interoperability\n      - Web\n      - Workspace\n    serviceName: Workspace Web Side by Side API\n    serviceCategory: API\n  - name: Workspace SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Application Development\n      - SDK\n      - UI Components\n      - Workspace\n    serviceName: Workspace SDK\n    serviceCategory: API\n  - name: LSEG DataScope Select REST API\n    baseURL: https://selectapi.datascope.refinitiv.com/RestApi/v1\n    tags:\n      - Corporate Actions\n      - Data\
  \ Extraction\n      - Reference Data\n      - REST API\n    serviceName: LSEG DataScope Select REST API\n    serviceCategory: API\n  - name: LSEG Tick History REST API\n    baseURL: https://selectapi.datascope.refinitiv.com/RestApi/v1\n    tags:\n      - Historical Data\n      - Market Data\n      - REST API\n      - Tick Data\n    serviceName: LSEG Tick History REST API\n    serviceCategory: API\n  - name: PermID Entity Search API\n    baseURL: https://api-eit.refinitiv.com/permid/search\n    tags:\n      - Entity Search\n      - Identifiers\n      - Open Data\n      - Symbology\n    serviceName: PermID Entity Search API\n    serviceCategory: API\n  - name: PermID Record Matching API\n    baseURL: https://api-eit.refinitiv.com/permid/match\n    tags:\n      - Concordance\n      - Entity Matching\n      - Identifiers\n      - Open Data\n    serviceName: PermID Record Matching API\n    serviceCategory: API\n  - name: Intelligent Tagging API\n    baseURL: https://api-eit.refinitiv.com/permid/calais\n\
  \    tags:\n      - Entity Extraction\n      - NLP\n      - Tagging\n      - Text Analytics\n    serviceName: Intelligent Tagging API\n    serviceCategory: API\n  - name: Refinitiv Knowledge Direct API\n    baseURL: https://api.rkd.refinitiv.com\n    tags:\n      - Market Data\n      - Portals\n      - SOAP\n      - Wealth Management\n    serviceName: Refinitiv Knowledge Direct API\n    serviceCategory: API\n  - name: Symbology API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Concordance\n      - Identifiers\n      - Reference Data\n      - Symbology\n    serviceName: Symbology API\n    serviceCategory: API\n  - name: Search API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Discovery\n      - Instruments\n      - Search\n      - Wealth Management\n    serviceName: Search API\n    serviceCategory: API\n  - name: Research API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Buy-Side\n      - Reports\n      - Research\n      - Sell-Side\n    serviceName:\
  \ Research API\n    serviceCategory: API\n  - name: News API for Wealth\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Financial News\n      - News\n      - Wealth Management\n    serviceName: News API for Wealth\n    serviceCategory: API\n  - name: Funds API for Wealth\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Funds\n      - Lipper\n      - Performance\n      - Wealth Management\n    serviceName: Funds API for Wealth\n    serviceCategory: API\n  - name: Estimates API for Wealth\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Consensus\n      - Estimates\n      - Forecasts\n      - Wealth Management\n    serviceName: Estimates API for Wealth\n    serviceCategory: API\n  - name: Ownership API for Wealth\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Holdings\n      - Ownership\n      - Shareholders\n      - Wealth Management\n    serviceName: Ownership API for Wealth\n    serviceCategory: API\n  - name: Filings API\n    baseURL: https://api.refinitiv.com\n\
  \    tags:\n      - Compliance\n      - Filings\n      - Regulatory\n      - SEC\n    serviceName: Filings API\n    serviceCategory: API\n  - name: World-Check One API\n    baseURL: https://rms-world-check-one-api.thomsonreuters.com\n    tags:\n      - AML\n      - Compliance\n      - Risk\n      - Screening\n    serviceName: World-Check One API\n    serviceCategory: API\n  - name: World-Check Verify API\n    baseURL: https://api.refinitiv.com\n    tags:\n      - Compliance\n      - Payments\n      - Real-Time\n      - Screening\n    serviceName: World-Check Verify API\n    serviceCategory: API\n  - name: App Studio Web SDK\n    baseURL: https://api.refinitiv.com\n    tags:\n      - App Development\n      - Embedded Apps\n      - HTML5\n      - JavaScript\n    serviceName: App Studio Web SDK\n    serviceCategory: API\n  - name: Eikon COM APIs for Microsoft Office\n    baseURL: https://api.refinitiv.com\n    tags:\n      - COM\n      - Deprecated\n      - Microsoft Office\n      - VBA\n\
  \    serviceName: Eikon COM APIs for Microsoft Office\n    serviceCategory: API\n  - name: Eikon .NET APIs\n    baseURL: https://api.refinitiv.com\n    tags:\n      - .NET\n      - Custom Applications\n      - Deprecated\n      - Desktop\n    serviceName: Eikon .NET APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/refinitiv-eikon/refs/heads/main/finops/refinitiv-eikon-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Financial Data
- Financial News
- Market Data
- Real-Time Data
- Trading
- FinOps
- Cost Management
- FOCUS
---
