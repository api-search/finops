---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: academy-software-foundation-opencue.yaml
  format: yaml
  label: OpenCue
  slug: opencue
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/academy-software-foundation/refs/heads/main/openapi/academy-software-foundation-opencue.yaml
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
description: FinOps framework definition for the Academy Software Foundation API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Academy Software Foundation
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Academy Software Foundation
  PublisherName: Academy Software Foundation
  ServiceCategory: Developer Tools / API
  ServiceName: Academy Software Foundation
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
name: Academy Software Foundation Finops
provider_name: Academy Software Foundation
provider_slug: academy-software-foundation
publisher_name: Academy Software Foundation
service_category: API
slug: academy-software-foundation-finops
source_filename: academy-software-foundation-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Academy Software Foundation\nproviderId: academy-software-foundation\npublisherName: Academy Software Foundation\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Animation\n  - Color Management\n  - Film\n  - Linux Foundation\n  - Open Source\n  - Rendering\n  - Standards\n  - Visual Effects\n  - VFX\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Academy Software Foundation API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Academy Software Foundation\n  ServiceCategory: Developer Tools / API\n  ProviderName: Academy Software Foundation\n  PublisherName: Academy Software Foundation\n  InvoiceIssuerName: Academy Software Foundation\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: OpenEXR\n    baseURL: ''\n    tags:\n      - Image Format\n      - HDR\n      - Standards\n      - C++\n    serviceName: OpenEXR\n    serviceCategory: API\n  - name: OpenVDB\n    baseURL: ''\n    tags:\n      - Volumetric Data\n      - C++\n      - Rendering\n      - Standards\n    serviceName: OpenVDB\n    serviceCategory: API\n  - name: OpenColorIO\n    baseURL: ''\n    tags:\n      - Color Management\n      - Standards\n      - C++\n    serviceName: OpenColorIO\n    serviceCategory: API\n  - name:\
  \ OpenTimelineIO\n    baseURL: ''\n    tags:\n      - Editorial\n      - Timeline\n      - Standards\n      - Python\n    serviceName: OpenTimelineIO\n    serviceCategory: API\n  - name: Open Shading Language\n    baseURL: ''\n    tags:\n      - Shading\n      - Rendering\n      - Standards\n      - C++\n    serviceName: Open Shading Language\n    serviceCategory: API\n  - name: MaterialX\n    baseURL: ''\n    tags:\n      - Materials\n      - Shading\n      - Standards\n      - XML\n    serviceName: MaterialX\n    serviceCategory: API\n  - name: OpenCue\n    baseURL: ''\n    tags:\n      - Render Management\n      - VFX\n      - Python\n    serviceName: OpenCue\n    serviceCategory: API\n  - name: OpenImageIO\n    baseURL: ''\n    tags:\n      - Image Processing\n      - C++\n      - VFX\n    serviceName: OpenImageIO\n    serviceCategory: API\n  - name: OpenFX\n    baseURL: ''\n    tags:\n      - Visual Effects\n      - Plugin API\n      - Standards\n      - C++\n    serviceName: OpenFX\n\
  \    serviceCategory: API\n  - name: OpenAPV\n    baseURL: ''\n    tags:\n      - Video Codec\n      - Standards\n      - C\n    serviceName: OpenAPV\n    serviceCategory: API\n  - name: OpenPBR\n    baseURL: ''\n    tags:\n      - Rendering\n      - Materials\n      - Standards\n    serviceName: OpenPBR\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/academy-software-foundation/refs/heads/main/finops/academy-software-foundation-finops.yml
sources: []
specification: FinOps Framework
tags:
- Animation
- Color Management
- Film
- Linux Foundation
- Open Source
- Rendering
- Standards
- Visual Effects
- VFX
- FinOps
- Cost Management
- FOCUS
---
