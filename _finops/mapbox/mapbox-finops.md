---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mapbox-openapi.yml
  format: yaml
  label: Mapbox Tiling Service
  slug: mapbox-tiling-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mapbox/refs/heads/main/openapi/mapbox-openapi.yml
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
description: FinOps framework definition for the Mapbox API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mapbox
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Mapbox
  PublisherName: Mapbox
  ServiceCategory: Developer Tools / API
  ServiceName: Mapbox
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
name: Mapbox Finops
provider_name: Mapbox
provider_slug: mapbox
publisher_name: Mapbox
service_category: API
slug: mapbox-finops
source_filename: mapbox-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Mapbox\nproviderId: mapbox\npublisherName: Mapbox\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Mapping\n  - Maps\n  - Geospatial\n  - Location\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Mapbox API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application,\
  \ and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education\
  \ and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Mapbox\n  ServiceCategory: Developer Tools / API\n  ProviderName: Mapbox\n  PublisherName: Mapbox\n  InvoiceIssuerName: Mapbox\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      -\
  \ consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Mapbox Tiling Service\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Tiles\n      - Vector Tiles\n    serviceName: Mapbox Tiling Service\n    serviceCategory: API\n  - name: Mapbox Vector Tiles API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Tiles\n      - Vector Tiles\n    serviceName: Mapbox Vector Tiles API\n    serviceCategory: API\n  - name: Mapbox Raster Tiles API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Tiles\n      - Raster Tiles\n    serviceName: Mapbox Raster Tiles API\n    serviceCategory: API\n  - name: Mapbox Static Images API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Static Images\n    serviceName: Mapbox Static Images\
  \ API\n    serviceCategory: API\n  - name: Mapbox Static Tiles API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Tiles\n      - Static Tiles\n    serviceName: Mapbox Static Tiles API\n    serviceCategory: API\n  - name: Mapbox Styles API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Styles\n    serviceName: Mapbox Styles API\n    serviceCategory: API\n  - name: Mapbox Tilequery API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Tile Query\n      - Geospatial\n    serviceName: Mapbox Tilequery API\n    serviceCategory: API\n  - name: Mapbox Uploads API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Uploads\n      - Geospatial\n    serviceName: Mapbox Uploads API\n    serviceCategory: API\n  - name: Mapbox Datasets API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Datasets\n      - GeoJSON\n    serviceName: Mapbox Datasets API\n    serviceCategory: API\n\
  \  - name: Mapbox Fonts API\n    baseURL: https://api.mapbox.com\n    tags:\n      - Mapping\n      - Fonts\n    serviceName: Mapbox Fonts API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    url: http://apievangelist.com\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mapbox/refs/heads/main/finops/mapbox-finops.yml
sources: []
specification: FinOps Framework
tags:
- Mapping
- Maps
- Geospatial
- Location
- FinOps
- Cost Management
- FOCUS
---
