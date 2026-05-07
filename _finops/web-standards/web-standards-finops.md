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
description: FinOps framework definition for the Web Standards API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Web Standards
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Web Standards
  PublisherName: Web Standards
  ServiceCategory: Developer Tools / API
  ServiceName: Web Standards
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
name: Web Standards Finops
provider_name: Web Standards
provider_slug: web-standards
publisher_name: Web Standards
service_category: API
slug: web-standards-finops
source_filename: web-standards-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Web Standards\nproviderId: web-standards\npublisherName: Web Standards\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Browser Compatibility\n  - CSS\n  - HTML\n  - Interoperability\n  - JavaScript\n  - Standards\n  - Web APIs\n  - Web Development\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Web Standards API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  -\
  \ name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n\
  \  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Web Standards\n  ServiceCategory: Developer Tools / API\n  ProviderName: Web Standards\n  PublisherName: Web Standards\n  InvoiceIssuerName: Web Standards\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: WHATWG HTML Living Standard\n    baseURL: ''\n    tags:\n      - HTML\n      - Living Standard\n      - WHATWG\n      - Web APIs\n    serviceName: WHATWG HTML Living Standard\n    serviceCategory: API\n  - name: WHATWG Fetch Living Standard\n    baseURL: ''\n    tags:\n      - Fetch API\n      - HTTP\n      - Living Standard\n      - Networking\n      - WHATWG\n    serviceName: WHATWG Fetch Living Standard\n    serviceCategory: API\n  - name: WHATWG DOM Living Standard\n    baseURL: ''\n    tags:\n      - DOM\n      - Living Standard\n      - WHATWG\n      - Web APIs\n    serviceName: WHATWG DOM Living Standard\n \
  \   serviceCategory: API\n  - name: WHATWG URL Living Standard\n    baseURL: ''\n    tags:\n      - Living Standard\n      - URL\n      - WHATWG\n    serviceName: WHATWG URL Living Standard\n    serviceCategory: API\n  - name: WHATWG Streams Living Standard\n    baseURL: ''\n    tags:\n      - Living Standard\n      - Streaming\n      - WHATWG\n      - Web APIs\n    serviceName: WHATWG Streams Living Standard\n    serviceCategory: API\n  - name: WHATWG WebSockets Living Standard\n    baseURL: ''\n    tags:\n      - Living Standard\n      - Real-Time\n      - WebSockets\n      - WHATWG\n    serviceName: WHATWG WebSockets Living Standard\n    serviceCategory: API\n  - name: WHATWG Storage Living Standard\n    baseURL: ''\n    tags:\n      - Living Standard\n      - Storage\n      - WHATWG\n      - Web APIs\n    serviceName: WHATWG Storage Living Standard\n    serviceCategory: API\n  - name: WHATWG Encoding Living Standard\n    baseURL: ''\n    tags:\n      - Character Encoding\n      - Living\
  \ Standard\n      - WHATWG\n    serviceName: WHATWG Encoding Living Standard\n    serviceCategory: API\n  - name: WHATWG Notifications API Living Standard\n    baseURL: ''\n    tags:\n      - Living Standard\n      - Notifications\n      - WHATWG\n    serviceName: WHATWG Notifications API Living Standard\n    serviceCategory: API\n  - name: WHATWG File System Living Standard\n    baseURL: ''\n    tags:\n      - File System\n      - Living Standard\n      - Storage\n      - WHATWG\n    serviceName: WHATWG File System Living Standard\n    serviceCategory: API\n  - name: W3C CSS Specifications\n    baseURL: ''\n    tags:\n      - CSS\n      - Layout\n      - Styling\n      - W3C\n    serviceName: W3C CSS Specifications\n    serviceCategory: API\n  - name: W3C Web Authentication (WebAuthn)\n    baseURL: ''\n    tags:\n      - Authentication\n      - Security\n      - W3C\n      - WebAuthn\n    serviceName: W3C Web Authentication (WebAuthn)\n    serviceCategory: API\n  - name: W3C WebRTC\n\
  \    baseURL: ''\n    tags:\n      - Communication\n      - Real-Time\n      - Video\n      - W3C\n      - WebRTC\n    serviceName: W3C WebRTC\n    serviceCategory: API\n  - name: W3C WebGPU\n    baseURL: ''\n    tags:\n      - GPU\n      - Graphics\n      - W3C\n      - WebGPU\n    serviceName: W3C WebGPU\n    serviceCategory: API\n  - name: W3C Web Components\n    baseURL: ''\n    tags:\n      - Components\n      - Custom Elements\n      - Shadow DOM\n      - W3C\n      - Web Components\n    serviceName: W3C Web Components\n    serviceCategory: API\n  - name: W3C Service Workers\n    baseURL: ''\n    tags:\n      - Offline\n      - Progressive Web Apps\n      - Service Workers\n      - W3C\n    serviceName: W3C Service Workers\n    serviceCategory: API\n  - name: W3C Payment Request API\n    baseURL: ''\n    tags:\n      - Commerce\n      - Payments\n      - W3C\n    serviceName: W3C Payment Request API\n    serviceCategory: API\n  - name: W3C WebAssembly\n    baseURL: ''\n    tags:\n\
  \      - Performance\n      - W3C\n      - WebAssembly\n    serviceName: W3C WebAssembly\n    serviceCategory: API\n  - name: W3C JSON-LD\n    baseURL: ''\n    tags:\n      - JSON-LD\n      - Linked Data\n      - Semantic Web\n      - W3C\n    serviceName: W3C JSON-LD\n    serviceCategory: API\n  - name: W3C Verifiable Credentials\n    baseURL: ''\n    tags:\n      - Credentials\n      - Identity\n      - Privacy\n      - Security\n      - W3C\n    serviceName: W3C Verifiable Credentials\n    serviceCategory: API\n  - name: W3C Web Neural Network API (WebNN)\n    baseURL: ''\n    tags:\n      - Artificial Intelligence\n      - Machine Learning\n      - W3C\n      - WebNN\n    serviceName: W3C Web Neural Network API (WebNN)\n    serviceCategory: API\n  - name: W3C Decentralized Identifiers (DIDs)\n    baseURL: ''\n    tags:\n      - Decentralized Identity\n      - DID\n      - Identity\n      - W3C\n    serviceName: W3C Decentralized Identifiers (DIDs)\n    serviceCategory: API\n  - name:\
  \ IETF HTTP Specifications\n    baseURL: ''\n    tags:\n      - HTTP\n      - IETF\n      - Networking\n      - Protocol\n    serviceName: IETF HTTP Specifications\n    serviceCategory: API\n  - name: ECMA JavaScript (ECMAScript)\n    baseURL: ''\n    tags:\n      - ECMAScript\n      - JavaScript\n      - Programming Language\n      - Standards\n    serviceName: ECMA JavaScript (ECMAScript)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/web-standards/refs/heads/main/finops/web-standards-finops.yml
sources: []
specification: FinOps Framework
tags:
- Browser Compatibility
- CSS
- HTML
- Interoperability
- JavaScript
- Standards
- Web APIs
- Web Development
- FinOps
- Cost Management
- FOCUS
---
