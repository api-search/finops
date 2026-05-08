---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stitch-openapi.yml
  format: yaml
  label: Stitch GraphQL API
  slug: stitch-graphql
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stitch/refs/heads/main/openapi/stitch-openapi.yml
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
description: FinOps framework definition for the Stitch API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Stitch
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Stitch
  PublisherName: Stitch
  ServiceCategory: Developer Tools / API
  ServiceName: Stitch
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
name: Stitch Finops
provider_name: Stitch
provider_slug: stitch
publisher_name: Stitch
service_category: API
slug: stitch-finops
source_filename: stitch-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Stitch\nproviderId: stitch\npublisherName: Stitch\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Africa\n  - Financial Data\n  - Open Banking\n  - Payments\n  - Unified API\n  - South Africa\n  - Nigeria\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Stitch API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Stitch\n  ServiceCategory: Developer Tools / API\n  ProviderName: Stitch\n  PublisherName: Stitch\n  InvoiceIssuerName: Stitch\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Stitch GraphQL API\n    baseURL: ''\n    tags:\n      - GraphQL\n      - Open Banking\n      - Payments\n    serviceName: Stitch GraphQL API\n    serviceCategory: API\n  - name: Stitch Pay By Bank\n    baseURL: ''\n    tags:\n      - Payments\n      - Bank Transfer\n      - Pay-ins\n    serviceName: Stitch Pay By Bank\n    serviceCategory: API\n  - name: Stitch Capitec Pay\n    baseURL: ''\n    tags:\n      - Payments\n      - Capitec\n      - South Africa\n    serviceName: Stitch Capitec Pay\n    serviceCategory: API\n  - name: Stitch Card Payments\n    baseURL: ''\n    tags:\n      - Payments\n      - Card Payments\n      - Pay-ins\n    serviceName: Stitch Card Payments\n    serviceCategory:\
  \ API\n  - name: Stitch DebiCheck\n    baseURL: ''\n    tags:\n      - Payments\n      - DebiCheck\n      - Recurring Payments\n      - South Africa\n    serviceName: Stitch DebiCheck\n    serviceCategory: API\n  - name: Stitch Manual EFT\n    baseURL: ''\n    tags:\n      - Payments\n      - EFT\n      - Bank Transfer\n    serviceName: Stitch Manual EFT\n    serviceCategory: API\n  - name: Stitch Disbursements\n    baseURL: ''\n    tags:\n      - Payouts\n      - Disbursements\n      - Bank Transfer\n    serviceName: Stitch Disbursements\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stitch/refs/heads/main/finops/stitch-finops.yml
sources: []
specification: FinOps Framework
tags:
- Africa
- Financial Data
- Open Banking
- Payments
- Unified API
- South Africa
- Nigeria
- FinOps
- Cost Management
- FOCUS
---
