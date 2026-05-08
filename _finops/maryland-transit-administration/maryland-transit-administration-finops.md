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
description: FinOps framework definition for the Maryland Transit Administration API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Maryland Transit Administration
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Maryland Transit Administration
  PublisherName: Maryland Transit Administration
  ServiceCategory: Developer Tools / API
  ServiceName: Maryland Transit Administration
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
name: Maryland Transit Administration Finops
provider_name: Maryland Transit Administration
provider_slug: maryland-transit-administration
publisher_name: Maryland Transit Administration
service_category: API
slug: maryland-transit-administration-finops
source_filename: maryland-transit-administration-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Maryland Transit Administration\nproviderId: maryland-transit-administration\npublisherName: Maryland Transit Administration\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Government\n  - GTFS\n  - GTFS-RT\n  - Public Transportation\n  - Transit\n  - Bus\n  - Rail\n  - Subway\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Maryland Transit Administration API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Maryland Transit Administration\n  ServiceCategory: Developer Tools / API\n  ProviderName: Maryland Transit Administration\n  PublisherName: Maryland Transit Administration\n  InvoiceIssuerName: Maryland Transit Administration\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: MDOT MTA Local Bus GTFS\n    baseURL: https://feeds.mta.maryland.gov/gtfs/local-bus\n    tags:\n      - GTFS\n      - Bus\n      - Public Transportation\n    serviceName: MDOT MTA Local Bus GTFS\n    serviceCategory: API\n  - name: MDOT MTA Light Rail GTFS\n    baseURL: https://feeds.mta.maryland.gov/gtfs/light-rail\n    tags:\n      - GTFS\n      - Light Rail\n      - Public Transportation\n    serviceName: MDOT MTA Light Rail GTFS\n    serviceCategory: API\n  - name: MDOT MTA Metro Subway GTFS\n \
  \   baseURL: https://feeds.mta.maryland.gov/gtfs/metro\n    tags:\n      - GTFS\n      - Subway\n      - Public Transportation\n    serviceName: MDOT MTA Metro Subway GTFS\n    serviceCategory: API\n  - name: MDOT MTA MARC Train GTFS\n    baseURL: https://feeds.mta.maryland.gov/gtfs/marc\n    tags:\n      - GTFS\n      - Rail\n      - Public Transportation\n    serviceName: MDOT MTA MARC Train GTFS\n    serviceCategory: API\n  - name: MDOT MTA Commuter Bus GTFS\n    baseURL: https://feeds.mta.maryland.gov/gtfs/commuter-bus\n    tags:\n      - GTFS\n      - Bus\n      - Public Transportation\n    serviceName: MDOT MTA Commuter Bus GTFS\n    serviceCategory: API\n  - name: MDOT MTA Service Alerts\n    baseURL: https://feeds.mta.maryland.gov/alerts.pb\n    tags:\n      - GTFS-RT\n      - Alerts\n      - Public Transportation\n    serviceName: MDOT MTA Service Alerts\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n\
  \    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/maryland-transit-administration/refs/heads/main/finops/maryland-transit-administration-finops.yml
sources: []
specification: FinOps Framework
tags:
- Government
- GTFS
- GTFS-RT
- Public Transportation
- Transit
- Bus
- Rail
- Subway
- FinOps
- Cost Management
- FOCUS
---
