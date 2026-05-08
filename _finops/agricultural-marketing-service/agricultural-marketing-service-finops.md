---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: agricultural-marketing-service-mars-api.yaml
  format: yaml
  label: USDA AMS MARS API (MyMarketNews)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/agricultural-marketing-service/refs/heads/main/openapi/agricultural-marketing-service-mars-api.yaml
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
description: FinOps framework definition for the Agricultural Marketing Service API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Agricultural Marketing Service
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Agricultural Marketing Service
  PublisherName: Agricultural Marketing Service
  ServiceCategory: Developer Tools / API
  ServiceName: Agricultural Marketing Service
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
name: Agricultural Marketing Service Finops
provider_name: Agricultural Marketing Service
provider_slug: agricultural-marketing-service
publisher_name: Agricultural Marketing Service
service_category: API
slug: agricultural-marketing-service-finops
source_filename: agricultural-marketing-service-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Agricultural Marketing Service\nproviderId: agricultural-marketing-service\npublisherName: Agricultural Marketing Service\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agriculture\n  - Federal Government\n  - Market News\n  - Livestock\n  - Dairy\n  - Fruits And Vegetables\n  - Cotton\n  - Tobacco\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Agricultural Marketing Service API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to\
  \ engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Agricultural Marketing Service\n  ServiceCategory: Developer Tools / API\n  ProviderName: Agricultural Marketing Service\n  PublisherName: Agricultural Marketing Service\n  InvoiceIssuerName: Agricultural Marketing Service\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: USDA AMS MARS API (MyMarketNews)\n    baseURL: https://marsapi.ams.usda.gov/services/v1.2\n    tags:\n      - Market News\n      - Commodity Prices\n      - Agriculture\n      - Livestock\n      - Dairy\n      - Fruits And Vegetables\n    serviceName: USDA AMS MARS API (MyMarketNews)\n    serviceCategory: API\n  - name: USDA AMS LMPRS API (Livestock Mandatory Price Reporting)\n    baseURL: https://mpr.datamart.ams.usda.gov\n    tags:\n      - Livestock\n      - Price Reporting\n\
  \      - Cattle\n      - Hogs\n      - Agriculture\n    serviceName: USDA AMS LMPRS API (Livestock Mandatory Price Reporting)\n    serviceCategory: API\n  - name: USDA Local Food Directories API\n    baseURL: https://www.usdalocalfoodportal.com\n    tags:\n      - Local Food\n      - Farmers Markets\n      - Food Hubs\n      - CSA\n      - Agriculture\n    serviceName: USDA Local Food Directories API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/agricultural-marketing-service/refs/heads/main/finops/agricultural-marketing-service-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agriculture
- Federal Government
- Market News
- Livestock
- Dairy
- Fruits And Vegetables
- Cotton
- Tobacco
- FinOps
- Cost Management
- FOCUS
---
