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
description: FinOps framework definition for the CHAMP Cargosystems API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CHAMP Cargosystems
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CHAMP Cargosystems
  PublisherName: CHAMP Cargosystems
  ServiceCategory: Developer Tools / API
  ServiceName: CHAMP Cargosystems
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
name: Champ Finops
provider_name: CHAMP Cargosystems
provider_slug: champ
publisher_name: CHAMP Cargosystems
service_category: API
slug: champ-finops
source_filename: champ-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CHAMP Cargosystems\nproviderId: champ\npublisherName: CHAMP Cargosystems\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Air Cargo\n  - Airlines\n  - Booking\n  - Cargo\n  - Cargospot\n  - Freight\n  - Logistics\n  - Tracking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CHAMP Cargosystems API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CHAMP Cargosystems\n  ServiceCategory: Developer Tools / API\n  ProviderName: CHAMP Cargosystems\n  PublisherName: CHAMP Cargosystems\n  InvoiceIssuerName: CHAMP Cargosystems\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CHAMP Cargosystems Cargospot Acceptance API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Acceptance API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Active Allotments API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Active Allotments API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Agent Air Waybill Stock API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName:\
  \ CHAMP Cargosystems Cargospot Agent Air Waybill Stock API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Price Class API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Price Class API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Product API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Product API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Participant API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Participant API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Air Waybill Notes API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Air Waybill Notes API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Availability\
  \ and Price API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Availability and Price API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Get Flight Capacity API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Get Flight Capacity API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Handling Invoices API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Handling Invoices API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Booking API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Booking API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Manage Delivery API\n    baseURL: ''\n    tags:\n      - Air Cargo\n\
  \      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Manage Delivery API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot E-Invoices From ZATCA API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot E-Invoices From ZATCA API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Manage Price Info API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Manage Price Info API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Master Allotments API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Master Allotments API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Operational Flight and Truck API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n\
  \      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Operational Flight and Truck API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Payment API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Payment API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Pickup API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Pickup API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Price Class API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Price Class API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Product API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Product API\n    serviceCategory: API\n  - name: CHAMP Cargosystems\
  \ Publish Ad-Hoc Price Details API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Publish Ad-Hoc Price Details API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Publish Bookings API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Publish Bookings API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Participant API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Participant API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Scale Weight API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Scale Weight API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Schedule APIs\n    baseURL: ''\n    tags:\n      - Air Cargo\n\
  \      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Schedule APIs\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Search Sell Prices API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Search Sell Prices API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Search Unit Load Devices API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Search Unit Load Devices API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Track and Trace API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Track and Trace API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Update Dimension Details for a Shipment API\n    baseURL: ''\n    tags:\n      - Air Cargo\n    \
  \  - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Update Dimension Details for a Shipment API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Update Driver Details for Acceptance API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Update Driver Details for Acceptance API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Update Flight and Truck Capacity API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Update Flight and Truck Capacity API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot Update ULD Acceptance Details API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Update ULD Acceptance Details API\n    serviceCategory: API\n  - name: CHAMP Cargosystems Cargospot\
  \ Update Warehouse Location API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems Cargospot Update Warehouse Location API\n    serviceCategory: API\n  - name: CHAMP Cargosystems TGS House Air Waybill Declarations API\n    baseURL: ''\n    tags:\n      - Air Cargo\n      - Cargospot\n      - Logistics\n    serviceName: CHAMP Cargosystems TGS House Air Waybill Declarations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/champ/refs/heads/main/finops/champ-finops.yml
sources: []
specification: FinOps Framework
tags:
- Air Cargo
- Airlines
- Booking
- Cargo
- Cargospot
- Freight
- Logistics
- Tracking
- FinOps
- Cost Management
- FOCUS
---
