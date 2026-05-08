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
description: FinOps framework definition for the TLA Plus Foundation API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: TLA Plus Foundation
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: TLA Plus Foundation
  PublisherName: TLA Plus Foundation
  ServiceCategory: Developer Tools / API
  ServiceName: TLA Plus Foundation
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
name: Tla Plus Foundation Finops
provider_name: TLA Plus Foundation
provider_slug: tla-plus-foundation
publisher_name: TLA Plus Foundation
service_category: API
slug: tla-plus-foundation-finops
source_filename: tla-plus-foundation-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TLA Plus Foundation\nproviderId: tla-plus-foundation\npublisherName: TLA Plus Foundation\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Formal Methods\n  - Linux Foundation\n  - Specifications\n  - Verification\n  - Distributed Systems\n  - Concurrency\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the TLA Plus Foundation API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: TLA Plus Foundation\n  ServiceCategory: Developer Tools / API\n  ProviderName: TLA Plus Foundation\n  PublisherName: TLA Plus Foundation\n  InvoiceIssuerName: TLA Plus Foundation\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  -\
  \ name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: TLC Model Checker\n    baseURL: ''\n    tags:\n      - Model Checking\n      - Formal Verification\n      - Java\n    serviceName: TLC Model Checker\n    serviceCategory: API\n  - name: TLAPS Proof System\n    baseURL: ''\n    tags:\n      - Proof System\n      - Formal Verification\n      - Mathematics\n    serviceName: TLAPS Proof System\n    serviceCategory: API\n  - name: TLA+ Toolbox IDE\n    baseURL: ''\n    tags:\n      - IDE\n      - Tooling\n      - Development\n    serviceName: TLA+ Toolbox IDE\n    serviceCategory: API\n  - name: TLA+ VS Code Extension\n    baseURL: ''\n\
  \    tags:\n      - IDE\n      - VS Code\n      - Tooling\n    serviceName: TLA+ VS Code Extension\n    serviceCategory: API\n  - name: TLA+ Community Modules\n    baseURL: ''\n    tags:\n      - Community\n      - Modules\n      - Specifications\n    serviceName: TLA+ Community Modules\n    serviceCategory: API\n  - name: TLA+ Specification Examples\n    baseURL: ''\n    tags:\n      - Examples\n      - Specifications\n      - Learning\n    serviceName: TLA+ Specification Examples\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tla-plus-foundation/refs/heads/main/finops/tla-plus-foundation-finops.yml
sources: []
specification: FinOps Framework
tags:
- Formal Methods
- Linux Foundation
- Specifications
- Verification
- Distributed Systems
- Concurrency
- FinOps
- Cost Management
- FOCUS
---
