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
description: FinOps framework definition for the Command Line Interface API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Command Line Interface
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Command Line Interface
  PublisherName: Command Line Interface
  ServiceCategory: Developer Tools / API
  ServiceName: Command Line Interface
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
name: Command Line Interface Finops
provider_name: Command Line Interface
provider_slug: command-line-interface
publisher_name: Command Line Interface
service_category: API
slug: command-line-interface-finops
source_filename: command-line-interface-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Command Line Interface\nproviderId: command-line-interface\npublisherName: Command Line Interface\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Automation\n  - CLI\n  - Command Line\n  - Developer Experience\n  - Developer Tools\n  - Scripting\n  - Shell\n  - Terminal\n  - Tooling\n  - UNIX\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Command Line Interface API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Command Line Interface\n  ServiceCategory: Developer Tools / API\n  ProviderName: Command Line Interface\n  PublisherName: Command Line Interface\n  InvoiceIssuerName: Command Line Interface\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Command Line Interface Guidelines\n    baseURL: https://clig.dev\n    tags:\n      - Best Practices\n      - CLI Design\n      - Developer Experience\n      - Guidelines\n      - Open Source\n    serviceName: Command Line Interface Guidelines\n    serviceCategory: API\n  - name: POSIX Utility Conventions\n    baseURL: https://pubs.opengroup.org\n    tags:\n      - Conventions\n      - POSIX\n      - Standards\n      - UNIX\n    serviceName: POSIX Utility Conventions\n    serviceCategory: API\n  - name: CLI Frameworks Landscape\n\
  \    baseURL: https://github.com\n    tags:\n      - Frameworks\n      - Libraries\n      - Open Source\n      - Tooling\n    serviceName: CLI Frameworks Landscape\n    serviceCategory: API\n  - name: Heroku CLI Style Guide\n    baseURL: https://devcenter.heroku.com\n    tags:\n      - Best Practices\n      - Developer Experience\n      - Heroku\n      - Style Guide\n    serviceName: Heroku CLI Style Guide\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/command-line-interface/refs/heads/main/finops/command-line-interface-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- CLI
- Command Line
- Developer Experience
- Developer Tools
- Scripting
- Shell
- Terminal
- Tooling
- UNIX
- FinOps
- Cost Management
- FOCUS
---
