---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sightline-api.yml
  format: yaml
  label: Goodyear SightLine API
  slug: sightline-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/goodyear-tire-and-rubber/refs/heads/main/openapi/sightline-api.yml
- filename: gaas-portal.yml
  format: yaml
  label: Goodyear API Management Portal
  slug: gaas-portal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/goodyear-tire-and-rubber/refs/heads/main/openapi/gaas-portal.yml
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
description: FinOps framework definition for the Goodyear Tire & Rubber API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Goodyear Tire & Rubber
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Goodyear Tire & Rubber
  PublisherName: Goodyear Tire & Rubber
  ServiceCategory: Developer Tools / API
  ServiceName: Goodyear Tire & Rubber
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
name: Goodyear Tire And Rubber Finops
provider_name: Goodyear Tire & Rubber
provider_slug: goodyear-tire-and-rubber
publisher_name: Goodyear Tire & Rubber
service_category: API
slug: goodyear-tire-and-rubber-finops
source_filename: goodyear-tire-and-rubber-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Goodyear Tire & Rubber\nproviderId: goodyear-tire-and-rubber\npublisherName: Goodyear Tire & Rubber\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Connected Vehicles\n  - Fleet Management\n  - IoT\n  - Telematics\n  - Tires\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Goodyear Tire & Rubber API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Goodyear Tire & Rubber\n  ServiceCategory: Developer Tools / API\n  ProviderName: Goodyear Tire & Rubber\n  PublisherName: Goodyear Tire & Rubber\n  InvoiceIssuerName: Goodyear Tire & Rubber\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Goodyear SightLine API\n    baseURL: https://developer.goodyearsightline.com\n    tags:\n      - Connected Vehicles\n      - IoT\n      - Telematics\n      - Tire Data\n      - Tires\n    serviceName: Goodyear SightLine API\n    serviceCategory: API\n  - name: Goodyear API Management Portal\n    baseURL: https://gaas-portal.goodyear.com\n    tags:\n      - API Management\n      - Fleet Management\n      - Tires\n    serviceName: Goodyear API Management Portal\n    serviceCategory: API\n  - name: Goodyear Truck Tire Catalog API\n    baseURL: https://api.catalog.goodyeartrucktires.com\n    tags:\n   \
  \   - Catalog\n      - Tires\n      - Truck Tires\n    serviceName: Goodyear Truck Tire Catalog API\n    serviceCategory: API\n  - name: Goodyear Work Order API\n    baseURL: https://api.workorder.goodyeartrucktires.com\n    tags:\n      - Fleet Management\n      - Tires\n      - Work Orders\n    serviceName: Goodyear Work Order API\n    serviceCategory: API\n  - name: Goodyear Service Ticket API\n    baseURL: https://api.serviceticket.goodyeartrucktires.com\n    tags:\n      - Fleet Management\n      - Service Tickets\n      - Tires\n    serviceName: Goodyear Service Ticket API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/goodyear-tire-and-rubber/refs/heads/main/finops/goodyear-tire-and-rubber-finops.yml
sources: []
specification: FinOps Framework
tags:
- Connected Vehicles
- Fleet Management
- IoT
- Telematics
- Tires
- FinOps
- Cost Management
- FOCUS
---
