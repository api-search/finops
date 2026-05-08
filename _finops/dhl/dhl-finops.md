---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dhl-openapi.yml
  format: yaml
  label: Location Finder Unified
  slug: location-finder-unified
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dhl/refs/heads/main/openapi/dhl-openapi.yml
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
description: FinOps framework definition for the DHL API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: DHL
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: DHL
  PublisherName: DHL
  ServiceCategory: Developer Tools / API
  ServiceName: DHL
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
name: Dhl Finops
provider_name: DHL
provider_slug: dhl
publisher_name: DHL
service_category: API
slug: dhl-finops
source_filename: dhl-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: DHL\nproviderId: dhl\npublisherName: DHL\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Freight\n  - Logistics\n  - Shipping\n  - eCommerce\n  - Tracking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the DHL API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: DHL\n  ServiceCategory: Developer Tools / API\n  ProviderName: DHL\n  PublisherName: DHL\n  InvoiceIssuerName: DHL\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n \
  \     - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Location Finder Unified\n    baseURL: ''\n    tags:\n      - Locations\n      - Logistics\n    serviceName: Location Finder Unified\n    serviceCategory: API\n  - name: Shipment Tracking Unified\n    baseURL: ''\n    tags:\n      - Tracking\n      - Shipping\n    serviceName: Shipment Tracking Unified\n    serviceCategory: API\n  - name: Shipment Tracking Unified Push\n    baseURL: ''\n    tags:\n      - Tracking\n      - Push\n    serviceName: Shipment Tracking Unified Push\n    serviceCategory: API\n  - name: User Guide DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - eCommerce\n      - Americas\n    serviceName: User Guide DHL eCommerce Americas\n    serviceCategory: API\n  - name: Additional Services DHL Freight\n    baseURL: ''\n\
  \    tags:\n      - Freight\n      - Services\n    serviceName: Additional Services DHL Freight\n    serviceCategory: API\n  - name: Authentication DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Authentication\n      - eCommerce\n    serviceName: Authentication DHL eCommerce Americas\n    serviceCategory: API\n  - name: Authentication API DHL Freight\n    baseURL: ''\n    tags:\n      - Authentication\n      - Freight\n    serviceName: Authentication API DHL Freight\n    serviceCategory: API\n  - name: Authentication API Post Parcel Germany\n    baseURL: ''\n    tags:\n      - Authentication\n      - Germany\n    serviceName: Authentication API Post Parcel Germany\n    serviceCategory: API\n  - name: Changelog DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Changelog\n      - eCommerce\n    serviceName: Changelog DHL eCommerce Americas\n    serviceCategory: API\n  - name: DATAFACTORY AUTOCOMPLETE 2.0\n    baseURL: ''\n    tags:\n      - Address\n      - Germany\n\
  \    serviceName: DATAFACTORY AUTOCOMPLETE 2.0\n    serviceCategory: API\n  - name: Deutsche Post Hybrid Mail Shipments E-POST\n    baseURL: ''\n    tags:\n      - Mail\n      - Germany\n    serviceName: Deutsche Post Hybrid Mail Shipments E-POST\n    serviceCategory: API\n  - name: Deutsche Post International\n    baseURL: ''\n    tags:\n      - Mail\n      - International\n    serviceName: Deutsche Post International\n    serviceCategory: API\n  - name: Deutsche Post INTERNETMARKE\n    baseURL: ''\n    tags:\n      - Postage\n      - Germany\n    serviceName: Deutsche Post INTERNETMARKE\n    serviceCategory: API\n  - name: Deutsche Post Order Management AM\n    baseURL: ''\n    tags:\n      - Orders\n      - Germany\n    serviceName: Deutsche Post Order Management AM\n    serviceCategory: API\n  - name: Deutsche Post Print-Mailing Dispatch Preparation\n    baseURL: ''\n    tags:\n      - Marketing\n      - Mail\n    serviceName: Deutsche Post Print-Mailing Dispatch Preparation\n    serviceCategory:\
  \ API\n  - name: Deutsche Post Print-Mailing Targeting\n    baseURL: ''\n    tags:\n      - Marketing\n      - Targeting\n    serviceName: Deutsche Post Print-Mailing Targeting\n    serviceCategory: API\n  - name: DHL eCommerce Europe eConnect\n    baseURL: ''\n    tags:\n      - eCommerce\n      - Europe\n    serviceName: DHL eCommerce Europe eConnect\n    serviceCategory: API\n  - name: DHL eCommerce Europe eConnect Beta\n    baseURL: ''\n    tags:\n      - eCommerce\n      - Beta\n    serviceName: DHL eCommerce Europe eConnect Beta\n    serviceCategory: API\n  - name: DHL Parcel DE Pickup\n    baseURL: ''\n    tags:\n      - Pickup\n      - Germany\n    serviceName: DHL Parcel DE Pickup\n    serviceCategory: API\n  - name: DHL Parcel DE Postnumber\n    baseURL: ''\n    tags:\n      - Validation\n      - Germany\n    serviceName: DHL Parcel DE Postnumber\n    serviceCategory: API\n  - name: DHL Parcel DE Private Shipping\n    baseURL: ''\n    tags:\n      - Shipping\n      - Germany\n\
  \    serviceName: DHL Parcel DE Private Shipping\n    serviceCategory: API\n  - name: DHL Parcel DE Returns\n    baseURL: ''\n    tags:\n      - Returns\n      - Germany\n    serviceName: DHL Parcel DE Returns\n    serviceCategory: API\n  - name: DHL Parcel DE Shipping\n    baseURL: ''\n    tags:\n      - Shipping\n      - Germany\n    serviceName: DHL Parcel DE Shipping\n    serviceCategory: API\n  - name: DHL Parcel DE Tracking\n    baseURL: ''\n    tags:\n      - Tracking\n      - Germany\n    serviceName: DHL Parcel DE Tracking\n    serviceCategory: API\n  - name: Document DHL Global Forwarding\n    baseURL: ''\n    tags:\n      - Documents\n      - Forwarding\n    serviceName: Document DHL Global Forwarding\n    serviceCategory: API\n  - name: Duty and Tax DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Duty\n      - Tax\n    serviceName: Duty and Tax DHL eCommerce Americas\n    serviceCategory: API\n  - name: Duty and Tax Calculator Unified\n    baseURL: ''\n    tags:\n\
  \      - Duty\n      - Tax\n    serviceName: Duty and Tax Calculator Unified\n    serviceCategory: API\n  - name: DHL eCommerce UK\n    baseURL: ''\n    tags:\n      - eCommerce\n      - United Kingdom\n    serviceName: DHL eCommerce UK\n    serviceCategory: API\n  - name: Parcel EU BE LU NL\n    baseURL: ''\n    tags:\n      - Parcel\n      - Europe\n    serviceName: Parcel EU BE LU NL\n    serviceCategory: API\n  - name: Pickup Cancellation DHL eCommerce India\n    baseURL: ''\n    tags:\n      - Pickup\n      - India\n    serviceName: Pickup Cancellation DHL eCommerce India\n    serviceCategory: API\n  - name: Price Quote DHL Freight\n    baseURL: ''\n    tags:\n      - Pricing\n      - Freight\n    serviceName: Price Quote DHL Freight\n    serviceCategory: API\n  - name: Print DHL Freight\n    baseURL: ''\n    tags:\n      - Print\n      - Freight\n    serviceName: Print DHL Freight\n    serviceCategory: API\n  - name: Product DHL Freight\n    baseURL: ''\n    tags:\n      - Products\n\
  \      - Freight\n    serviceName: Product DHL Freight\n    serviceCategory: API\n  - name: Product and Sub-Product Pickup Detail DHL eCommerce India\n    baseURL: ''\n    tags:\n      - Products\n      - India\n    serviceName: Product and Sub-Product Pickup Detail DHL eCommerce India\n    serviceCategory: API\n  - name: Product Finder DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Products\n      - Americas\n    serviceName: Product Finder DHL eCommerce Americas\n    serviceCategory: API\n  - name: Products API Post Parcel Germany\n    baseURL: ''\n    tags:\n      - Products\n      - Germany\n    serviceName: Products API Post Parcel Germany\n    serviceCategory: API\n  - name: Push API DHL Global Forwarding\n    baseURL: ''\n    tags:\n      - Push\n      - Forwarding\n    serviceName: Push API DHL Global Forwarding\n    serviceCategory: API\n  - name: References DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Reference\n      - eCommerce\n    serviceName:\
  \ References DHL eCommerce Americas\n    serviceCategory: API\n  - name: Registration for Pickup DHL eCommerce India\n    baseURL: ''\n    tags:\n      - Pickup\n      - India\n    serviceName: Registration for Pickup DHL eCommerce India\n    serviceCategory: API\n  - name: Return Label DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Returns\n      - Americas\n    serviceName: Return Label DHL eCommerce Americas\n    serviceCategory: API\n  - name: Shipment Booking DHL Freight\n    baseURL: ''\n    tags:\n      - Booking\n      - Freight\n    serviceName: Shipment Booking DHL Freight\n    serviceCategory: API\n  - name: Shipment Booking DHL Global Forwarding\n    baseURL: ''\n    tags:\n      - Booking\n      - Forwarding\n    serviceName: Shipment Booking DHL Global Forwarding\n    serviceCategory: API\n  - name: Shipment Label DHL Global Forwarding\n    baseURL: ''\n    tags:\n      - Labels\n      - Forwarding\n    serviceName: Shipment Label DHL Global Forwarding\n    serviceCategory:\
  \ API\n  - name: Shipment Status DHL Global Forwarding\n    baseURL: ''\n    tags:\n      - Status\n      - Forwarding\n    serviceName: Shipment Status DHL Global Forwarding\n    serviceCategory: API\n  - name: Shipment Tracking DHL eCommerce India\n    baseURL: ''\n    tags:\n      - Tracking\n      - India\n    serviceName: Shipment Tracking DHL eCommerce India\n    serviceCategory: API\n  - name: Shipment Tracking v2 DHL Global Forwarding\n    baseURL: ''\n    tags:\n      - Tracking\n      - Forwarding\n    serviceName: Shipment Tracking v2 DHL Global Forwarding\n    serviceCategory: API\n  - name: Time Table DHL Freight\n    baseURL: ''\n    tags:\n      - Schedule\n      - Freight\n    serviceName: Time Table DHL Freight\n    serviceCategory: API\n  - name: Tracking DHL eCommerce Americas\n    baseURL: ''\n    tags:\n      - Tracking\n      - Americas\n    serviceName: Tracking DHL eCommerce Americas\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n   \
  \ metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dhl/refs/heads/main/finops/dhl-finops.yml
sources: []
specification: FinOps Framework
tags:
- Freight
- Logistics
- Shipping
- eCommerce
- Tracking
- FinOps
- Cost Management
- FOCUS
---
