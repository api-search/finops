---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: yardi-voyager-api-openapi.yml
  format: yaml
  label: Yardi Voyager API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/yardi/refs/heads/main/openapi/yardi-voyager-api-openapi.yml
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
description: FinOps framework definition for the Yardi API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Yardi
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Yardi
  PublisherName: Yardi
  ServiceCategory: Developer Tools / API
  ServiceName: Yardi
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
name: Yardi Finops
provider_name: Yardi
provider_slug: yardi
publisher_name: Yardi
service_category: API
slug: yardi-finops
source_filename: yardi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Yardi\nproviderId: yardi\npublisherName: Yardi\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accounting\n  - Commercial Real Estate\n  - Coworking\n  - Investment Management\n  - Multifamily\n  - Property Management\n  - Real Estate\n  - Residential\n  - Self Storage\n  - Senior Living\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Yardi API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams\
  \ in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Yardi\n  ServiceCategory: Developer Tools / API\n  ProviderName: Yardi\n  PublisherName: Yardi\n  InvoiceIssuerName: Yardi\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Yardi Voyager API\n    baseURL: https://api.yardi.com\n    tags:\n      - Accounting\n      - Commercial\n      - Property Management\n      - Real Estate\n      - Residential\n    serviceName: Yardi Voyager API\n    serviceCategory: API\n  - name: Yardi Voyager Commercial Data API\n    baseURL: https://api.yardi.com\n    tags:\n      - Commercial\n      - Data Export\n      - Leasing\n      - OSCRE\n    serviceName: Yardi Voyager Commercial Data API\n    serviceCategory: API\n  - name: Yardi RENTCafe API\n    baseURL: https://api.rentcafe.com\n    tags:\n      - Applications\n      - Multifamily\n      - Payments\n\
  \      - Portal\n      - Residents\n    serviceName: Yardi RENTCafe API\n    serviceCategory: API\n  - name: Yardi Maintenance IQ API\n    baseURL: https://api.yardi.com/maintenance\n    tags:\n      - Facilities\n      - Maintenance\n      - Vendors\n      - Work Orders\n    serviceName: Yardi Maintenance IQ API\n    serviceCategory: API\n  - name: Yardi Investment Manager API\n    baseURL: https://api.yardi.com/investment\n    tags:\n      - Analytics\n      - Asset Management\n      - Investment\n      - Reporting\n    serviceName: Yardi Investment Manager API\n    serviceCategory: API\n  - name: Yardi Store Web Services API\n    baseURL: https://api.yardi.com\n    tags:\n      - Reservations\n      - Self Storage\n      - SOAP\n      - Store Management\n    serviceName: Yardi Store Web Services API\n    serviceCategory: API\n  - name: Yardi Kube API\n    baseURL: https://api.yardikube.com\n    tags:\n      - Booking\n      - Coworking\n      - Flexible Workspace\n      - Webhooks\n\
  \    serviceName: Yardi Kube API\n    serviceCategory: API\n  - name: Yardi Senior Living EHR API\n    baseURL: https://api.yardi.com\n    tags:\n      - EHR\n      - Healthcare\n      - Pharmacy\n      - Senior Living\n    serviceName: Yardi Senior Living EHR API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/yardi/refs/heads/main/finops/yardi-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Commercial Real Estate
- Coworking
- Investment Management
- Multifamily
- Property Management
- Real Estate
- Residential
- Self Storage
- Senior Living
- FinOps
- Cost Management
- FOCUS
---
