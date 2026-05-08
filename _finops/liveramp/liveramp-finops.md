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
description: FinOps framework definition for the LiveRamp API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: LiveRamp
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: LiveRamp
  PublisherName: LiveRamp
  ServiceCategory: Developer Tools / API
  ServiceName: LiveRamp
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
name: Liveramp Finops
provider_name: LiveRamp
provider_slug: liveramp
publisher_name: LiveRamp
service_category: API
slug: liveramp-finops
source_filename: liveramp-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: LiveRamp\nproviderId: liveramp\npublisherName: LiveRamp\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Data Connectivity\n  - Identity Resolution\n  - Activation\n  - Clean Room\n  - Privacy\n  - AdTech\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the LiveRamp API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: LiveRamp\n  ServiceCategory: Developer Tools / API\n  ProviderName: LiveRamp\n  PublisherName: LiveRamp\n  InvoiceIssuerName: LiveRamp\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: LiveRamp Activation API\n    baseURL: ''\n    tags:\n      - Activation\n      - AdTech\n      - Marketing\n    serviceName: LiveRamp Activation API\n    serviceCategory: API\n  - name: LiveRamp Authenticated Traffic Solution (ATS) API\n    baseURL: ''\n    tags:\n      - Identity\n      - Privacy\n      - Authentication\n    serviceName: LiveRamp Authenticated Traffic Solution (ATS) API\n    serviceCategory: API\n  - name: LiveRamp Clean Room API\n    baseURL: ''\n    tags:\n      - Clean Room\n      - Data Collaboration\n      - Privacy\n    serviceName: LiveRamp Clean Room API\n    serviceCategory: API\n  - name: LiveRamp Data Marketplace Buyer API\n    baseURL: ''\n    tags:\n      - Data Marketplace\n\
  \      - Segments\n      - AdTech\n    serviceName: LiveRamp Data Marketplace Buyer API\n    serviceCategory: API\n  - name: LiveRamp AbiliTec API\n    baseURL: ''\n    tags:\n      - Identity\n      - Resolution\n      - PII\n    serviceName: LiveRamp AbiliTec API\n    serviceCategory: API\n  - name: LiveRamp RampID API\n    baseURL: ''\n    tags:\n      - Identity\n      - RampID\n      - Pseudonymous\n    serviceName: LiveRamp RampID API\n    serviceCategory: API\n  - name: LiveRamp Safe Haven Job Management API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Automation\n      - Jobs\n    serviceName: LiveRamp Safe Haven Job Management API\n    serviceCategory: API\n  - name: LiveRamp Privacy API\n    baseURL: ''\n    tags:\n      - Privacy\n      - Consent\n      - Compliance\n    serviceName: LiveRamp Privacy API\n    serviceCategory: API\n  - name: LiveRamp Sidecar\n    baseURL: ''\n    tags:\n      - SSP\n      - Programmatic\n      - Identity\n    serviceName: LiveRamp\
  \ Sidecar\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/liveramp/refs/heads/main/finops/liveramp-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Connectivity
- Identity Resolution
- Activation
- Clean Room
- Privacy
- AdTech
- FinOps
- Cost Management
- FOCUS
---
