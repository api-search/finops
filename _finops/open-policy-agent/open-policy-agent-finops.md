---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: policy-api.yml
  format: yaml
  label: Open Policy Agent Policy API
  slug: open-policy-agent-policy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/policy-api.yml
- filename: data-api.yml
  format: yaml
  label: Open Policy Agent Data API
  slug: open-policy-agent-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/data-api.yml
- filename: query-api.yml
  format: yaml
  label: Open Policy Agent Query API
  slug: open-policy-agent-query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/query-api.yml
- filename: compile-api.yml
  format: yaml
  label: Open Policy Agent Compile API
  slug: open-policy-agent-compile-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/compile-api.yml
- filename: health-api.yml
  format: yaml
  label: Open Policy Agent Health API
  slug: open-policy-agent-health-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/health-api.yml
- filename: config-api.yml
  format: yaml
  label: Open Policy Agent Config API
  slug: open-policy-agent-config-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/config-api.yml
- filename: status-api.yml
  format: yaml
  label: Open Policy Agent Status API
  slug: open-policy-agent-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/openapi/status-api.yml
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
description: FinOps framework definition for the Open Policy Agent API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Open Policy Agent
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Open Policy Agent
  PublisherName: Open Policy Agent
  ServiceCategory: Developer Tools / API
  ServiceName: Open Policy Agent
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
name: Open Policy Agent Finops
provider_name: Open Policy Agent
provider_slug: open-policy-agent
publisher_name: Open Policy Agent
service_category: API
slug: open-policy-agent-finops
source_filename: open-policy-agent-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Open Policy Agent\nproviderId: open-policy-agent\npublisherName: Open Policy Agent\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Policies\n  - Standards\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Open Policy Agent API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team,\
  \ environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n\
  \      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Open Policy Agent\n  ServiceCategory: Developer Tools / API\n  ProviderName: Open Policy Agent\n  PublisherName: Open Policy Agent\n  InvoiceIssuerName: Open Policy Agent\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Open Policy Agent Policy API\n    baseURL: ''\n    tags:\n      - Management\n      - Policies\n      - Rego\n    serviceName: Open Policy Agent Policy API\n    serviceCategory: API\n  - name: Open Policy Agent Data API\n    baseURL: ''\n    tags:\n      - Data\n      - Documents\n      - Storage\n    serviceName: Open Policy Agent Data API\n    serviceCategory: API\n  - name: Open Policy Agent Query API\n    baseURL: ''\n    tags:\n      - Evaluation\n      - Queries\n      - Rego\n    serviceName: Open Policy Agent Query API\n    serviceCategory: API\n  - name: Open Policy Agent Compile API\n    baseURL: ''\n    tags:\n      - Compile\n      - Evaluation\n      - Partial Evaluation\n    serviceName:\
  \ Open Policy Agent Compile API\n    serviceCategory: API\n  - name: Open Policy Agent Health API\n    baseURL: ''\n    tags:\n      - Availability\n      - Health\n      - Monitoring\n    serviceName: Open Policy Agent Health API\n    serviceCategory: API\n  - name: Open Policy Agent Config API\n    baseURL: ''\n    tags:\n      - Configurations\n      - Discovery\n      - Management\n    serviceName: Open Policy Agent Config API\n    serviceCategory: API\n  - name: Open Policy Agent Status API\n    baseURL: ''\n    tags:\n      - Monitoring\n      - Observability\n      - Status\n    serviceName: Open Policy Agent Status API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/open-policy-agent/refs/heads/main/finops/open-policy-agent-finops.yml
sources: []
specification: FinOps Framework
tags:
- Policies
- Standards
- FinOps
- Cost Management
- FOCUS
---
