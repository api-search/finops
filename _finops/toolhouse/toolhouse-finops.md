---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: toolhouse-openapi-original.yml
  format: yaml
  label: Toolhouse Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toolhouse/refs/heads/main/openapi/toolhouse-openapi-original.yml
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
description: FinOps framework definition for the Toolhouse API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs. Toolhouse meters consumption in "credits" (one credit per agent run) rather than per-request, so the primary billable meter below is agent_run_credits.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Toolhouse
  PricingCategory: Subscription with Included Quota
  PricingUnit: credit
  ProviderName: Toolhouse
  PublisherName: Toolhouse
  ServiceCategory: Developer Tools / API
  ServiceName: Toolhouse
layout: finops
meters:
- aggregation: sum
  description: Primary Toolhouse billable meter. One credit corresponds to one agent run on the Toolhouse runtime. Monthly credit allowance is set by the subscribed plan (Basic 15, Pro 100, Business 15000).
  dimensions:
  - api
  - agent
  - tier
  - region
  - consumer
  name: agent_run_credits
  unit: credit
- aggregation: sum
  description: Count of HTTP API requests (operational telemetry; not directly billed per request).
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses (operational telemetry).
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by an agent run on the Virtual Computer sandbox or other Toolhouse runtime (operational telemetry).
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Toolhouse Finops
provider_name: Toolhouse
provider_slug: toolhouse
publisher_name: Toolhouse
service_category: API
slug: toolhouse-finops
source_filename: toolhouse-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Toolhouse\nproviderId: toolhouse\npublisherName: Toolhouse\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-15'\nreconciled: true\nreconciledOn: '2026-05-15'\nreconciledAgainst: https://toolhouse.ai/pricing\ntags:\n  - Agent Infrastructure\n  - AI Agents\n  - AI Workers\n  - Backend as a Service\n  - MCP\n  - Tools\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Toolhouse API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs. Toolhouse\n  meters consumption in \"credits\" (one credit per agent run) rather than per-request, so the primary\n\
  \  billable meter below is agent_run_credits.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n\
  \  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Toolhouse\n  ServiceCategory: Developer Tools / API\n  ProviderName: Toolhouse\n  PublisherName: Toolhouse\n  InvoiceIssuerName: Toolhouse\n  PricingCategory: Subscription with Included Quota\n  PricingUnit: credit\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: agent_run_credits\n    description:\
  \ Primary Toolhouse billable meter. One credit corresponds to one agent run on the Toolhouse\n      runtime. Monthly credit allowance is set by the subscribed plan (Basic 15, Pro 100, Business 15000).\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api\n      - agent\n      - tier\n      - region\n      - consumer\n  - name: api_requests\n    description: Count of HTTP API requests (operational telemetry; not directly billed per request).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses (operational telemetry).\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by an agent run on the Virtual Computer sandbox or other\n      Toolhouse runtime (operational telemetry).\n    unit:\
  \ second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Toolhouse Platform API\n    baseURL: ''\n    tags:\n      - Agent Runs\n      - AI Agents\n      - API Keys\n      - Billing\n      - Bundles\n      - Management\n      - Schedules\n      - Tools\n    serviceName: Toolhouse Platform API\n    serviceCategory: API\n  - name: Toolhouse Agents API\n    baseURL: ''\n    tags:\n      - AI Agents\n      - Conversations\n      - Execution\n      - Streaming\n    serviceName: Toolhouse Agents API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Agent Run (Credit)\n    metric: billed_cost / agent_run_credits\n    target: '0.10 (Pro), 0.0333 (Business)'\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\n  - name: Credit Utilization\n    metric: agent_run_credits_consumed / agent_run_credits_allocated\n\
  \    target: '> 0.50'\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/toolhouse/refs/heads/main/finops/toolhouse-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agent Infrastructure
- AI Agents
- AI Workers
- Backend as a Service
- MCP
- Tools
- FinOps
- Cost Management
- FOCUS
---
