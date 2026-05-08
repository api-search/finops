---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Adobe Photoshop API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.adobe.com/photoshop/api/openapi/
- filename: openapi.yaml
  format: yaml
  label: Adobe Lightroom API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.adobe.com/lightroom/api/openapi/
- filename: openapi.yaml
  format: yaml
  label: Adobe PDF Services API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.adobe.com/document-services/docs/apis/
- filename: openapi.yaml
  format: yaml
  label: Adobe PDF Extract API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.adobe.com/document-services/docs/apis/
- filename: openapi.yaml
  format: yaml
  label: Adobe PDF Accessibility Auto-Tag API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.adobe.com/document-services/docs/apis/
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
description: FinOps framework definition for the Adobe Suite API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Adobe Suite
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Adobe Suite
  PublisherName: Adobe Suite
  ServiceCategory: Developer Tools / API
  ServiceName: Adobe Suite
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
name: Adobe Suite Finops
provider_name: Adobe Suite
provider_slug: adobe-suite
publisher_name: Adobe Suite
service_category: API
slug: adobe-suite-finops
source_filename: adobe-suite-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Adobe Suite\nproviderId: adobe-suite\npublisherName: Adobe Suite\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Ai\n  - Analytics\n  - Automation\n  - Commerce\n  - Creative\n  - Design\n  - Documents\n  - Experience\n  - Marketing\n  - Personalization\n  - Video\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Adobe Suite API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Adobe Suite\n  ServiceCategory: Developer Tools / API\n  ProviderName: Adobe Suite\n  PublisherName: Adobe Suite\n  InvoiceIssuerName: Adobe Suite\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Adobe Photoshop API\n    baseURL: https://image.adobe.io\n    tags:\n      - Automation\n      - Creative\n      - Editing\n      - Images\n    serviceName: Adobe Photoshop API\n    serviceCategory: API\n  - name: Adobe Lightroom API\n    baseURL: https://lr.adobe.io\n    tags:\n      - Editing\n      - Organization\n      - Photography\n      - Raw\n    serviceName: Adobe Lightroom API\n    serviceCategory: API\n  - name: Adobe Illustrator API\n    baseURL: https://illustrator.adobe.io\n    tags:\n      - Automation\n      - Design\n      - Graphics\n      - Vector\n    serviceName: Adobe Illustrator API\n    serviceCategory:\
  \ API\n  - name: Adobe InDesign API\n    baseURL: https://indesign.adobe.io\n    tags:\n      - Documents\n      - Layout\n      - Print\n      - Publishing\n    serviceName: Adobe InDesign API\n    serviceCategory: API\n  - name: Adobe PDF Services API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - Conversion\n      - Documents\n      - Ocr\n      - Pdf\n    serviceName: Adobe PDF Services API\n    serviceCategory: API\n  - name: Adobe PDF Extract API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - Ai\n      - Documents\n      - Extraction\n      - Pdf\n    serviceName: Adobe PDF Extract API\n    serviceCategory: API\n  - name: Adobe PDF Accessibility Auto-Tag API\n    baseURL: https://pdf-services.adobe.io\n    tags:\n      - Accessibility\n      - Ai\n      - Compliance\n      - Pdf\n    serviceName: Adobe PDF Accessibility Auto-Tag API\n    serviceCategory: API\n  - name: Adobe Sign API\n    baseURL: https://api.adobe.io/sign\n    tags:\n      - Documents\n\
  \      - Esignature\n      - Legal\n      - Workflow\n    serviceName: Adobe Sign API\n    serviceCategory: API\n  - name: Adobe Analytics API\n    baseURL: https://analytics.adobe.io\n    tags:\n      - Analytics\n      - Data\n      - Marketing\n      - Reporting\n    serviceName: Adobe Analytics API\n    serviceCategory: API\n  - name: Adobe Experience Manager API\n    baseURL: https://aem.adobe.io\n    tags:\n      - Assets\n      - Cms\n      - Content\n      - Dam\n    serviceName: Adobe Experience Manager API\n    serviceCategory: API\n  - name: Adobe Stock API\n    baseURL: https://stock.adobe.io\n    tags:\n      - Assets\n      - Images\n      - Licensing\n      - Stock\n    serviceName: Adobe Stock API\n    serviceCategory: API\n  - name: Adobe Firefly API\n    baseURL: https://firefly.adobe.io\n    tags:\n      - Ai\n      - Creative\n      - Generative\n      - Images\n    serviceName: Adobe Firefly API\n    serviceCategory: API\n  - name: Adobe Firefly Audio/Video APIs\n\
  \    baseURL: https://firefly.adobe.io\n    tags:\n      - Ai\n      - Audio\n      - Generative\n      - Translation\n      - Video\n    serviceName: Adobe Firefly Audio/Video APIs\n    serviceCategory: API\n  - name: Adobe Creative Cloud Libraries API\n    baseURL: https://cc-libraries.adobe.io\n    tags:\n      - Assets\n      - Collaboration\n      - Creative\n      - Libraries\n    serviceName: Adobe Creative Cloud Libraries API\n    serviceCategory: API\n  - name: Adobe Express Embed SDK\n    baseURL: https://express.adobe.com\n    tags:\n      - Creative\n      - Design\n      - Embed\n      - Templates\n    serviceName: Adobe Express Embed SDK\n    serviceCategory: API\n  - name: Adobe Premiere Pro API\n    baseURL: https://premiere.adobe.io\n    tags:\n      - Automation\n      - Creative\n      - Editing\n      - Video\n    serviceName: Adobe Premiere Pro API\n    serviceCategory: API\n  - name: Adobe After Effects API\n    baseURL: https://aftereffects.adobe.io\n    tags:\n\
  \      - Animation\n      - Creative\n      - Effects\n      - Video\n    serviceName: Adobe After Effects API\n    serviceCategory: API\n  - name: Adobe Experience Platform API\n    baseURL: https://platform.adobe.io\n    tags:\n      - Data\n      - Experience\n      - Marketing\n      - Platform\n    serviceName: Adobe Experience Platform API\n    serviceCategory: API\n  - name: Adobe Target API\n    baseURL: https://mc.adobe.io\n    tags:\n      - Marketing\n      - Optimization\n      - Personalization\n      - Testing\n    serviceName: Adobe Target API\n    serviceCategory: API\n  - name: Adobe Campaign API\n    baseURL: https://mc.adobe.io\n    tags:\n      - Automation\n      - Campaigns\n      - Email\n      - Marketing\n    serviceName: Adobe Campaign API\n    serviceCategory: API\n  - name: Adobe Marketo Engage API\n    baseURL: https://marketo.adobe.io\n    tags:\n      - Automation\n      - Crm\n      - Leads\n      - Marketing\n    serviceName: Adobe Marketo Engage API\n\
  \    serviceCategory: API\n  - name: Adobe Commerce API\n    baseURL: https://commerce.adobe.io\n    tags:\n      - Commerce\n      - Ecommerce\n      - Graphql\n      - Rest\n    serviceName: Adobe Commerce API\n    serviceCategory: API\n  - name: Adobe User Management API\n    baseURL: https://usermanagement.adobe.io\n    tags:\n      - Enterprise\n      - Identity\n      - Management\n      - Users\n    serviceName: Adobe User Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adobe-suite/refs/heads/main/finops/adobe-suite-finops.yml
sources: []
specification: FinOps Framework
tags:
- Ai
- Analytics
- Automation
- Commerce
- Creative
- Design
- Documents
- Experience
- Marketing
- Personalization
- Video
- FinOps
- Cost Management
- FOCUS
---
