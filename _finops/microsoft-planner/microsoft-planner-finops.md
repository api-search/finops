---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Planner API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Graph Plans API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Graph Tasks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
- filename: microsoft-planner-openapi.yml
  format: yaml
  label: Microsoft Graph Buckets API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/openapi/microsoft-planner-openapi.yml
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
description: FinOps framework definition for the Microsoft Planner API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Planner
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Planner
  PublisherName: Microsoft Planner
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Planner
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
name: Microsoft Planner Finops
provider_name: Microsoft Planner
provider_slug: microsoft-planner
publisher_name: Microsoft Planner
service_category: API
slug: microsoft-planner-finops
source_filename: microsoft-planner-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Planner\nproviderId: microsoft-planner\npublisherName: Microsoft Planner\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Collaboration\n  - Microsoft 365\n  - Productivity\n  - Project Management\n  - Task Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Planner API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Planner\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Planner\n  PublisherName: Microsoft Planner\n  InvoiceIssuerName: Microsoft Planner\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Microsoft Planner API\n    baseURL: https://graph.microsoft.com/v1.0/planner\n    tags:\n      - Assignments\n      - Buckets\n      - Microsoft Graph\n      - Plans\n      - Tasks\n    serviceName: Microsoft Planner API\n    serviceCategory: API\n  - name: Microsoft Graph Plans API\n    baseURL: https://graph.microsoft.com/v1.0/planner/plans\n    tags:\n      - Microsoft Graph\n      - Planner\n      - Plans\n    serviceName: Microsoft Graph Plans API\n    serviceCategory: API\n  - name: Microsoft Graph Tasks API\n    baseURL: https://graph.microsoft.com/v1.0/planner/tasks\n    tags:\n      - Assignments\n      -\
  \ Microsoft Graph\n      - Planner\n      - Tasks\n    serviceName: Microsoft Graph Tasks API\n    serviceCategory: API\n  - name: Microsoft Graph Buckets API\n    baseURL: https://graph.microsoft.com/v1.0/planner/buckets\n    tags:\n      - Buckets\n      - Microsoft Graph\n      - Organization\n      - Planner\n    serviceName: Microsoft Graph Buckets API\n    serviceCategory: API\n  - name: Microsoft Graph Planner API (Beta)\n    baseURL: https://graph.microsoft.com/beta/planner\n    tags:\n      - Beta\n      - Microsoft Graph\n      - Planner\n      - Preview\n      - Rosters\n    serviceName: Microsoft Graph Planner API (Beta)\n    serviceCategory: API\n  - name: Microsoft Graph Business Scenarios Planner API (Beta)\n    baseURL: https://graph.microsoft.com/beta/solutions/businessScenarios\n    tags:\n      - Beta\n      - Business Scenarios\n      - Integration\n      - Microsoft Graph\n      - Planner\n    serviceName: Microsoft Graph Business Scenarios Planner API (Beta)\n   \
  \ serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-planner/refs/heads/main/finops/microsoft-planner-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Microsoft 365
- Productivity
- Project Management
- Task Management
- FinOps
- Cost Management
- FOCUS
---
