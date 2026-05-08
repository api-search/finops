---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: united-states-postal-service-addresses-openapi.yml
  format: yaml
  label: USPS Addresses API
  slug: usps-addresses-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-addresses-openapi.yml
- filename: united-states-postal-service-tracking-openapi.yml
  format: yaml
  label: USPS Tracking API
  slug: usps-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-tracking-openapi.yml
- filename: united-states-postal-service-domestic-prices-openapi.yml
  format: yaml
  label: USPS Domestic Prices API
  slug: usps-domestic-prices-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-domestic-prices-openapi.yml
- filename: united-states-postal-service-carrier-pickup-openapi.yml
  format: yaml
  label: USPS Carrier Pickup API
  slug: usps-carrier-pickup-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/openapi/united-states-postal-service-carrier-pickup-openapi.yml
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
description: FinOps framework definition for the United States Postal Service API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: United States Postal Service
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: United States Postal Service
  PublisherName: United States Postal Service
  ServiceCategory: Developer Tools / API
  ServiceName: United States Postal Service
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
name: United States Postal Service Finops
provider_name: United States Postal Service
provider_slug: united-states-postal-service
publisher_name: United States Postal Service
service_category: API
slug: united-states-postal-service-finops
source_filename: united-states-postal-service-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: United States Postal Service\nproviderId: united-states-postal-service\npublisherName: United States Postal Service\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Government\n  - Postal Service\n  - Shipping\n  - Logistics\n  - Address Validation\n  - Package Tracking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the United States Postal Service API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: United States Postal Service\n  ServiceCategory: Developer Tools / API\n  ProviderName: United States Postal Service\n  PublisherName: United States Postal Service\n  InvoiceIssuerName: United States Postal Service\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: USPS Addresses API\n    baseURL: https://apis.usps.com\n    tags:\n      - Addresses\n      - Address Validation\n      - Government\n    serviceName: USPS Addresses API\n    serviceCategory: API\n  - name: USPS Tracking API\n    baseURL: https://apis.usps.com\n    tags:\n      - Tracking\n      - Package Tracking\n      - Government\n    serviceName: USPS Tracking API\n    serviceCategory: API\n  - name: USPS Domestic Prices API\n    baseURL: https://apis.usps.com\n    tags:\n      - Pricing\n      - Postage\n      - Shipping\n\
  \      - Government\n    serviceName: USPS Domestic Prices API\n    serviceCategory: API\n  - name: USPS Carrier Pickup API\n    baseURL: https://apis.usps.com\n    tags:\n      - Carrier Pickup\n      - Shipping\n      - Government\n    serviceName: USPS Carrier Pickup API\n    serviceCategory: API\n  - name: USPS International Prices API\n    baseURL: https://apis.usps.com\n    tags:\n      - International\n      - Pricing\n      - Postage\n      - Government\n    serviceName: USPS International Prices API\n    serviceCategory: API\n  - name: USPS Domestic Labels API\n    baseURL: https://apis.usps.com\n    tags:\n      - Labels\n      - Shipping\n      - Government\n    serviceName: USPS Domestic Labels API\n    serviceCategory: API\n  - name: USPS International Labels API\n    baseURL: https://apis.usps.com\n    tags:\n      - International\n      - Labels\n      - Shipping\n      - Government\n    serviceName: USPS International Labels API\n    serviceCategory: API\n  - name: USPS\
  \ Locations API\n    baseURL: https://apis.usps.com\n    tags:\n      - Locations\n      - Post Offices\n      - Government\n    serviceName: USPS Locations API\n    serviceCategory: API\n  - name: USPS Service Standards API\n    baseURL: https://apis.usps.com\n    tags:\n      - Service Standards\n      - Delivery\n      - Government\n    serviceName: USPS Service Standards API\n    serviceCategory: API\n  - name: USPS Shipping Options API\n    baseURL: https://apis.usps.com\n    tags:\n      - Shipping\n      - Pricing\n      - Government\n    serviceName: USPS Shipping Options API\n    serviceCategory: API\n  - name: USPS SCAN Forms API\n    baseURL: https://apis.usps.com\n    tags:\n      - SCAN Forms\n      - Shipping\n      - Government\n    serviceName: USPS SCAN Forms API\n    serviceCategory: API\n  - name: USPS OAuth API\n    baseURL: https://apis.usps.com\n    tags:\n      - Authentication\n      - OAuth\n      - Government\n    serviceName: USPS OAuth API\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/united-states-postal-service/refs/heads/main/finops/united-states-postal-service-finops.yml
sources: []
specification: FinOps Framework
tags:
- Government
- Postal Service
- Shipping
- Logistics
- Address Validation
- Package Tracking
- FinOps
- Cost Management
- FOCUS
---
