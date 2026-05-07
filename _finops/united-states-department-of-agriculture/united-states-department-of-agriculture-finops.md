---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: yaml-spec
  format: yaml
  label: USDA FoodData Central API
  slug: usda-fooddata-central-api
  spec_type: OpenAPI
  url: https://api.nal.usda.gov/fdc/v1/yaml-spec?api_key=DEMO_KEY
- filename: usda-nass-quickstats-openapi.yml
  format: yaml
  label: USDA NASS Quick Stats API
  slug: usda-nass-quickstats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-department-of-agriculture/refs/heads/main/openapi/usda-nass-quickstats-openapi.yml
- filename: usda-ers-arms-openapi.yml
  format: yaml
  label: USDA ERS ARMS Data API
  slug: usda-ers-arms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-department-of-agriculture/refs/heads/main/openapi/usda-ers-arms-openapi.yml
- filename: usda-nrcs-awdb-openapi.yml
  format: yaml
  label: USDA NRCS AWDB Water and Climate REST API
  slug: usda-nrcs-awdb-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-department-of-agriculture/refs/heads/main/openapi/usda-nrcs-awdb-openapi.yml
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
description: FinOps framework definition for the United States Department of Agriculture API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: United States Department of Agriculture
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: United States Department of Agriculture
  PublisherName: United States Department of Agriculture
  ServiceCategory: Developer Tools / API
  ServiceName: United States Department of Agriculture
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
name: United States Department Of Agriculture Finops
provider_name: United States Department of Agriculture
provider_slug: united-states-department-of-agriculture
publisher_name: United States Department of Agriculture
service_category: API
slug: united-states-department-of-agriculture-finops
source_filename: united-states-department-of-agriculture-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: United States Department of Agriculture\nproviderId: united-states-department-of-agriculture\npublisherName: United States Department of Agriculture\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Federal Government\n  - Agriculture\n  - Food Safety\n  - Nutrition\n  - Rural Development\n  - Climate\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the United States Department of Agriculture API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n  across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs\
  \ visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n   \
  \   - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: United States Department of Agriculture\n  ServiceCategory: Developer Tools / API\n  ProviderName: United States Department of Agriculture\n  PublisherName: United States Department of Agriculture\n  InvoiceIssuerName: United States Department of Agriculture\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable\
  \ API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: USDA FoodData Central API\n    baseURL: https://api.nal.usda.gov/fdc/v1\n    tags:\n      - Food\n      - Nutrition\n      - Agriculture\n      - Federal Government\n    serviceName: USDA FoodData Central API\n    serviceCategory: API\n  - name: USDA NASS Quick Stats API\n    baseURL: https://quickstats.nass.usda.gov/api\n    tags:\n      - Agriculture\n      - Statistics\n      - Crops\n      - Livestock\n      - Federal Government\n\
  \    serviceName: USDA NASS Quick Stats API\n    serviceCategory: API\n  - name: USDA ERS ARMS Data API\n    baseURL: https://api.ers.usda.gov/data/arms\n    tags:\n      - Agriculture\n      - Economics\n      - Farm Management\n      - Federal Government\n    serviceName: USDA ERS ARMS Data API\n    serviceCategory: API\n  - name: USDA NRCS AWDB Water and Climate REST API\n    baseURL: https://wcc.sc.egov.usda.gov/awdbRestApi/services/v1\n    tags:\n      - Water\n      - Climate\n      - Snow\n      - SNOTEL\n      - Federal Government\n    serviceName: USDA NRCS AWDB Water and Climate REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-states-department-of-agriculture/refs/heads/main/finops/united-states-department-of-agriculture-finops.yml
sources: []
specification: FinOps Framework
tags:
- Federal Government
- Agriculture
- Food Safety
- Nutrition
- Rural Development
- Climate
- FinOps
- Cost Management
- FOCUS
---
