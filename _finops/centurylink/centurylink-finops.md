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
description: FinOps framework definition for the CenturyLink (Lumen Technologies) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CenturyLink (Lumen Technologies)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CenturyLink (Lumen Technologies)
  PublisherName: CenturyLink (Lumen Technologies)
  ServiceCategory: Developer Tools / API
  ServiceName: CenturyLink (Lumen Technologies)
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
name: Centurylink Finops
provider_name: CenturyLink (Lumen Technologies)
provider_slug: centurylink
publisher_name: CenturyLink (Lumen Technologies)
service_category: API
slug: centurylink-finops
source_filename: centurylink-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CenturyLink (Lumen Technologies)\nproviderId: centurylink\npublisherName: CenturyLink (Lumen Technologies)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Broadband\n  - Connectivity\n  - Edge\n  - Fiber\n  - Lumen\n  - Network\n  - OAuth 2.0\n  - Quantum Fiber\n  - SD-WAN\n  - Telecom\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CenturyLink (Lumen Technologies) API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CenturyLink (Lumen Technologies)\n  ServiceCategory: Developer Tools / API\n  ProviderName: CenturyLink (Lumen Technologies)\n  PublisherName: CenturyLink (Lumen Technologies)\n  InvoiceIssuerName: CenturyLink (Lumen Technologies)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Lumen Developer Center APIs\n    baseURL: ''\n    tags:\n      - Enterprise\n      - Lumen\n      - OAuth 2.0\n      - Partner\n      - REST\n    serviceName: Lumen Developer Center APIs\n    serviceCategory: API\n  - name: Lumen API Marketplace\n    baseURL: ''\n    tags:\n      - API Marketplace\n      - Enterprise\n      - Partner\n    serviceName: Lumen API Marketplace\n    serviceCategory: API\n  - name: Lumen OpenAPI Services (Level 3 legacy)\n    baseURL: ''\n    tags:\n    \
  \  - Connectivity\n      - Level 3\n      - Location\n      - OpenAPI\n    serviceName: Lumen OpenAPI Services (Level 3 legacy)\n    serviceCategory: API\n  - name: Lumen Public Sector API Center\n    baseURL: ''\n    tags:\n      - Federal\n      - Government\n      - Public Sector\n      - State and Local\n    serviceName: Lumen Public Sector API Center\n    serviceCategory: API\n  - name: Quantum Fiber Residential Services\n    baseURL: ''\n    tags:\n      - Broadband\n      - Fiber\n      - Residential\n    serviceName: Quantum Fiber Residential Services\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/centurylink/refs/heads/main/finops/centurylink-finops.yml
sources: []
specification: FinOps Framework
tags:
- Broadband
- Connectivity
- Edge
- Fiber
- Lumen
- Network
- OAuth 2.0
- Quantum Fiber
- SD-WAN
- Telecom
- FinOps
- Cost Management
- FOCUS
---
