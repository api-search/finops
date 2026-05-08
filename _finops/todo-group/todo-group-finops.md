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
description: FinOps framework definition for the TODO Group API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: TODO Group
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: TODO Group
  PublisherName: TODO Group
  ServiceCategory: Developer Tools / API
  ServiceName: TODO Group
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
name: Todo Group Finops
provider_name: TODO Group
provider_slug: todo-group
publisher_name: TODO Group
service_category: API
slug: todo-group-finops
source_filename: todo-group-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: TODO Group\nproviderId: todo-group\npublisherName: TODO Group\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Community\n  - Linux Foundation\n  - Open Source\n  - OSPO\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the TODO Group API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: TODO Group\n  ServiceCategory: Developer Tools / API\n  ProviderName: TODO Group\n  PublisherName: TODO Group\n  InvoiceIssuerName: TODO Group\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Repolinter\n    baseURL: ''\n    tags:\n      - Linting\n      - Open Source\n      - Repository\n      - Compliance\n    serviceName: Repolinter\n    serviceCategory: API\n  - name: Repolinter Action\n    baseURL: ''\n    tags:\n      - GitHub Actions\n      - Linting\n      - CI/CD\n      - Compliance\n    serviceName: Repolinter Action\n    serviceCategory: API\n  - name: OSPO Landscape\n    baseURL: ''\n    tags:\n      - Landscape\n      - OSPO\n      - Ecosystem\n      - Data\n    serviceName: OSPO Landscape\n    serviceCategory: API\n  - name: OSPO Guides\n    baseURL: ''\n    tags:\n      - Guides\n      - OSPO\n      - Best Practices\n      - Documentation\n    serviceName: OSPO Guides\n   \
  \ serviceCategory: API\n  - name: OSPOlogy\n    baseURL: ''\n    tags:\n      - Community\n      - Webinars\n      - OSPO\n      - Education\n    serviceName: OSPOlogy\n    serviceCategory: API\n  - name: OSPO Career Path\n    baseURL: ''\n    tags:\n      - Career Development\n      - OSPO\n      - Human Resources\n      - Skills Framework\n    serviceName: OSPO Career Path\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/todo-group/refs/heads/main/finops/todo-group-finops.yml
sources: []
specification: FinOps Framework
tags:
- Community
- Linux Foundation
- Open Source
- OSPO
- FinOps
- Cost Management
- FOCUS
---
