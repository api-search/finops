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
description: FinOps framework definition for the Defense Technical Information Center API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Defense Technical Information Center
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Defense Technical Information Center
  PublisherName: Defense Technical Information Center
  ServiceCategory: Developer Tools / API
  ServiceName: Defense Technical Information Center
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
name: Defense Technical Information Center Finops
provider_name: Defense Technical Information Center
provider_slug: defense-technical-information-center
publisher_name: Defense Technical Information Center
service_category: API
slug: defense-technical-information-center-finops
source_filename: defense-technical-information-center-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Defense Technical Information Center\nproviderId: defense-technical-information-center\npublisherName: Defense Technical Information Center\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Defense\n  - Department of Defense\n  - DTIC\n  - Federal Government\n  - Knowledge Management\n  - Library\n  - Research\n  - Scientific and Technical Information\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Defense Technical Information Center API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n\
  \    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting\
  \ for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Defense Technical Information Center\n  ServiceCategory: Developer Tools / API\n  ProviderName: Defense Technical Information Center\n  PublisherName: Defense Technical Information Center\n  InvoiceIssuerName: Defense Technical Information Center\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n\
  \    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: DTIC Website\n    baseURL: ''\n    tags:\n      - Federal Government\n      - Website\n    serviceName: DTIC Website\n    serviceCategory: API\n  - name: DTIC Discover\n    baseURL: ''\n    tags:\n      - Discovery\n      - Search\n      - Technical Reports\n    serviceName: DTIC Discover\n    serviceCategory: API\n  - name: DTIC Research and Engineering (R&E) Gateway\n    baseURL: ''\n    tags:\n\
  \      - Engineering\n      - R&E\n      - Research\n    serviceName: DTIC Research and Engineering (R&E) Gateway\n    serviceCategory: API\n  - name: DoDTechSpace\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Communities of Practice\n    serviceName: DoDTechSpace\n    serviceCategory: API\n  - name: DTIC FOIA Reading Room\n    baseURL: ''\n    tags:\n      - FOIA\n      - Open Records\n      - Transparency\n    serviceName: DTIC FOIA Reading Room\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/defense-technical-information-center/refs/heads/main/finops/defense-technical-information-center-finops.yml
sources: []
specification: FinOps Framework
tags:
- Defense
- Department of Defense
- DTIC
- Federal Government
- Knowledge Management
- Library
- Research
- Scientific and Technical Information
- FinOps
- Cost Management
- FOCUS
---
