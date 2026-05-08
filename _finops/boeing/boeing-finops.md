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
description: FinOps framework definition for the Boeing API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Boeing
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Boeing
  PublisherName: Boeing
  ServiceCategory: Developer Tools / API
  ServiceName: Boeing
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
name: Boeing Finops
provider_name: Boeing
provider_slug: boeing
publisher_name: Boeing
service_category: API
slug: boeing-finops
source_filename: boeing-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Boeing\nproviderId: boeing\npublisherName: Boeing\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Aviation\n  - Airplanes\n  - Aerospace\n  - Flight\n  - Aeronautical\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Boeing API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Boeing\n  ServiceCategory: Developer Tools / API\n  ProviderName: Boeing\n  PublisherName: Boeing\n  InvoiceIssuerName: Boeing\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Boeing Aircraft Models API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Aircraft\n      - Models\n      - Jeppesen\n    serviceName: Boeing Aircraft Models API\n    serviceCategory: API\n  - name: Boeing Airports and Aerodromes API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Airports\n      - Aerodromes\n      - Jeppesen\n    serviceName: Boeing Airports and Aerodromes API\n    serviceCategory: API\n  - name: Boeing Airspaces API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Airspace\n      - Flight Planning\n    serviceName: Boeing Airspaces API\n    serviceCategory: API\n  - name: Boeing Parts API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Parts\n      - MRO\n      - Maintenance\n    serviceName:\
  \ Boeing Parts API\n    serviceCategory: API\n  - name: Boeing Flight Events API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Flight\n      - Events\n      - Real-Time\n      - Tracking\n    serviceName: Boeing Flight Events API\n    serviceCategory: API\n  - name: Boeing NOTAMs API\n    baseURL: ''\n    tags:\n      - Aviation\n      - NOTAMs\n      - Safety\n      - Flight Planning\n      - Jeppesen\n    serviceName: Boeing NOTAMs API\n    serviceCategory: API\n  - name: Boeing Runway Monitor API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Runway\n      - Airports\n      - Operations\n    serviceName: Boeing Runway Monitor API\n    serviceCategory: API\n  - name: Boeing Standard Minimums API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Minimums\n      - Instrument\n      - Flight Planning\n    serviceName: Boeing Standard Minimums API\n    serviceCategory: API\n  - name: Boeing Taxi Time API\n    baseURL: ''\n    tags:\n      - Aviation\n      - Taxi\n\
  \      - Airports\n      - Operations\n      - Flight Planning\n    serviceName: Boeing Taxi Time API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/boeing/refs/heads/main/finops/boeing-finops.yml
sources: []
specification: FinOps Framework
tags:
- Aviation
- Airplanes
- Aerospace
- Flight
- Aeronautical
- FinOps
- Cost Management
- FOCUS
---
