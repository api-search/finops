---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: acronis-account-management-openapi.yaml
  format: yaml
  label: Acronis Account Management API
  slug: account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/openapi/acronis-account-management-openapi.yaml
- filename: acronis-agent-management-openapi.yaml
  format: yaml
  label: Acronis Agent Management REST API
  slug: agent-management-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/openapi/acronis-agent-management-openapi.yaml
- filename: acronis-task-manager-openapi.yaml
  format: yaml
  label: Acronis Task Manager API
  slug: task-manager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/openapi/acronis-task-manager-openapi.yaml
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
description: FinOps framework definition for the Acronis API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Acronis
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Acronis
  PublisherName: Acronis
  ServiceCategory: Developer Tools / API
  ServiceName: Acronis
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
name: Acronis Finops
provider_name: Acronis
provider_slug: acronis
publisher_name: Acronis
service_category: API
slug: acronis-finops
source_filename: acronis-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Acronis\nproviderId: acronis\npublisherName: Acronis\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cybersecurity\n  - Data Protection\n  - Endpoint Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Acronis API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Acronis\n  ServiceCategory: Developer Tools / API\n  ProviderName: Acronis\n  PublisherName: Acronis\n  InvoiceIssuerName: Acronis\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n \
  \     - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Acronis Account Management API\n    baseURL: ''\n    tags:\n      - Account Management\n      - Acronis\n      - Tenants\n      - Users\n    serviceName: Acronis Account Management API\n    serviceCategory: API\n  - name: Acronis Agent Management REST API\n    baseURL: ''\n    tags:\n      - Acronis\n      - Agent Management\n      - Backup\n      - Endpoints\n    serviceName: Acronis Agent Management REST API\n    serviceCategory: API\n  - name: Acronis Resource and Policy Management API\n    baseURL: ''\n    tags:\n      - Acronis\n      - Policy Management\n      - Resources\n    serviceName: Acronis Resource and Policy Management API\n    serviceCategory: API\n  - name: Acronis Task Manager API\n    baseURL: ''\n    tags:\n  \
  \    - Acronis\n      - Backup\n      - Monitoring\n      - Tasks\n    serviceName: Acronis Task Manager API\n    serviceCategory: API\n  - name: Acronis Advanced Automation API\n    baseURL: ''\n    tags:\n      - Acronis\n      - Advanced Automation\n      - PSA\n    serviceName: Acronis Advanced Automation API\n    serviceCategory: API\n  - name: Acronis Event Manager API\n    baseURL: ''\n    tags:\n      - Acronis\n      - Events\n      - Monitoring\n    serviceName: Acronis Event Manager API\n    serviceCategory: API\n  - name: Acronis Disaster Recovery Service API\n    baseURL: ''\n    tags:\n      - Acronis\n      - Disaster Recovery\n    serviceName: Acronis Disaster Recovery Service API\n    serviceCategory: API\n  - name: Acronis Endpoint Detection and Response API\n    baseURL: ''\n    tags:\n      - Acronis\n      - EDR\n      - Endpoint Security\n    serviceName: Acronis Endpoint Detection and Response API\n    serviceCategory: API\n  - name: Acronis Vault Manager REST API\n\
  \    baseURL: ''\n    tags:\n      - Acronis\n      - Storage\n      - Vault Management\n    serviceName: Acronis Vault Manager REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/acronis/refs/heads/main/finops/acronis-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cybersecurity
- Data Protection
- Endpoint Management
- FinOps
- Cost Management
- FOCUS
---
