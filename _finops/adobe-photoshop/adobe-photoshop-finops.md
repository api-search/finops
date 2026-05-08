---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-photoshop-api-openapi-original.yml
  format: yaml
  label: Adobe Photoshop API
  slug: photoshop-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-photoshop/refs/heads/main/openapi/adobe-photoshop-api-openapi-original.yml
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
description: FinOps framework definition for the Adobe Photoshop API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Adobe Photoshop
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Adobe Photoshop
  PublisherName: Adobe Photoshop
  ServiceCategory: Developer Tools / API
  ServiceName: Adobe Photoshop
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
name: Adobe Photoshop Finops
provider_name: Adobe Photoshop
provider_slug: adobe-photoshop
publisher_name: Adobe Photoshop
service_category: API
slug: adobe-photoshop-finops
source_filename: adobe-photoshop-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Adobe Photoshop\nproviderId: adobe-photoshop\npublisherName: Adobe Photoshop\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI/ML\n  - Creative Cloud\n  - Image Editing\n  - Photoshop\n  - Plugins\n  - REST API\n  - Scripting\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Adobe Photoshop API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Adobe Photoshop\n  ServiceCategory: Developer Tools / API\n  ProviderName: Adobe Photoshop\n  PublisherName: Adobe Photoshop\n  InvoiceIssuerName: Adobe Photoshop\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Adobe Photoshop API\n    baseURL: https://image.adobe.io\n    tags:\n      - AI/ML\n      - Asynchronous\n      - Background Removal\n      - Cloud\n      - Image Processing\n      - PSD Editing\n      - REST API\n    serviceName: Adobe Photoshop API\n    serviceCategory: API\n  - name: Adobe Firefly Services SDK for JavaScript\n    baseURL: https://image.adobe.io\n    tags:\n      - Client Library\n      - Node.js\n      - NPM\n      - SDK\n      - TypeScript\n    serviceName: Adobe Firefly Services SDK for JavaScript\n    serviceCategory: API\n  - name: Adobe Photoshop UXP Plugin API\n    baseURL: https://api.example.com\n\
  \    tags:\n      - Desktop\n      - DOM API\n      - HTML/CSS\n      - JavaScript\n      - Plugin Platform\n      - Spectrum UI\n    serviceName: Adobe Photoshop UXP Plugin API\n    serviceCategory: API\n  - name: Adobe Photoshop UXP Scripting\n    baseURL: https://api.example.com\n    tags:\n      - Automation\n      - JavaScript\n      - Modern JS\n      - Scripting\n    serviceName: Adobe Photoshop UXP Scripting\n    serviceCategory: API\n  - name: Adobe Photoshop UXP Hybrid Plugins\n    baseURL: https://api.example.com\n    tags:\n      - C++\n      - Filters\n      - Hybrid\n      - Native Code\n      - Performance\n      - Plugin\n    serviceName: Adobe Photoshop UXP Hybrid Plugins\n    serviceCategory: API\n  - name: Adobe Photoshop C++ Plugin SDK\n    baseURL: https://api.example.com\n    tags:\n      - C++\n      - Desktop\n      - File Formats\n      - Filters\n      - Native SDK\n    serviceName: Adobe Photoshop C++ Plugin SDK\n    serviceCategory: API\n  - name: Adobe Photoshop\
  \ ExtendScript Scripting API\n    baseURL: https://api.example.com\n    tags:\n      - Automation\n      - ExtendScript\n      - JSX\n      - Legacy\n      - Scripting\n    serviceName: Adobe Photoshop ExtendScript Scripting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-photoshop/refs/heads/main/finops/adobe-photoshop-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI/ML
- Creative Cloud
- Image Editing
- Photoshop
- Plugins
- REST API
- Scripting
- FinOps
- Cost Management
- FOCUS
---
