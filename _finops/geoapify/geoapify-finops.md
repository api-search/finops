---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: geoapify-forward-geocoding-api-openapi.yml
  format: yaml
  label: Forward Geocoding API
  slug: forward-geocoding
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/geoapify/refs/heads/main/openapi/geoapify-forward-geocoding-api-openapi.yml
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
description: FinOps framework definition for the Geoapify API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Geoapify
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Geoapify
  PublisherName: Geoapify
  ServiceCategory: Developer Tools / API
  ServiceName: Geoapify
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
name: Geoapify Finops
provider_name: Geoapify
provider_slug: geoapify
publisher_name: Geoapify
service_category: API
slug: geoapify-finops
source_filename: geoapify-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Geoapify\nproviderId: geoapify\npublisherName: Geoapify\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Geocoding\n  - Geospatial\n  - Location\n  - Maps\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Geoapify API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Geoapify\n  ServiceCategory: Developer Tools / API\n  ProviderName: Geoapify\n  PublisherName: Geoapify\n  InvoiceIssuerName: Geoapify\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Map Tiles API\n    baseURL: https://maps.geoapify.com/maptiles\n    tags:\n      - Maps\n    serviceName: Map Tiles API\n    serviceCategory: API\n  - name: Static Maps API\n    baseURL: https://maps.geoapify.com/staticmap\n    tags:\n      - Maps\n    serviceName: Static Maps API\n    serviceCategory: API\n  - name: Forward Geocoding API\n    baseURL: https://api.geoapify.com/geocode/search\n    tags:\n      - Geocoding\n    serviceName: Forward Geocoding API\n    serviceCategory: API\n  - name: Reverse Geocoding API\n    baseURL: https://api.geoapify.com/geocode/reverse\n    tags:\n      - Geocoding\n    serviceName: Reverse Geocoding API\n    serviceCategory: API\n  - name: Address Autocomplete API\n    baseURL: https://api.geoapify.com/geocode/autocomplete\n\
  \    tags:\n      - Geocoding\n    serviceName: Address Autocomplete API\n    serviceCategory: API\n  - name: IP Geolocation API\n    baseURL: https://api.geoapify.com/geocode/ip\n    tags:\n      - Geolocation\n    serviceName: IP Geolocation API\n    serviceCategory: API\n  - name: Routing API\n    baseURL: https://api.geoapify.com/routing\n    tags:\n      - Routing\n    serviceName: Routing API\n    serviceCategory: API\n  - name: Places API\n    baseURL: https://api.geoapify.com/places\n    tags:\n      - Places\n    serviceName: Places API\n    serviceCategory: API\n  - name: Boundaries API\n    baseURL: https://api.geoapify.com/boundaries\n    tags:\n      - Boundaries\n    serviceName: Boundaries API\n    serviceCategory: API\n  - name: Isoline API\n    baseURL: https://api.geoapify.com/isolines\n    tags:\n      - Reachability\n    serviceName: Isoline API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n\
  \    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/geoapify/refs/heads/main/finops/geoapify-finops.yml
sources: []
specification: FinOps Framework
tags:
- Geocoding
- Geospatial
- Location
- Maps
- FinOps
- Cost Management
- FOCUS
---
