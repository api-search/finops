---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: autodesk-authentication-openapi.yml
  format: yaml
  label: Autodesk Authentication API
  slug: authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-authentication-openapi.yml
- filename: autodesk-data-management-openapi.yml
  format: yaml
  label: Autodesk Data Management API
  slug: data-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-data-management-openapi.yml
- filename: autodesk-model-derivative-openapi.yml
  format: yaml
  label: Autodesk Model Derivative API
  slug: model-derivative-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-model-derivative-openapi.yml
- filename: autodesk-design-automation-openapi.yml
  format: yaml
  label: Autodesk Design Automation API
  slug: design-automation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-design-automation-openapi.yml
- filename: autodesk-webhooks-openapi.yml
  format: yaml
  label: Autodesk Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-webhooks-openapi.yml
- filename: autodesk-reality-capture-openapi.yml
  format: yaml
  label: Autodesk Reality Capture API
  slug: reality-capture-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-reality-capture-openapi.yml
- filename: autodesk-sustainability-data-openapi.yml
  format: yaml
  label: Autodesk Sustainability Data API
  slug: sustainability-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-sustainability-data-openapi.yml
- filename: autodesk-parameters-openapi.yml
  format: yaml
  label: Autodesk Parameters API
  slug: parameters-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-parameters-openapi.yml
- filename: autodesk-tandem-data-openapi.yml
  format: yaml
  label: Autodesk Tandem Data API
  slug: tandem-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-tandem-data-openapi.yml
- filename: autodesk-flow-graph-engine-openapi.yml
  format: yaml
  label: Autodesk Flow Graph Engine API
  slug: flow-graph-engine-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-flow-graph-engine-openapi.yml
- filename: autodesk-acc-account-admin-openapi.yml
  format: yaml
  label: Autodesk ACC Account Admin API
  slug: acc-account-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-acc-account-admin-openapi.yml
- filename: autodesk-bim360-openapi.yml
  format: yaml
  label: Autodesk BIM 360 API
  slug: bim-360-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/openapi/autodesk-bim360-openapi.yml
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
description: FinOps framework definition for the Autodesk API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Autodesk
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Autodesk
  PublisherName: Autodesk
  ServiceCategory: Developer Tools / API
  ServiceName: Autodesk
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
name: Autodesk Finops
provider_name: Autodesk
provider_slug: autodesk
publisher_name: Autodesk
service_category: API
slug: autodesk-finops
source_filename: autodesk-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Autodesk\nproviderId: autodesk\npublisherName: Autodesk\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - 3D Modeling\n  - Architecture\n  - BIM\n  - CAD\n  - Construction\n  - Design\n  - Digital Twins\n  - Engineering\n  - Manufacturing\n  - Media and Entertainment\n  - Sustainability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Autodesk API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Autodesk\n  ServiceCategory: Developer Tools / API\n  ProviderName: Autodesk\n  PublisherName: Autodesk\n  InvoiceIssuerName: Autodesk\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n  \
  \  description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Autodesk Build Photos API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Photos\n      - Documentation\n    serviceName: Autodesk Build Photos API\n    serviceCategory: API\n  - name: Autodesk Authentication API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Authentication\n      - OAuth\n    serviceName: Autodesk Authentication API\n    serviceCategory: API\n  - name: Autodesk Data Management API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM 360\n      - Data Management\n      - Storage\n    serviceName: Autodesk\
  \ Data Management API\n    serviceCategory: API\n  - name: Autodesk Model Derivative API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - 3D Models\n      - File Conversion\n      - Metadata\n    serviceName: Autodesk Model Derivative API\n    serviceCategory: API\n  - name: Autodesk Design Automation API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - 3ds Max\n      - AutoCAD\n      - Automation\n      - Fusion\n      - Inventor\n      - Revit\n    serviceName: Autodesk Design Automation API\n    serviceCategory: API\n  - name: Autodesk Viewer SDK\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - 2D Visualization\n      - 3D Visualization\n      - Viewer\n    serviceName: Autodesk Viewer SDK\n    serviceCategory: API\n  - name: Autodesk Webhooks API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Autodesk Webhooks API\n    serviceCategory:\
  \ API\n  - name: Autodesk Reality Capture API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - 3D Models\n      - Photogrammetry\n      - Point Clouds\n      - Reality Capture\n    serviceName: Autodesk Reality Capture API\n    serviceCategory: API\n  - name: Autodesk AEC Data Model API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - AEC\n      - BIM\n      - Design Data\n      - GraphQL\n    serviceName: Autodesk AEC Data Model API\n    serviceCategory: API\n  - name: Autodesk Data Exchange API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM\n      - CAD\n      - Data Exchange\n      - Interoperability\n    serviceName: Autodesk Data Exchange API\n    serviceCategory: API\n  - name: Autodesk Sustainability Data API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Carbon Calculations\n      - Environmental Data\n      - Sustainability\n    serviceName: Autodesk Sustainability Data API\n    serviceCategory:\
  \ API\n  - name: Autodesk Parameters API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM\n      - Parameters\n      - Revit\n    serviceName: Autodesk Parameters API\n    serviceCategory: API\n  - name: Autodesk Tandem Data API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Digital Twins\n      - Facility Management\n      - IoT\n    serviceName: Autodesk Tandem Data API\n    serviceCategory: API\n  - name: Autodesk Flow Graph Engine API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Bifrost\n      - Cloud Computing\n      - Media and Entertainment\n    serviceName: Autodesk Flow Graph Engine API\n    serviceCategory: API\n  - name: Autodesk ACC Account Admin API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Account Administration\n      - Construction\n      - Project Management\n    serviceName: Autodesk ACC Account Admin API\n    serviceCategory: API\n  - name: Autodesk ACC Issues API\n    baseURL:\
  \ https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Issues\n      - Project Management\n    serviceName: Autodesk ACC Issues API\n    serviceCategory: API\n  - name: Autodesk ACC RFIs API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Project Management\n      - RFIs\n    serviceName: Autodesk ACC RFIs API\n    serviceCategory: API\n  - name: Autodesk ACC Cost Management API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Budgets\n      - Construction\n      - Cost Management\n    serviceName: Autodesk ACC Cost Management API\n    serviceCategory: API\n  - name: Autodesk ACC Data Connector API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Business Intelligence\n      - Construction\n      - Data Analytics\n    serviceName: Autodesk ACC Data Connector API\n    serviceCategory: API\n  - name: Autodesk ACC Model Coordination API\n    baseURL: https://developer.api.autodesk.com\n\
  \    tags:\n      - Clash Detection\n      - Construction\n      - Model Coordination\n    serviceName: Autodesk ACC Model Coordination API\n    serviceCategory: API\n  - name: Autodesk ACC Assets API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Asset Management\n      - Assets\n      - Construction\n    serviceName: Autodesk ACC Assets API\n    serviceCategory: API\n  - name: Autodesk ACC Locations API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Locations\n      - Project Management\n    serviceName: Autodesk ACC Locations API\n    serviceCategory: API\n  - name: Autodesk ACC Forms API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Data Collection\n      - Forms\n    serviceName: Autodesk ACC Forms API\n    serviceCategory: API\n  - name: Autodesk ACC Photos API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Documentation\n    \
  \  - Photos\n    serviceName: Autodesk ACC Photos API\n    serviceCategory: API\n  - name: Autodesk ACC Submittals API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Approvals\n      - Construction\n      - Submittals\n    serviceName: Autodesk ACC Submittals API\n    serviceCategory: API\n  - name: Autodesk ACC Sheets API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Document Management\n      - Sheets\n    serviceName: Autodesk ACC Sheets API\n    serviceCategory: API\n  - name: Autodesk ACC Reviews API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Approvals\n      - Construction\n      - Reviews\n    serviceName: Autodesk ACC Reviews API\n    serviceCategory: API\n  - name: Autodesk ACC Relationships API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Data Linking\n      - Relationships\n    serviceName: Autodesk ACC Relationships API\n    serviceCategory:\
  \ API\n  - name: Autodesk ACC Model Properties API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM\n      - Construction\n      - Model Properties\n    serviceName: Autodesk ACC Model Properties API\n    serviceCategory: API\n  - name: Autodesk ACC Transmittals API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Document Management\n      - Transmittals\n    serviceName: Autodesk ACC Transmittals API\n    serviceCategory: API\n  - name: Autodesk ACC AutoSpecs API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Specifications\n      - Submittals\n    serviceName: Autodesk ACC AutoSpecs API\n    serviceCategory: API\n  - name: Autodesk ACC Takeoff API\n    baseURL: https://developer.api.autodesk.com\n    tags:\n      - Construction\n      - Quantity Estimation\n      - Takeoff\n    serviceName: Autodesk ACC Takeoff API\n    serviceCategory: API\n  - name: Autodesk BIM 360 API\n\
  \    baseURL: https://developer.api.autodesk.com\n    tags:\n      - BIM\n      - Construction\n      - Project Management\n    serviceName: Autodesk BIM 360 API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autodesk/refs/heads/main/finops/autodesk-finops.yml
sources: []
specification: FinOps Framework
tags:
- 3D Modeling
- Architecture
- BIM
- CAD
- Construction
- Design
- Digital Twins
- Engineering
- Manufacturing
- Media and Entertainment
- Sustainability
- FinOps
- Cost Management
- FOCUS
---
