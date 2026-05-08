---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: booking-com-demand-api-openapi.yml
  format: yaml
  label: Booking.com Demand API
  slug: demand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-demand-api-openapi.yml
- filename: booking-com-car-rentals-api-openapi.yml
  format: yaml
  label: Booking.com Car Rentals API
  slug: car-rentals-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-car-rentals-api-openapi.yml
- filename: booking-com-connectivity-content-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Content API
  slug: connectivity-content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-content-api-openapi.yml
- filename: booking-com-connectivity-reservations-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Reservations API
  slug: connectivity-reservations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-reservations-api-openapi.yml
- filename: booking-com-connectivity-rates-availability-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Rates and Availability API
  slug: connectivity-rates-availability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-rates-availability-api-openapi.yml
- filename: booking-com-connectivity-promotions-api-openapi.yml
  format: yaml
  label: Booking.com Connectivity Promotions API
  slug: connectivity-promotions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/openapi/booking-com-connectivity-promotions-api-openapi.yml
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
description: FinOps framework definition for the booking-com API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: booking-com
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: booking-com
  PublisherName: booking-com
  ServiceCategory: Developer Tools / API
  ServiceName: booking-com
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
name: Booking Com Finops
provider_name: booking-com
provider_slug: booking-com
publisher_name: booking-com
service_category: API
slug: booking-com-finops
source_filename: booking-com-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: booking-com\nproviderId: booking-com\npublisherName: booking-com\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the booking-com API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost\
  \ can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n     \
  \ - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: booking-com\n  ServiceCategory: Developer Tools / API\n  ProviderName: booking-com\n  PublisherName: booking-com\n  InvoiceIssuerName: booking-com\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n\
  \  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Booking.com Demand API\n    baseURL: https://demandapi.booking.com\n    tags:\n      - Accommodations\n      - Affiliates\n      - Booking\n      - Hotels\n      - Search\n      - Travel\n    serviceName: Booking.com Demand API\n    serviceCategory: API\n  - name: Booking.com Car Rentals API\n    baseURL: https://demandapi.booking.com\n    tags:\n      - Car Rentals\n      - Transportation\n      - Travel\n      - Vehicles\n    serviceName: Booking.com Car Rentals API\n    serviceCategory: API\n  - name: Booking.com Connectivity Content API\n    baseURL: https://supply-xml.booking.com\n    tags:\n      - Connectivity\n      - Content Management\n      - Hotels\n      - Properties\n    serviceName: Booking.com Connectivity Content API\n    serviceCategory: API\n \
  \ - name: Booking.com Connectivity Reservations API\n    baseURL: https://secure-supply-xml.booking.com\n    tags:\n      - Booking\n      - Connectivity\n      - Hotels\n      - Reservations\n    serviceName: Booking.com Connectivity Reservations API\n    serviceCategory: API\n  - name: Booking.com Connectivity Rates and Availability API\n    baseURL: https://supply-xml.booking.com\n    tags:\n      - Availability\n      - Connectivity\n      - Inventory\n      - Pricing\n      - Rates\n    serviceName: Booking.com Connectivity Rates and Availability API\n    serviceCategory: API\n  - name: Booking.com Connectivity Promotions API\n    baseURL: https://supply-xml.booking.com\n    tags:\n      - Connectivity\n      - Deals\n      - Discounts\n      - Marketing\n      - Promotions\n    serviceName: Booking.com Connectivity Promotions API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost\
  \ per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/booking-com/refs/heads/main/finops/booking-com-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
