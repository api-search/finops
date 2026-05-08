---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: red5-server-api-openapi.yml
  format: yaml
  label: Red5 Pro Server API
  slug: server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-server-api-openapi.yml
- filename: red5-stream-manager-2-openapi.yml
  format: yaml
  label: Red5 Pro Stream Manager 2.0 API
  slug: stream-manager-2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-stream-manager-2-openapi.yml
- filename: red5-brew-mixer-api-openapi.yml
  format: yaml
  label: Red5 Pro Brew Mixer API
  slug: brew-mixer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-brew-mixer-api-openapi.yml
- filename: red5-restreamer-api-openapi.yml
  format: yaml
  label: Red5 Pro Restreamer API
  slug: restreamer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/openapi/red5-restreamer-api-openapi.yml
- filename: red5-webrtc-streaming-asyncapi.yml
  format: yaml
  label: Red5 Pro WebRTC SDK
  slug: webrtc-sdk
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/asyncapi/red5-webrtc-streaming-asyncapi.yml
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
description: FinOps framework definition for the Red5 API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Red5
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Red5
  PublisherName: Red5
  ServiceCategory: Developer Tools / API
  ServiceName: Red5
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
name: Red5 Finops
provider_name: Red5
provider_slug: red5
publisher_name: Red5
service_category: API
slug: red5-finops
source_filename: red5-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Red5\nproviderId: red5\npublisherName: Red5\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Live Streaming\n  - Media\n  - Real-Time\n  - RTMP\n  - Streaming\n  - Video\n  - WebRTC\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Red5 API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Red5\n  ServiceCategory: Developer Tools / API\n  ProviderName: Red5\n  PublisherName: Red5\n  InvoiceIssuerName: Red5\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Red5 Pro Server API\n    baseURL: http://localhost:5080/api/v1\n    tags:\n      - Media\n      - Real-Time\n      - REST\n      - Server Management\n      - Streaming\n    serviceName: Red5 Pro Server API\n    serviceCategory: API\n  - name: Red5 Pro Stream Manager 2.0 API\n    baseURL: https://streammanager.example.com/as/v1\n    tags:\n      - Autoscaling\n      - Cluster Management\n      - Media\n      - REST\n      - Streaming\n      - WebRTC\n      - WHEP\n      - WHIP\n    serviceName: Red5 Pro Stream Manager 2.0 API\n    serviceCategory: API\n  - name: Red5 Pro Brew Mixer API\n    baseURL: https://api.example.com/brewmixer/2.0\n    tags:\n      - Audio\n      - Composition\n      - Media\n      - Mixing\n      - REST\n\
  \      - Streaming\n      - Video\n    serviceName: Red5 Pro Brew Mixer API\n    serviceCategory: API\n  - name: Red5 Pro Restreamer API\n    baseURL: https://api.example.com\n    tags:\n      - Media\n      - REST\n      - Restreaming\n      - RTMP\n      - Social Media\n      - Streaming\n    serviceName: Red5 Pro Restreamer API\n    serviceCategory: API\n  - name: Red5 Pro WebRTC SDK\n    baseURL: https://api.example.com\n    tags:\n      - JavaScript\n      - Media\n      - SDK\n      - Streaming\n      - WebRTC\n      - WHEP\n      - WHIP\n    serviceName: Red5 Pro WebRTC SDK\n    serviceCategory: API\n  - name: Red5 Core SDK\n    baseURL: https://api.example.com\n    tags:\n      - Desktop\n      - Linux\n      - Media\n      - Native\n      - SDK\n      - Streaming\n      - Windows\n    serviceName: Red5 Core SDK\n    serviceCategory: API\n  - name: Red5 Pro iOS Streaming SDK\n    baseURL: https://api.example.com\n    tags:\n      - iOS\n      - Media\n      - Mobile\n      - SDK\n\
  \      - Streaming\n      - Swift\n    serviceName: Red5 Pro iOS Streaming SDK\n    serviceCategory: API\n  - name: Red5 Pro Android Streaming SDK\n    baseURL: https://api.example.com\n    tags:\n      - Android\n      - Java\n      - Media\n      - Mobile\n      - SDK\n      - Streaming\n    serviceName: Red5 Pro Android Streaming SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/red5/refs/heads/main/finops/red5-finops.yml
sources: []
specification: FinOps Framework
tags:
- Live Streaming
- Media
- Real-Time
- RTMP
- Streaming
- Video
- WebRTC
- FinOps
- Cost Management
- FOCUS
---
