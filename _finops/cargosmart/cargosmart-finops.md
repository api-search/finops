---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Container Booking API
  slug: cargosmart-container-booking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Shipment Tracking API
  slug: cargosmart-shipment-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Vessel Schedule API
  slug: cargosmart-vessel-schedule-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Shipping Documentation API
  slug: cargosmart-shipping-documents-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
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
description: FinOps framework definition for the CargoSmart API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CargoSmart
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CargoSmart
  PublisherName: CargoSmart
  ServiceCategory: Developer Tools / API
  ServiceName: CargoSmart
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
name: Cargosmart Finops
provider_name: CargoSmart
provider_slug: cargosmart
publisher_name: CargoSmart
service_category: API
slug: cargosmart-finops
source_filename: cargosmart-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CargoSmart\nproviderId: cargosmart\npublisherName: CargoSmart\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Booking\n  - Container\n  - Documentation\n  - GSBN\n  - IQAX\n  - Logistics\n  - Maritime\n  - Ocean Freight\n  - Schedule\n  - Shipping\n  - Supply Chain\n  - Tracking\n  - Visibility\n  - Vessel\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CargoSmart API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CargoSmart\n  ServiceCategory: Developer Tools / API\n  ProviderName: CargoSmart\n  PublisherName: CargoSmart\n  InvoiceIssuerName: CargoSmart\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CargoSmart Container Booking API\n    baseURL: https://api.cargosmart.com\n    tags:\n      - Booking\n      - Container\n      - Logistics\n      - Maritime\n      - Ocean Freight\n      - Shipping\n    serviceName: CargoSmart Container Booking API\n    serviceCategory: API\n  - name: CargoSmart Shipment Tracking API\n    baseURL: https://api.cargosmart.com\n    tags:\n      - Container\n      - Logistics\n      - Maritime\n      - Shipping\n      - Tracking\n      - Visibility\n    serviceName: CargoSmart Shipment Tracking API\n    serviceCategory: API\n  - name: CargoSmart\
  \ Vessel Schedule API\n    baseURL: https://api.cargosmart.com\n    tags:\n      - Logistics\n      - Maritime\n      - Port\n      - Schedule\n      - Shipping\n      - Vessel\n    serviceName: CargoSmart Vessel Schedule API\n    serviceCategory: API\n  - name: CargoSmart Shipping Documentation API\n    baseURL: https://api.cargosmart.com\n    tags:\n      - Bill of Lading\n      - Container\n      - Documentation\n      - EDI\n      - Maritime\n      - Shipping\n    serviceName: CargoSmart Shipping Documentation API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/finops/cargosmart-finops.yml
sources: []
specification: FinOps Framework
tags:
- Booking
- Container
- Documentation
- GSBN
- IQAX
- Logistics
- Maritime
- Ocean Freight
- Schedule
- Shipping
- Supply Chain
- Tracking
- Visibility
- Vessel
- FinOps
- Cost Management
- FOCUS
---
