---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: census-data-api-openapi.yml
  format: yaml
  label: Census Data API
  slug: census-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-census-bureau/refs/heads/main/openapi/census-data-api-openapi.yml
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
description: FinOps framework definition for the United States Census Bureau API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: United States Census Bureau
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: United States Census Bureau
  PublisherName: United States Census Bureau
  ServiceCategory: Developer Tools / API
  ServiceName: United States Census Bureau
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
name: United States Census Bureau Finops
provider_name: United States Census Bureau
provider_slug: united-states-census-bureau
publisher_name: United States Census Bureau
service_category: API
slug: united-states-census-bureau-finops
source_filename: united-states-census-bureau-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: United States Census Bureau\nproviderId: united-states-census-bureau\npublisherName: United States Census Bureau\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Demographics\n  - Federal Government\n  - Open Data\n  - Statistics\n  - Economics\n  - Population\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the United States Census Bureau API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: United States Census Bureau\n  ServiceCategory: Developer Tools / API\n  ProviderName: United States Census Bureau\n  PublisherName: United States Census Bureau\n  InvoiceIssuerName: United States Census Bureau\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Census Data API\n    baseURL: https://api.census.gov/data\n    tags:\n      - Demographics\n      - Statistics\n      - Open Data\n      - REST API\n    serviceName: Census Data API\n    serviceCategory: API\n  - name: TIGERweb GeoServices REST API\n    baseURL: https://tigerweb.geo.census.gov/arcgis/rest/services\n    tags:\n      - Geography\n      - GIS\n      - Boundaries\n      - Mapping\n    serviceName: TIGERweb GeoServices REST API\n    serviceCategory: API\n  - name: Census Geocoding Services\n    baseURL: https://geocoding.geo.census.gov/geocoder\n\
  \    tags:\n      - Geocoding\n      - Geography\n      - Address\n    serviceName: Census Geocoding Services\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-states-census-bureau/refs/heads/main/finops/united-states-census-bureau-finops.yml
sources: []
specification: FinOps Framework
tags:
- Demographics
- Federal Government
- Open Data
- Statistics
- Economics
- Population
- FinOps
- Cost Management
- FOCUS
---
