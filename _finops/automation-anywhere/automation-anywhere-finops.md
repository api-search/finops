---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: automation-anywhere-control-room-openapi.yml
  format: yaml
  label: Automation Anywhere Control Room API
  slug: control-room-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-control-room-openapi.yml
- filename: automation-anywhere-bot-deploy-openapi.yml
  format: yaml
  label: Automation Anywhere Bot Deploy API
  slug: bot-deploy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-bot-deploy-openapi.yml
- filename: automation-anywhere-workload-management-openapi.yml
  format: yaml
  label: Automation Anywhere Workload Management API
  slug: workload-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-workload-management-openapi.yml
- filename: automation-anywhere-bot-insight-openapi.yml
  format: yaml
  label: Automation Anywhere Bot Insight API
  slug: bot-insight-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-bot-insight-openapi.yml
- filename: automation-anywhere-api-task-execution-openapi.yml
  format: yaml
  label: Automation Anywhere API Task Execution API
  slug: api-task-execution-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-api-task-execution-openapi.yml
- filename: automation-anywhere-credential-vault-openapi.yml
  format: yaml
  label: Automation Anywhere Credential Vault API
  slug: credential-vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-credential-vault-openapi.yml
- filename: automation-anywhere-repository-management-openapi.yml
  format: yaml
  label: Automation Anywhere Repository Management API
  slug: repository-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-repository-management-openapi.yml
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
description: FinOps framework definition for the automation-anywhere API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: automation-anywhere
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: automation-anywhere
  PublisherName: automation-anywhere
  ServiceCategory: Developer Tools / API
  ServiceName: automation-anywhere
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
name: Automation Anywhere Finops
provider_name: automation-anywhere
provider_slug: automation-anywhere
publisher_name: automation-anywhere
service_category: API
slug: automation-anywhere-finops
source_filename: automation-anywhere-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: automation-anywhere\nproviderId: automation-anywhere\npublisherName: automation-anywhere\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the automation-anywhere API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application,\
  \ and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education\
  \ and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: automation-anywhere\n  ServiceCategory: Developer Tools / API\n  ProviderName: automation-anywhere\n  PublisherName: automation-anywhere\n  InvoiceIssuerName: automation-anywhere\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Automation Anywhere Control Room API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n    tags:\n      - Automation\n      - Bot Management\n      - Enterprise\n      - REST\n      - RPA\n    serviceName: Automation Anywhere Control Room API\n    serviceCategory: API\n  - name: Automation Anywhere Bot Deploy API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n    tags:\n      - Automation\n      - Bot Deployment\n      - Enterprise\n      - Orchestration\n      - RPA\n    serviceName: Automation Anywhere Bot Deploy API\n    serviceCategory: API\n  - name: Automation Anywhere Workload Management API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n\
  \    tags:\n      - Automation\n      - Queues\n      - RPA\n      - Work Items\n      - Workload Management\n    serviceName: Automation Anywhere Workload Management API\n    serviceCategory: API\n  - name: Automation Anywhere Bot Insight API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n    tags:\n      - Analytics\n      - Bot Monitoring\n      - Business Intelligence\n      - Reporting\n      - RPA\n    serviceName: Automation Anywhere Bot Insight API\n    serviceCategory: API\n  - name: Automation Anywhere API Task Execution API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n    tags:\n      - API Task\n      - Automation\n      - Bot Execution\n      - Integration\n      - RPA\n    serviceName: Automation Anywhere API Task Execution API\n    serviceCategory: API\n  - name: Automation Anywhere Credential Vault API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n    tags:\n      - Credentials\n      - Enterprise\n\
  \      - RPA\n      - Secrets Management\n      - Security\n    serviceName: Automation Anywhere Credential Vault API\n    serviceCategory: API\n  - name: Automation Anywhere Package SDK\n    baseURL: https://api.example.com\n    tags:\n      - Bot Development\n      - Custom Packages\n      - Extensions\n      - Java\n      - SDK\n    serviceName: Automation Anywhere Package SDK\n    serviceCategory: API\n  - name: Automation Anywhere Repository Management API\n    baseURL: https://automationanywhere-be-prod.automationanywhere.com\n    tags:\n      - Bot Lifecycle\n      - DevOps\n      - File Management\n      - Repository\n      - RPA\n    serviceName: Automation Anywhere Repository Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/finops/automation-anywhere-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
