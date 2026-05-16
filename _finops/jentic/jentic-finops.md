---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jentic-openapi.yml
  format: yaml
  label: Jentic API
  slug: jentic-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jentic/refs/heads/main/openapi/jentic-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Subscription
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription Plus Usage
description: FinOps framework definition for the Jentic agentic knowledge layer. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit economics across the search / load / execute surface, the Remote MCP server, and the Agentic Sandbox.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Jentic
  PricingCategory: Subscription Plus Usage
  PricingUnit: execution
  ProviderName: Jentic
  PublisherName: Jentic
  ServiceCategory: AI Agent Platform
  ServiceName: Jentic
layout: finops
meters:
- aggregation: sum
  description: Count of /agents/execute calls where execution_type = workflow (Arazzo workflows).
  dimensions:
  - agent
  - workflow_uuid
  - api_name
  - status
  - tier
  name: workflow_executions
  unit: execution
- aggregation: sum
  description: Count of /agents/execute calls where execution_type = operation (single OpenAPI operation).
  dimensions:
  - agent
  - operation_uuid
  - api_name
  - status
  - tier
  name: operation_executions
  unit: execution
- aggregation: count_distinct
  description: Distinct upstream APIs (api_name) actually invoked by an agent during the billing period. Counts breadth, not depth.
  dimensions:
  - agent
  - org
  - tier
  name: integrations_used
  unit: api
- aggregation: sum
  description: One end-to-end search → load → execute session, correlated by execution_id chain.
  dimensions:
  - agent
  - tier
  name: agent_runs
  unit: run
- aggregation: max
  description: Active human operators on the Jentic console.
  dimensions:
  - org
  - role
  - tier
  name: seats
  unit: user
- aggregation: sum
  description: Tool invocations against the Remote MCP server at api.jentic.com/mcp (search_apis, load_execution_info, execute).
  dimensions:
  - agent
  - tool
  - client
  - tier
  name: mcp_calls
  unit: call
- aggregation: sum
  description: Count of /agents/search calls.
  dimensions:
  - agent
  - tier
  name: search_queries
  unit: query
- aggregation: sum
  description: Count of /agents/load calls.
  dimensions:
  - agent
  - tier
  name: load_calls
  unit: call
- aggregation: sum
  description: Bytes returned over the network in /agents/execute responses.
  dimensions:
  - agent
  - api_name
  name: data_egress
  unit: GB
name: Jentic Finops
provider_name: Jentic
provider_slug: jentic
publisher_name: Jentic
service_category: AI Agent Platform
slug: jentic-finops
source_filename: jentic-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Jentic\nproviderId: jentic\npublisherName: Jentic\nserviceCategory: AI Agent Platform\ncreated: '2026-05-04'\nmodified: '2026-05-15'\nreconciled: false\nnotes: >-\n  Jentic's Enterprise Edition pricing is gated (contact sales), and the\n  Core Edition is free, so a published unit-rate card is not available.\n  Meters and unit economics below are aligned to the obvious chargeable\n  signals on the platform (workflow executions, integrations used, agent\n  runs, seats, MCP calls). Reconcile against a real Jentic order form\n  before treating rates as authoritative.\ntags:\n  - AI Agents\n  - Arazzo\n  - OpenAPI\n  - MCP\n  - Workflows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription:\
  \ >-\n  FinOps framework definition for the Jentic agentic knowledge layer.\n  Provides a FOCUS-aligned mapping for cost allocation, usage\n  measurement, and unit economics across the search / load / execute\n  surface, the Remote MCP server, and the Agentic Sandbox.\nprinciples:\n  - name: Visibility\n    description: >-\n      Make AI agent consumption costs (per agent, per workflow, per\n      upstream API) visible to engineering, product, and finance in\n      near real-time via execution_id telemetry.\n  - name: Allocation\n    description: >-\n      Every chargeable agent call is tagged with the agent UUID, scope,\n      upstream api_name, and execution_type (operation vs workflow) so\n      cost can be split across teams and features.\n  - name: Optimization\n    description: >-\n      Continuously evaluate which goals should be Arazzo workflows\n      (cheaper, deterministic) vs free-form tool calls (more LLM\n      tokens), and which APIs are pulling disproportionate cost.\n\
  \  - name: Accountability\n    description: >-\n      Establish per-agent budget owners and chargeback or showback\n      flows. Enterprise scopes can be aligned to business cost centers.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory:\
  \ Subscription Plus Usage\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Jentic\n  ServiceCategory: AI Agent Platform\n  ProviderName: Jentic\n  PublisherName: Jentic\n  InvoiceIssuerName: Jentic\n  PricingCategory: Subscription Plus Usage\n  PricingUnit: execution\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: workflow_executions\n    description: >-\n      Count of /agents/execute calls where execution_type = workflow\n      (Arazzo workflows).\n    unit: execution\n    aggregation: sum\n    dimensions:\n      - agent\n      - workflow_uuid\n      - api_name\n      - status\n      - tier\n  - name: operation_executions\n    description: >-\n      Count of /agents/execute calls where execution_type = operation\n      (single OpenAPI operation).\n    unit: execution\n    aggregation: sum\n\
  \    dimensions:\n      - agent\n      - operation_uuid\n      - api_name\n      - status\n      - tier\n  - name: integrations_used\n    description: >-\n      Distinct upstream APIs (api_name) actually invoked by an agent\n      during the billing period. Counts breadth, not depth.\n    unit: api\n    aggregation: count_distinct\n    dimensions:\n      - agent\n      - org\n      - tier\n  - name: agent_runs\n    description: >-\n      One end-to-end search → load → execute session, correlated by\n      execution_id chain.\n    unit: run\n    aggregation: sum\n    dimensions:\n      - agent\n      - tier\n  - name: seats\n    description: Active human operators on the Jentic console.\n    unit: user\n    aggregation: max\n    dimensions:\n      - org\n      - role\n      - tier\n  - name: mcp_calls\n    description: >-\n      Tool invocations against the Remote MCP server at\n      api.jentic.com/mcp (search_apis, load_execution_info, execute).\n    unit: call\n    aggregation: sum\n\
  \    dimensions:\n      - agent\n      - tool\n      - client\n      - tier\n  - name: search_queries\n    description: Count of /agents/search calls.\n    unit: query\n    aggregation: sum\n    dimensions:\n      - agent\n      - tier\n  - name: load_calls\n    description: Count of /agents/load calls.\n    unit: call\n    aggregation: sum\n    dimensions:\n      - agent\n      - tier\n  - name: data_egress\n    description: Bytes returned over the network in /agents/execute responses.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - agent\n      - api_name\napis:\n  - name: Jentic API\n    baseURL: https://api.jentic.com/api/v1\n    serviceName: Jentic API\n    serviceCategory: AI Agent Platform\n    tags:\n      - AI Agents\n      - Arazzo\n      - OpenAPI\n      - Workflows\n  - name: Jentic Remote MCP\n    baseURL: https://api.jentic.com/mcp\n    serviceName: Jentic Remote MCP\n    serviceCategory: MCP Server\n    tags:\n      - MCP\n      - AI Agents\nunitEconomics:\n\
  \  - name: Cost Per Workflow Execution\n    metric: billed_cost / workflow_executions\n    target: TBD\n  - name: Cost Per Agent Run\n    metric: billed_cost / agent_runs\n    target: TBD\n  - name: Cost Per Integration Used\n    metric: billed_cost / integrations_used\n    target: TBD\n  - name: Cost Per Seat\n    metric: billed_cost / seats\n    target: TBD\n  - name: Cost Per MCP Call\n    metric: billed_cost / mcp_calls\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jentic/refs/heads/main/finops/jentic-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI Agents
- Arazzo
- OpenAPI
- MCP
- Workflows
- FinOps
- Cost Management
- FOCUS
---
