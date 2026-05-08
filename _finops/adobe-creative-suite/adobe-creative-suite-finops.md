---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Adobe Photoshop API
  slug: photoshop-api
  spec_type: OpenAPI
  url: https://developer.adobe.com/photoshop/api/openapi.json
- filename: openapi.json
  format: json
  label: Adobe Lightroom API
  slug: lightroom-api
  spec_type: OpenAPI
  url: https://developer.adobe.com/lightroom/api/openapi.json
- filename: openapi.json
  format: json
  label: Adobe Stock API
  slug: stock-api
  spec_type: OpenAPI
  url: https://developer.adobe.com/stock/docs/api/openapi.json
- filename: adobe-creative-suite-firefly-openapi.yml
  format: yaml
  label: Adobe Firefly API
  slug: firefly-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-suite/refs/heads/main/openapi/adobe-creative-suite-firefly-openapi.yml
- filename: adobe-creative-suite-pdf-services-openapi.yml
  format: yaml
  label: Adobe PDF Services API
  slug: pdf-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-suite/refs/heads/main/openapi/adobe-creative-suite-pdf-services-openapi.yml
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
description: FinOps framework definition for the Adobe Creative Suite API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Adobe Creative Suite
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Adobe Creative Suite
  PublisherName: Adobe Creative Suite
  ServiceCategory: Developer Tools / API
  ServiceName: Adobe Creative Suite
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
name: Adobe Creative Suite Finops
provider_name: Adobe Creative Suite
provider_slug: adobe-creative-suite
publisher_name: Adobe Creative Suite
service_category: API
slug: adobe-creative-suite-finops
source_filename: adobe-creative-suite-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Adobe Creative Suite\nproviderId: adobe-creative-suite\npublisherName: Adobe Creative Suite\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Creative\n  - Design\n  - Graphics\n  - Photography\n  - Video\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Adobe Creative Suite API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Adobe Creative Suite\n  ServiceCategory: Developer Tools / API\n  ProviderName: Adobe Creative Suite\n  PublisherName: Adobe Creative Suite\n  InvoiceIssuerName: Adobe Creative Suite\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Adobe Photoshop API\n    baseURL: https://image.adobe.io\n    tags:\n      - Automation\n      - Graphics\n      - Image Editing\n      - Photoshop\n    serviceName: Adobe Photoshop API\n    serviceCategory: API\n  - name: Adobe Lightroom API\n    baseURL: https://lr.adobe.io\n    tags:\n      - Editing\n      - Lightroom\n      - Photo Management\n      - Photography\n    serviceName: Adobe Lightroom API\n    serviceCategory: API\n  - name: Adobe Illustrator API\n    baseURL: https://image.adobe.io\n    tags:\n      - Automation\n      - Design\n      - Illustrator\n      - Vector Graphics\n    serviceName: Adobe Illustrator\
  \ API\n    serviceCategory: API\n  - name: Adobe InDesign API\n    baseURL: https://indesign-api.adobe.io\n    tags:\n      - Documents\n      - InDesign\n      - Layout\n      - Publishing\n    serviceName: Adobe InDesign API\n    serviceCategory: API\n  - name: Adobe Premiere Pro API\n    baseURL: https://premiere-api.adobe.io\n    tags:\n      - Automation\n      - Media\n      - Premiere Pro\n      - Video Editing\n    serviceName: Adobe Premiere Pro API\n    serviceCategory: API\n  - name: Adobe After Effects API\n    baseURL: https://aftereffects-api.adobe.io\n    tags:\n      - After Effects\n      - Animation\n      - Motion Graphics\n      - Visual Effects\n    serviceName: Adobe After Effects API\n    serviceCategory: API\n  - name: Adobe Creative Cloud Libraries API\n    baseURL: https://cc-libraries.adobe.io\n    tags:\n      - Assets\n      - Collaboration\n      - Creative Cloud\n      - Libraries\n    serviceName: Adobe Creative Cloud Libraries API\n    serviceCategory:\
  \ API\n  - name: Adobe Stock API\n    baseURL: https://stock.adobe.io\n    tags:\n      - Images\n      - Licensing\n      - Stock\n      - Video\n    serviceName: Adobe Stock API\n    serviceCategory: API\n  - name: Adobe Firefly API\n    baseURL: https://firefly-api.adobe.io/v3\n    tags:\n      - Creative AI\n      - Firefly\n      - Generative AI\n      - Image Generation\n    serviceName: Adobe Firefly API\n    serviceCategory: API\n  - name: Adobe PDF Services API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - Acrobat\n      - Document Conversion\n      - Document Services\n      - PDF\n    serviceName: Adobe PDF Services API\n    serviceCategory: API\n  - name: Adobe Analytics API\n    baseURL: https://analytics.adobe.io/api\n    tags:\n      - Analytics\n      - Data\n      - Experience Cloud\n      - Reporting\n    serviceName: Adobe Analytics API\n    serviceCategory: API\n  - name: Adobe Experience Manager Assets API\n    baseURL: https://author-{program}-{environment}.adobeaemcloud.com/api\n\
  \    tags:\n      - AEM\n      - Content Management\n      - Digital Asset Management\n      - Experience Manager\n    serviceName: Adobe Experience Manager Assets API\n    serviceCategory: API\n  - name: Adobe Acrobat Sign API\n    baseURL: https://api.na1.adobesign.com/api/rest/v6\n    tags:\n      - Acrobat Sign\n      - Agreements\n      - Documents\n      - Electronic Signatures\n    serviceName: Adobe Acrobat Sign API\n    serviceCategory: API\n  - name: Adobe Fonts API\n    baseURL: https://fonts.adobe.io\n    tags:\n      - Design\n      - Fonts\n      - Typography\n      - Web Fonts\n    serviceName: Adobe Fonts API\n    serviceCategory: API\n  - name: Adobe Express Embed SDK\n    baseURL: https://express-api.adobe.io\n    tags:\n      - Design\n      - Embed SDK\n      - Express\n      - Templates\n    serviceName: Adobe Express Embed SDK\n    serviceCategory: API\n  - name: Adobe UXP\n    baseURL: https://developer.adobe.com/uxp/\n    tags:\n      - Creative Cloud\n      - Extensibility\n\
  \      - Plugins\n      - UXP\n    serviceName: Adobe UXP\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-creative-suite/refs/heads/main/finops/adobe-creative-suite-finops.yml
sources: []
specification: FinOps Framework
tags:
- Creative
- Design
- Graphics
- Photography
- Video
- FinOps
- Cost Management
- FOCUS
---
