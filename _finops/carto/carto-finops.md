---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Carto API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Carto
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Carto
  PublisherName: Carto
  ServiceCategory: Developer Tools / API
  ServiceName: Carto
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
name: Carto Finops
provider_name: Carto
provider_slug: carto
publisher_name: Carto
service_category: API
slug: carto-finops
source_filename: carto-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Carto\nproviderId: carto\npublisherName: Carto\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Location Intelligence\n  - Geospatial\n  - Mapping\n  - GIS\n  - SQL\n  - BigQuery\n  - Snowflake\n  - Data Warehouse\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Carto API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every\
  \ chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n   \
  \ capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Carto\n  ServiceCategory: Developer Tools / API\n  ProviderName: Carto\n  PublisherName: Carto\n  InvoiceIssuerName: Carto\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CARTO Maps API\n    baseURL: https://gcp-us-east1.api.carto.com\n    tags:\n      - Maps\n      - Tiles\n      - Vector\n      - Geospatial\n    serviceName: CARTO Maps API\n    serviceCategory: API\n  - name: CARTO SQL API\n    baseURL: https://gcp-us-east1.api.carto.com\n    tags:\n      - SQL\n      - Analytics\n      - Spatial\n    serviceName: CARTO SQL API\n    serviceCategory: API\n  - name: CARTO Workflows API\n    baseURL: https://gcp-us-east1.api.carto.com\n    tags:\n      - Workflows\n      - Analytics\n      - Automation\n    serviceName: CARTO Workflows API\n    serviceCategory: API\n  - name: CARTO Import API\n    baseURL: https://gcp-us-east1.api.carto.com\n    tags:\n\
  \      - Import\n      - Ingestion\n      - Data\n    serviceName: CARTO Import API\n    serviceCategory: API\n  - name: CARTO Data Observatory\n    baseURL: ''\n    tags:\n      - Data Catalog\n      - Datasets\n      - Third-Party Data\n    serviceName: CARTO Data Observatory\n    serviceCategory: API\n  - name: CARTO Accounts API\n    baseURL: https://accounts.app.carto.com\n    tags:\n      - Accounts\n      - Authentication\n      - OAuth\n    serviceName: CARTO Accounts API\n    serviceCategory: API\n  - name: CARTO for deck.gl\n    baseURL: ''\n    tags:\n      - SDK\n      - deck.gl\n      - Client Library\n    serviceName: CARTO for deck.gl\n    serviceCategory: API\n  - name: CARTO for React\n    baseURL: ''\n    tags:\n      - SDK\n      - React\n      - Client Library\n    serviceName: CARTO for React\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n\
  \    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carto/refs/heads/main/finops/carto-finops.yml
sources: []
specification: FinOps Framework
tags:
- Location Intelligence
- Geospatial
- Mapping
- GIS
- SQL
- BigQuery
- Snowflake
- Data Warehouse
- FinOps
- Cost Management
- FOCUS
---
