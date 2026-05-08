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
description: FinOps framework definition for the AAR Corp API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AAR Corp
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AAR Corp
  PublisherName: AAR Corp
  ServiceCategory: Developer Tools / API
  ServiceName: AAR Corp
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
name: Aar Finops
provider_name: AAR Corp
provider_slug: aar
publisher_name: AAR Corp
service_category: API
slug: aar-finops
source_filename: aar-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AAR Corp\nproviderId: aar\npublisherName: AAR Corp\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Aviation\n  - MRO\n  - Aerospace\n  - Defense\n  - Parts Supply\n  - Maintenance\n  - Government\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AAR Corp API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AAR Corp\n  ServiceCategory: Developer Tools / API\n  ProviderName: AAR Corp\n  PublisherName: AAR Corp\n  InvoiceIssuerName: AAR Corp\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AAR Parts Supply\n    baseURL: ''\n    tags:\n      - Aviation\n      - Parts Supply\n      - Aircraft Parts\n      - Aerospace\n    serviceName: AAR Parts Supply\n    serviceCategory: API\n  - name: AAR Airframe MRO\n    baseURL: ''\n    tags:\n      - Aviation\n      - MRO\n      - Maintenance\n      - Repair\n      - Overhaul\n    serviceName: AAR Airframe MRO\n    serviceCategory: API\n  - name: AAR Component MRO\n    baseURL: ''\n    tags:\n      - Aviation\n      - MRO\n      - Components\n      - Repair\n    serviceName: AAR Component MRO\n    serviceCategory: API\n  - name: AAR Trax Aviation Software\n    baseURL: ''\n    tags:\n      - Aviation\n      - Software\n      - MRO Software\n\
  \      - Fleet Management\n      - Maintenance Tracking\n    serviceName: AAR Trax Aviation Software\n    serviceCategory: API\n  - name: AAR Aerostrat\n    baseURL: ''\n    tags:\n      - Aviation\n      - Software\n      - Supply Chain\n      - Parts Management\n    serviceName: AAR Aerostrat\n    serviceCategory: API\n  - name: AAR Airinmar Warranty and Claims\n    baseURL: ''\n    tags:\n      - Aviation\n      - Software\n      - Warranty Management\n      - Claims Processing\n    serviceName: AAR Airinmar Warranty and Claims\n    serviceCategory: API\n  - name: AAR Government Services\n    baseURL: ''\n    tags:\n      - Aviation\n      - Government\n      - Defense\n      - Expeditionary\n    serviceName: AAR Government Services\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n \
  \ - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aar/refs/heads/main/finops/aar-finops.yml
sources: []
specification: FinOps Framework
tags:
- Aviation
- MRO
- Aerospace
- Defense
- Parts Supply
- Maintenance
- Government
- FinOps
- Cost Management
- FOCUS
---
