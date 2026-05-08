---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: mapquest-openapi.yml
  format: yaml
  label: MapQuest Directions API
  slug: mapquest-directions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mapquest/refs/heads/main/openapi/mapquest-openapi.yml
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
description: FinOps framework definition for the MapQuest API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: MapQuest
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: MapQuest
  PublisherName: MapQuest
  ServiceCategory: Developer Tools / API
  ServiceName: MapQuest
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
name: Mapquest Finops
provider_name: MapQuest
provider_slug: mapquest
publisher_name: MapQuest
service_category: API
slug: mapquest-finops
source_filename: mapquest-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: MapQuest\nproviderId: mapquest\npublisherName: MapQuest\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Geocoding\n  - Mapping\n  - Maps\n  - Navigation\n  - Routing\n  - Traffic\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the MapQuest API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: MapQuest\n  ServiceCategory: Developer Tools / API\n  ProviderName: MapQuest\n  PublisherName: MapQuest\n  InvoiceIssuerName: MapQuest\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: MapQuest Directions API\n    baseURL: https://www.mapquestapi.com/directions/v2\n    tags:\n      - Directions\n      - Navigation\n      - Routing\n    serviceName: MapQuest Directions API\n    serviceCategory: API\n  - name: MapQuest Geocoding API\n    baseURL: https://www.mapquestapi.com/geocoding/v1\n    tags:\n      - Geocoding\n      - Location\n    serviceName: MapQuest Geocoding API\n    serviceCategory: API\n  - name: MapQuest Static Map API\n    baseURL: https://www.mapquestapi.com/staticmap/v5\n    tags:\n      - Maps\n      - Static Maps\n    serviceName: MapQuest Static Map API\n    serviceCategory: API\n  - name: MapQuest Traffic API\n    baseURL: https://www.mapquestapi.com/traffic/v2\n\
  \    tags:\n      - Incidents\n      - Traffic\n    serviceName: MapQuest Traffic API\n    serviceCategory: API\n  - name: MapQuest Search API\n    baseURL: https://www.mapquestapi.com/search/v2\n    tags:\n      - Points of Interest\n      - Search\n    serviceName: MapQuest Search API\n    serviceCategory: API\n  - name: MapQuest Place Search API\n    baseURL: https://www.mapquestapi.com/search/v5\n    tags:\n      - Place Search\n      - Points of Interest\n      - Search\n    serviceName: MapQuest Place Search API\n    serviceCategory: API\n  - name: MapQuest Search Ahead API\n    baseURL: https://www.mapquestapi.com/search/v5\n    tags:\n      - Autocomplete\n      - Search\n      - Search Ahead\n    serviceName: MapQuest Search Ahead API\n    serviceCategory: API\n  - name: MapQuest Geolocation API\n    baseURL: https://www.mapquestapi.com/geolocation/v1\n    tags:\n      - Geolocation\n      - Location\n    serviceName: MapQuest Geolocation API\n    serviceCategory: API\n  - name:\
  \ MapQuest Icons API\n    baseURL: https://www.mapquestapi.com/icons/v2\n    tags:\n      - Icons\n      - Maps\n    serviceName: MapQuest Icons API\n    serviceCategory: API\n  - name: MapQuest Data Manager API\n    baseURL: https://www.mapquestapi.com/datamanager/v2\n    tags:\n      - Custom Data\n      - Data Management\n    serviceName: MapQuest Data Manager API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mapquest/refs/heads/main/finops/mapquest-finops.yml
sources: []
specification: FinOps Framework
tags:
- Geocoding
- Mapping
- Maps
- Navigation
- Routing
- Traffic
- FinOps
- Cost Management
- FOCUS
---
