---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: adobe-firefly-api-openapi-original.yml
  format: yaml
  label: Adobe Firefly API
  slug: firefly-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-firefly-api-openapi-original.yml
- filename: adobe-cc-libraries-api-openapi-original.yml
  format: yaml
  label: Creative Cloud Libraries API
  slug: cc-libraries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-cc-libraries-api-openapi-original.yml
- filename: adobe-stock-api-openapi-original.yml
  format: yaml
  label: Adobe Stock API
  slug: stock-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-stock-api-openapi-original.yml
- filename: adobe-pdf-services-api-openapi-original.yml
  format: yaml
  label: Adobe PDF Services API
  slug: pdf-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/openapi/adobe-pdf-services-api-openapi-original.yml
- filename: adobe-io-events-asyncapi-original.yml
  format: yaml
  label: Adobe I/O Events
  slug: io-events
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/asyncapi/adobe-io-events-asyncapi-original.yml
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
description: FinOps framework definition for the Adobe Creative Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Adobe Creative Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Adobe Creative Cloud
  PublisherName: Adobe Creative Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Adobe Creative Cloud
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
name: Adobe Creative Cloud Finops
provider_name: Adobe Creative Cloud
provider_slug: adobe-creative-cloud
publisher_name: Adobe Creative Cloud
service_category: API
slug: adobe-creative-cloud-finops
source_filename: adobe-creative-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Adobe Creative Cloud\nproviderId: adobe-creative-cloud\npublisherName: Adobe Creative Cloud\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI/ML\n  - Cloud\n  - Creative\n  - Design\n  - Documents\n  - Photography\n  - SaaS\n  - Video\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Adobe Creative Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Adobe Creative Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Adobe Creative Cloud\n  PublisherName: Adobe Creative Cloud\n  InvoiceIssuerName: Adobe Creative Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Adobe Firefly API\n    baseURL: https://firefly-api.adobe.io/v2\n    tags:\n      - AI/ML\n      - Generative AI\n      - Generative Fill\n      - Image Generation\n      - Text-To-Image\n    serviceName: Adobe Firefly API\n    serviceCategory: API\n  - name: Adobe Express Embed SDK\n    baseURL: https://api.example.com\n    tags:\n      - Editor\n      - Embed SDK\n      - JavaScript\n      - Quick Actions\n      - Web Components\n    serviceName: Adobe Express Embed SDK\n    serviceCategory: API\n  - name: Creative Cloud Libraries API\n    baseURL: https://cc-libraries.adobe.io\n   \
  \ tags:\n      - Assets\n      - Collaboration\n      - Colors\n      - Libraries\n      - Styles\n      - Sync\n    serviceName: Creative Cloud Libraries API\n    serviceCategory: API\n  - name: Adobe Cloud Storage and Collaboration API\n    baseURL: https://api.example.com\n    tags:\n      - Cloud Storage\n      - Collaboration\n      - Files\n      - Projects\n      - REST API\n    serviceName: Adobe Cloud Storage and Collaboration API\n    serviceCategory: API\n  - name: Adobe Stock API\n    baseURL: https://stock.adobe.io\n    tags:\n      - Assets\n      - Licensing\n      - Media\n      - Search\n      - Stock Photos\n      - Vectors\n    serviceName: Adobe Stock API\n    serviceCategory: API\n  - name: Adobe Fonts API\n    baseURL: https://typekit.com/api\n    tags:\n      - Fonts\n      - Kits\n      - Typekit\n      - Typography\n      - Web Fonts\n    serviceName: Adobe Fonts API\n    serviceCategory: API\n  - name: Adobe PDF Services API\n    baseURL: https://pdf-services.adobe.io\n\
  \    tags:\n      - Acrobat Services\n      - Conversion\n      - Document Processing\n      - Extraction\n      - OCR\n      - PDF\n    serviceName: Adobe PDF Services API\n    serviceCategory: API\n  - name: Adobe Document Generation API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - Data Merge\n      - Document Generation\n      - PDF\n      - Templates\n      - Word\n    serviceName: Adobe Document Generation API\n    serviceCategory: API\n  - name: Acrobat Sign API\n    baseURL: https://api.example.com\n    tags:\n      - Agreements\n      - Compliance\n      - Documents\n      - Electronic Signatures\n      - Workflows\n    serviceName: Acrobat Sign API\n    serviceCategory: API\n  - name: Adobe I/O Events\n    baseURL: https://api.example.com\n    tags:\n      - Event-Driven\n      - Events\n      - Notifications\n      - Real-Time\n      - Webhooks\n    serviceName: Adobe I/O Events\n    serviceCategory: API\n  - name: Adobe I/O Runtime\n    baseURL: https://api.example.com\n\
  \    tags:\n      - Cloud Computing\n      - FaaS\n      - Functions\n      - OpenWhisk\n      - Serverless\n    serviceName: Adobe I/O Runtime\n    serviceCategory: API\n  - name: Adobe App Builder\n    baseURL: https://api.example.com\n    tags:\n      - Application Framework\n      - Custom Apps\n      - Enterprise\n      - React Spectrum\n      - SPA\n    serviceName: Adobe App Builder\n    serviceCategory: API\n  - name: Adobe UXP (Unified Extensibility Platform)\n    baseURL: https://api.example.com\n    tags:\n      - Cross-App\n      - Extensions\n      - HTML/CSS\n      - JavaScript\n      - Modern\n      - Plugin Framework\n    serviceName: Adobe UXP (Unified Extensibility Platform)\n    serviceCategory: API\n  - name: Adobe CEP (Common Extensibility Platform)\n    baseURL: https://api.example.com\n    tags:\n      - ExtendScript\n      - HTML5\n      - Legacy\n      - Panels\n      - Plugin Framework\n    serviceName: Adobe CEP (Common Extensibility Platform)\n    serviceCategory:\
  \ API\n  - name: Adobe Photoshop API\n    baseURL: https://image.adobe.io\n    tags:\n      - Automation\n      - Cloud\n      - Firefly Services\n      - Image Processing\n      - Photoshop\n    serviceName: Adobe Photoshop API\n    serviceCategory: API\n  - name: Adobe Lightroom API\n    baseURL: https://lr.adobe.io\n    tags:\n      - Cloud\n      - Image Editing\n      - Photo Management\n      - Photography\n      - Presets\n    serviceName: Adobe Lightroom API\n    serviceCategory: API\n  - name: Adobe Developer Distribution\n    baseURL: https://api.example.com\n    tags:\n      - Exchange\n      - Marketplace\n      - Plugin Distribution\n      - Publishing\n    serviceName: Adobe Developer Distribution\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-cloud/refs/heads/main/finops/adobe-creative-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI/ML
- Cloud
- Creative
- Design
- Documents
- Photography
- SaaS
- Video
- FinOps
- Cost Management
- FOCUS
---
