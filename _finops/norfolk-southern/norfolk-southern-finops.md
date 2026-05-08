---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: norfolk-southern-shipment-status-api.yml
  format: yaml
  label: Norfolk Southern Shipment Status API
  slug: shipment-status
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/norfolk-southern/refs/heads/main/openapi/norfolk-southern-shipment-status-api.yml
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
description: FinOps framework definition for the Norfolk Southern API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Norfolk Southern
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Norfolk Southern
  PublisherName: Norfolk Southern
  ServiceCategory: Developer Tools / API
  ServiceName: Norfolk Southern
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
name: Norfolk Southern Finops
provider_name: Norfolk Southern
provider_slug: norfolk-southern
publisher_name: Norfolk Southern
service_category: API
slug: norfolk-southern-finops
source_filename: norfolk-southern-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Norfolk Southern\nproviderId: norfolk-southern\npublisherName: Norfolk Southern\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Freight\n  - Logistics\n  - Railroad\n  - Shipping\n  - Transportation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Norfolk Southern API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Norfolk Southern\n  ServiceCategory: Developer Tools / API\n  ProviderName: Norfolk Southern\n  PublisherName: Norfolk Southern\n  InvoiceIssuerName: Norfolk Southern\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API\
  \ responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Norfolk Southern Shipment Status API\n    baseURL: https://api.nscorp.com\n    tags:\n      - Freight\n      - Railroad\n      - Shipment\n      - Tracking\n    serviceName: Norfolk Southern Shipment Status API\n    serviceCategory: API\n  - name: Norfolk Southern Trip Plan API\n    baseURL: https://api.nscorp.com\n    tags:\n      - ETA\n      - Railroad\n      - Route\n      - Trip Plan\n    serviceName: Norfolk Southern Trip Plan API\n    serviceCategory: API\n  - name: Norfolk Southern Gate Receipts API\n    baseURL: https://api.nscorp.com\n    tags:\n      - Gate Receipts\n      - Intermodal\n      - Terminal\n    serviceName: Norfolk Southern Gate\
  \ Receipts API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    url: https://apievangelist.com\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/norfolk-southern/refs/heads/main/finops/norfolk-southern-finops.yml
sources: []
specification: FinOps Framework
tags:
- Freight
- Logistics
- Railroad
- Shipping
- Transportation
- FinOps
- Cost Management
- FOCUS
---
