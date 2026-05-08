---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tomtom-maps-openapi.yml
  format: yaml
  label: TomTom Maps API
  slug: tomtom-maps-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-maps-openapi.yml
- filename: tomtom-search-openapi.yml
  format: yaml
  label: TomTom Search API
  slug: tomtom-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-search-openapi.yml
- filename: tomtom-routing-openapi.yml
  format: yaml
  label: TomTom Routing API
  slug: tomtom-routing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-routing-openapi.yml
- filename: tomtom-traffic-openapi.yml
  format: yaml
  label: TomTom Traffic API
  slug: tomtom-traffic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/openapi/tomtom-traffic-openapi.yml
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
description: FinOps framework definition for the TomTom API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: TomTom
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: TomTom
  PublisherName: TomTom
  ServiceCategory: Developer Tools / API
  ServiceName: TomTom
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
name: Tomtom Finops
provider_name: TomTom
provider_slug: tomtom
publisher_name: TomTom
service_category: API
slug: tomtom-finops
source_filename: tomtom-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TomTom\nproviderId: tomtom\npublisherName: TomTom\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Maps\n  - Traffic\n  - Transportation\n  - Navigation\n  - Location\n  - Geospatial\n  - Routing\n  - Geocoding\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the TomTom API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: TomTom\n  ServiceCategory: Developer Tools / API\n  ProviderName: TomTom\n  PublisherName: TomTom\n  InvoiceIssuerName: TomTom\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: TomTom Maps API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Maps\n      - Tiles\n      - Raster\n      - Vector\n    serviceName: TomTom Maps API\n    serviceCategory: API\n  - name: TomTom Search API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Search\n      - Geocoding\n      - Points of Interest\n      - Location\n    serviceName: TomTom Search API\n    serviceCategory: API\n  - name: TomTom Routing API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Routing\n      - Navigation\n      - Transportation\n      - Electric Vehicle\n    serviceName: TomTom Routing API\n    serviceCategory: API\n  - name: TomTom Traffic API\n    baseURL: https://api.tomtom.com\n\
  \    tags:\n      - Traffic\n      - Incidents\n      - Real-Time\n      - Transportation\n    serviceName: TomTom Traffic API\n    serviceCategory: API\n  - name: TomTom Geocoding API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Geocoding\n      - Location\n      - Address\n    serviceName: TomTom Geocoding API\n    serviceCategory: API\n  - name: TomTom Fuel Prices API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Fuel\n      - Prices\n      - Automotive\n    serviceName: TomTom Fuel Prices API\n    serviceCategory: API\n  - name: TomTom Parking Availability API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Parking\n      - Transportation\n      - Real-Time\n    serviceName: TomTom Parking Availability API\n    serviceCategory: API\n  - name: TomTom Geofencing API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Geofencing\n      - Location\n      - Tracking\n      - Notifications\n    serviceName: TomTom Geofencing API\n    serviceCategory:\
  \ API\n  - name: TomTom AutoStream API\n    baseURL: https://api.tomtom.com\n    tags:\n      - Maps\n      - Streaming\n      - Automotive\n    serviceName: TomTom AutoStream API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tomtom/refs/heads/main/finops/tomtom-finops.yml
sources: []
specification: FinOps Framework
tags:
- Maps
- Traffic
- Transportation
- Navigation
- Location
- Geospatial
- Routing
- Geocoding
- FinOps
- Cost Management
- FOCUS
---
