---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: maps-js.yaml
  format: yaml
  label: Maps JavaScript API
  slug: ''
  spec_type: OpenAPI
  url: https://api.example.com/openapi/maps-js.yaml
- filename: google-maps-geocoding-api.yml
  format: yaml
  label: Geocoding API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/openapi/google-maps-geocoding-api.yml
- filename: google-maps-places-api.yml
  format: yaml
  label: Places API (New)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/openapi/google-maps-places-api.yml
- filename: google-maps-directions-api.yml
  format: yaml
  label: Directions API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/openapi/google-maps-directions-api.yml
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
description: FinOps framework definition for the Google Maps Platform API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Maps Platform
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Maps Platform
  PublisherName: Google Maps Platform
  ServiceCategory: Developer Tools / API
  ServiceName: Google Maps Platform
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
name: Google Maps Finops
provider_name: Google Maps Platform
provider_slug: google-maps
publisher_name: Google Maps Platform
service_category: API
slug: google-maps-finops
source_filename: google-maps-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Maps Platform\nproviderId: google-maps\npublisherName: Google Maps Platform\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Environment\n  - Geocoding\n  - Geolocation\n  - Maps\n  - Navigation\n  - Places\n  - Routing\n  - Solar\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Maps Platform API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Maps Platform\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Maps Platform\n  PublisherName: Google Maps Platform\n  InvoiceIssuerName: Google Maps Platform\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Maps JavaScript API\n    baseURL: ''\n    tags:\n      - Javascript\n      - Maps\n      - Visualization\n    serviceName: Maps JavaScript API\n    serviceCategory: API\n  - name: Maps SDK for Android\n    baseURL: ''\n    tags:\n      - Android\n      - Maps\n      - Mobile\n      - Sdk\n    serviceName: Maps SDK for Android\n    serviceCategory: API\n  - name: Maps SDK for iOS\n    baseURL: ''\n    tags:\n      - Ios\n      - Maps\n      - Mobile\n      - Sdk\n    serviceName: Maps SDK for iOS\n    serviceCategory: API\n  - name: Google Maps for Flutter\n    baseURL: ''\n    tags:\n\
  \      - Cross-Platform\n      - Flutter\n      - Maps\n      - Mobile\n    serviceName: Google Maps for Flutter\n    serviceCategory: API\n  - name: Navigation SDK for Android\n    baseURL: ''\n    tags:\n      - Android\n      - Mobile\n      - Navigation\n      - Sdk\n    serviceName: Navigation SDK for Android\n    serviceCategory: API\n  - name: Navigation SDK for iOS\n    baseURL: ''\n    tags:\n      - Ios\n      - Mobile\n      - Navigation\n      - Sdk\n    serviceName: Navigation SDK for iOS\n    serviceCategory: API\n  - name: Navigation for Flutter and React Native\n    baseURL: ''\n    tags:\n      - Cross-Platform\n      - Flutter\n      - Navigation\n      - React-Native\n    serviceName: Navigation for Flutter and React Native\n    serviceCategory: API\n  - name: Geocoding API\n    baseURL: ''\n    tags:\n      - Addresses\n      - Coordinates\n      - Geocoding\n    serviceName: Geocoding API\n    serviceCategory: API\n  - name: Places API\n    baseURL: ''\n    tags:\n\
  \      - Places\n      - Poi\n      - Search\n    serviceName: Places API\n    serviceCategory: API\n  - name: Places API (New)\n    baseURL: ''\n    tags:\n      - Autocomplete\n      - Places\n      - Poi\n      - Search\n    serviceName: Places API (New)\n    serviceCategory: API\n  - name: Places SDK for Android\n    baseURL: ''\n    tags:\n      - Android\n      - Mobile\n      - Places\n      - Sdk\n    serviceName: Places SDK for Android\n    serviceCategory: API\n  - name: Places SDK for iOS\n    baseURL: ''\n    tags:\n      - Ios\n      - Mobile\n      - Places\n      - Sdk\n    serviceName: Places SDK for iOS\n    serviceCategory: API\n  - name: Directions API\n    baseURL: ''\n    tags:\n      - Directions\n      - Navigation\n      - Routing\n    serviceName: Directions API\n    serviceCategory: API\n  - name: Distance Matrix API\n    baseURL: ''\n    tags:\n      - Distance\n      - Matrix\n      - Routing\n    serviceName: Distance Matrix API\n    serviceCategory: API\n\
  \  - name: Roads API\n    baseURL: ''\n    tags:\n      - Roads\n      - Snap-To-Road\n      - Speed-Limits\n    serviceName: Roads API\n    serviceCategory: API\n  - name: Routes API\n    baseURL: ''\n    tags:\n      - Directions\n      - Routing\n      - Tolls\n      - Traffic\n    serviceName: Routes API\n    serviceCategory: API\n  - name: Route Optimization API\n    baseURL: ''\n    tags:\n      - Fleet\n      - Logistics\n      - Optimization\n      - Routing\n    serviceName: Route Optimization API\n    serviceCategory: API\n  - name: Maps Static API\n    baseURL: ''\n    tags:\n      - Images\n      - Maps\n      - Static\n    serviceName: Maps Static API\n    serviceCategory: API\n  - name: Maps Embed API\n    baseURL: ''\n    tags:\n      - Embed\n      - Iframe\n      - Maps\n    serviceName: Maps Embed API\n    serviceCategory: API\n  - name: Street View Static API\n    baseURL: ''\n    tags:\n      - Imagery\n      - Panorama\n      - Street-View\n    serviceName: Street\
  \ View Static API\n    serviceCategory: API\n  - name: Maps URLs\n    baseURL: ''\n    tags:\n      - Cross-Platform\n      - Deep-Linking\n      - Urls\n    serviceName: Maps URLs\n    serviceCategory: API\n  - name: Elevation API\n    baseURL: ''\n    tags:\n      - Altitude\n      - Elevation\n      - Terrain\n    serviceName: Elevation API\n    serviceCategory: API\n  - name: Geolocation API\n    baseURL: ''\n    tags:\n      - Cell-Towers\n      - Geolocation\n      - Wifi\n    serviceName: Geolocation API\n    serviceCategory: API\n  - name: Time Zone API\n    baseURL: ''\n    tags:\n      - Daylight-Savings\n      - Timezone\n      - Utc-Offset\n    serviceName: Time Zone API\n    serviceCategory: API\n  - name: Address Validation API\n    baseURL: ''\n    tags:\n      - Address\n      - Deliverability\n      - Validation\n    serviceName: Address Validation API\n    serviceCategory: API\n  - name: Aerial View API\n    baseURL: ''\n    tags:\n      - 3d\n      - Aerial\n      -\
  \ Video\n      - Visualization\n    serviceName: Aerial View API\n    serviceCategory: API\n  - name: Map Tiles API\n    baseURL: ''\n    tags:\n      - 3d\n      - Photorealistic\n      - Rendering\n      - Tiles\n    serviceName: Map Tiles API\n    serviceCategory: API\n  - name: Maps Datasets API\n    baseURL: ''\n    tags:\n      - Data\n      - Datasets\n      - Geospatial\n    serviceName: Maps Datasets API\n    serviceCategory: API\n  - name: Places Aggregate API\n    baseURL: ''\n    tags:\n      - Aggregate\n      - Analytics\n      - Insights\n      - Places\n    serviceName: Places Aggregate API\n    serviceCategory: API\n  - name: Places Insights\n    baseURL: ''\n    tags:\n      - Analytics\n      - Bigquery\n      - Insights\n      - Places\n    serviceName: Places Insights\n    serviceCategory: API\n  - name: Air Quality API\n    baseURL: ''\n    tags:\n      - Air-Quality\n      - Environment\n      - Health\n      - Pollution\n    serviceName: Air Quality API\n    serviceCategory:\
  \ API\n  - name: Pollen API\n    baseURL: ''\n    tags:\n      - Allergy\n      - Environment\n      - Health\n      - Pollen\n    serviceName: Pollen API\n    serviceCategory: API\n  - name: Solar API\n    baseURL: ''\n    tags:\n      - Energy\n      - Environment\n      - Solar\n      - Sustainability\n    serviceName: Solar API\n    serviceCategory: API\n  - name: Weather API\n    baseURL: ''\n    tags:\n      - Environment\n      - Forecast\n      - Temperature\n      - Weather\n    serviceName: Weather API\n    serviceCategory: API\n  - name: Street View Insights\n    baseURL: ''\n    tags:\n      - Analytics\n      - Imagery\n      - Insights\n      - Street-View\n    serviceName: Street View Insights\n    serviceCategory: API\n  - name: Imagery Insights API\n    baseURL: ''\n    tags:\n      - Ai\n      - Analytics\n      - Imagery\n      - Insights\n    serviceName: Imagery Insights API\n    serviceCategory: API\n  - name: Roads Management Insights\n    baseURL: ''\n    tags:\n\
  \      - Analytics\n      - Insights\n      - Roads\n      - Transportation\n    serviceName: Roads Management Insights\n    serviceCategory: API\n  - name: Google Earth\n    baseURL: ''\n    tags:\n      - Analytics\n      - Earth\n      - Geospatial\n      - Imagery\n    serviceName: Google Earth\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-maps/refs/heads/main/finops/google-maps-finops.yml
sources: []
specification: FinOps Framework
tags:
- Environment
- Geocoding
- Geolocation
- Maps
- Navigation
- Places
- Routing
- Solar
- FinOps
- Cost Management
- FOCUS
---
