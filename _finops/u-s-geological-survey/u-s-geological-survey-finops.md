---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: usgs-earthquake-api-openapi.yaml
  format: yaml
  label: Earthquake Notifications, Feeds, and Web Services
  slug: earthquake-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/u-s-geological-survey/refs/heads/main/openapi/usgs-earthquake-api-openapi.yaml
- filename: usgs-water-data-api-openapi.yaml
  format: yaml
  label: USGS Water Data APIs
  slug: water-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/u-s-geological-survey/refs/heads/main/openapi/usgs-water-data-api-openapi.yaml
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
description: FinOps framework definition for the U.S. Geological Survey API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: U.S. Geological Survey
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: U.S. Geological Survey
  PublisherName: U.S. Geological Survey
  ServiceCategory: Developer Tools / API
  ServiceName: U.S. Geological Survey
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
name: U S Geological Survey Finops
provider_name: U.S. Geological Survey
provider_slug: u-s-geological-survey
publisher_name: U.S. Geological Survey
service_category: API
slug: u-s-geological-survey-finops
source_filename: u-s-geological-survey-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: U.S. Geological Survey\nproviderId: u-s-geological-survey\npublisherName: U.S. Geological Survey\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Federal Government\n  - Geological\n  - Earth Science\n  - Natural Resources\n  - Earthquake\n  - Water\n  - Hydrology\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the U.S. Geological Survey API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: U.S. Geological Survey\n  ServiceCategory: Developer Tools / API\n  ProviderName: U.S. Geological Survey\n  PublisherName: U.S. Geological Survey\n  InvoiceIssuerName: U.S. Geological Survey\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      -\
  \ region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Earthquake Notifications, Feeds, and Web Services\n    baseURL: https://earthquake.usgs.gov/fdsnws/event/1\n    tags:\n      - Earthquakes\n      - Seismic\n      - Geoscience\n    serviceName: Earthquake Notifications, Feeds, and Web Services\n    serviceCategory: API\n  - name: USGS Water Data APIs\n    baseURL: https://api.waterdata.usgs.gov/ogcapi/v0\n    tags:\n      - Water\n      - Hydrology\n      - Streamflow\n      - Groundwater\n    serviceName: USGS Water Data APIs\n    serviceCategory: API\n  - name: Asset Identifier Service (AIS)\n    baseURL:\
  \ ''\n    tags:\n      - Identifiers\n      - Research Data\n    serviceName: Asset Identifier Service (AIS)\n    serviceCategory: API\n  - name: Seismic Design Web Service\n    baseURL: ''\n    tags:\n      - Seismic\n      - Engineering\n    serviceName: Seismic Design Web Service\n    serviceCategory: API\n  - name: ScienceBase\n    baseURL: ''\n    tags:\n      - Research Data\n      - Data Repository\n    serviceName: ScienceBase\n    serviceCategory: API\n  - name: StreamStats Web Services\n    baseURL: ''\n    tags:\n      - Hydrology\n      - Streamflow\n      - Statistics\n    serviceName: StreamStats Web Services\n    serviceCategory: API\n  - name: USGS Water Services (Legacy)\n    baseURL: ''\n    tags:\n      - Water\n      - Hydrology\n      - Legacy\n    serviceName: USGS Water Services (Legacy)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n\
  \    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/u-s-geological-survey/refs/heads/main/finops/u-s-geological-survey-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Geological
- Earth Science
- Natural Resources
- Earthquake
- Water
- Hydrology
- FinOps
- Cost Management
- FOCUS
---
