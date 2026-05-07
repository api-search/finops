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
description: FinOps framework definition for the Bloomberg Television and Radio API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bloomberg Television and Radio
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bloomberg Television and Radio
  PublisherName: Bloomberg Television and Radio
  ServiceCategory: Developer Tools / API
  ServiceName: Bloomberg Television and Radio
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
name: Bloomberg Television And Radio Finops
provider_name: Bloomberg Television and Radio
provider_slug: bloomberg-television-and-radio
publisher_name: Bloomberg Television and Radio
service_category: API
slug: bloomberg-television-and-radio-finops
source_filename: bloomberg-television-and-radio-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bloomberg Television and Radio\nproviderId: bloomberg-television-and-radio\npublisherName: Bloomberg Television and Radio\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Television\n  - Radio\n  - Financial News\n  - Media\n  - Streaming\n  - Bloomberg TV\n  - Bloomberg Radio\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bloomberg Television and Radio API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bloomberg Television and Radio\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bloomberg Television and Radio\n  PublisherName: Bloomberg Television and Radio\n  InvoiceIssuerName: Bloomberg Television and Radio\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bloomberg Media Content API\n    baseURL: https://api.bloomberg.com/media\n    tags:\n      - TV Content\n      - Radio Content\n      - Video\n      - Audio\n      - Media Licensing\n    serviceName: Bloomberg Media Content API\n    serviceCategory: API\n  - name: Bloomberg Live Streaming API\n    baseURL: https://stream.bloomberg.com\n    tags:\n      - Live Stream\n      - Video\n      - Streaming\n      - Digital Distribution\n    serviceName: Bloomberg Live Streaming API\n    serviceCategory: API\n\
  unitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-television-and-radio/refs/heads/main/finops/bloomberg-television-and-radio-finops.yml
sources: []
specification: FinOps Framework
tags:
- Television
- Radio
- Financial News
- Media
- Streaming
- Bloomberg TV
- Bloomberg Radio
- FinOps
- Cost Management
- FOCUS
---
