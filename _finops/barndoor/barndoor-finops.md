---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: barndoor-openapi.yml
  format: yaml
  label: Barndoor Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/barndoor/refs/heads/main/openapi/barndoor-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (Annual Commit Available)
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Subscription (Plan-Based Seats + Feature Tiers)
description: 'FOCUS 1.3-aligned FinOps for Barndoor. Public pricing is seat-style (non- human identities) and feature-gated by plan tier, not consumption-metered. The pricing page shows $500/month Team, custom Pro and Enterprise, and free Trial. The likely commercial meters are: registered agents (seats), governed MCP server registrations, OAuth connection events, governance / policy decisions, and proxied MCP / SSE requests, but only the agent seat ceiling is published. Cost is currently fixed-per-plan; reconciled:false until a real customer contract confirms add-on or overage line items.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Barndoor AI, Inc.
  ProviderName: Barndoor
  PublisherName: Barndoor AI, Inc.
  ServiceCategory: AI Governance / Control Plane
  ServiceName: Barndoor Platform
layout: finops
meters:
- aggregation: sum
  description: Recurring monthly subscription per plan tier (Trial / Team / Pro / Enterprise). Team is published at $500/month billed annually; Pro and Enterprise are custom.
  dimensions:
  - organization_id
  - plan_tier
  name: plan_subscription
  unit: month
- aggregation: max
  description: 'Registered agents (non-human identities). The published structural quota: Trial unlimited, Team 250, Pro 1,000, Enterprise custom. Likely acts as a seat license rather than a per-call meter.'
  dimensions:
  - organization_id
  - agent_type
  name: non_human_identities
  unit: agent
- aggregation: max
  description: Registered MCP server instances under the organization. Not separately priced today; included in the plan.
  dimensions:
  - organization_id
  - server_type
  name: mcp_server_registrations
  unit: mcp_server
- aggregation: sum
  description: OAuth connections established from agents to backend SaaS through Barndoor's connection broker. Not separately priced today.
  dimensions:
  - organization_id
  - mcp_server_id
  - status
  name: oauth_connections
  unit: connection
- aggregation: sum
  description: Policy decisions emitted by the runtime enforcement engine (Cerbos PDP) against agent actions. Surfaced through audit logs and dashboards; not separately priced today.
  dimensions:
  - organization_id
  - policy_id
  - authorized
  name: governance_events
  unit: decision
- aggregation: sum
  description: Requests proxied through Barndoor's MCP / SSE endpoints (`/mcp/{server}`, `/sse/{server}`) to backend MCP servers. Not separately priced today.
  dimensions:
  - organization_id
  - mcp_server_id
  - agent_id
  name: mcp_proxy_requests
  unit: request
- aggregation: sum
  description: Audit events exported to S3-compatible storage. Batched every 30 seconds or per 100 events. Not separately priced today; included in Pro and Enterprise.
  dimensions:
  - organization_id
  - bucket
  name: audit_log_events_exported
  unit: event
- aggregation: max
  description: Private cloud / on-premises deployment add-on (Enterprise only). Custom-quoted.
  dimensions:
  - organization_id
  name: private_deployment
  unit: month
name: Barndoor Finops
provider_name: Barndoor
provider_slug: barndoor
publisher_name: Barndoor AI, Inc.
service_category: AI Governance / Control Plane
slug: barndoor-finops
source_filename: barndoor-finops.yml
source_heading: FinOps Profile
source_url: https://barndoor.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Barndoor\nproviderId: barndoor\ncreated: '2026-05-15'\nmodified: '2026-05-15'\nreconciled: false\ntags:\n  - AI Agents\n  - AI Governance\n  - MCP\n  - Control Plane\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS 1.3-aligned FinOps for Barndoor. Public pricing is seat-style (non-\n  human identities) and feature-gated by plan tier, not consumption-metered.\n  The pricing page shows $500/month Team, custom Pro and Enterprise, and free\n  Trial. The likely commercial meters are: registered agents (seats),\n  governed MCP server registrations, OAuth connection events, governance /\n  policy decisions, and proxied MCP / SSE requests, but only the agent seat\n  ceiling is published. Cost is currently fixed-per-plan; reconciled:false\n  until a real customer contract confirms add-on or overage line items.\nsources:\n  - https://barndoor.ai/pricing\n  - https://docs.barndoor.ai/api-reference/introduction\n\
  \  - https://docs.barndoor.ai/how-tos/log-export\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Barndoor AI, Inc.\nserviceCategory: AI Governance / Control Plane\nbillingModel:\n  pricingCategory: Subscription (Plan-Based Seats + Feature Tiers)\n  billingFrequency: Monthly (Annual Commit Available)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Barndoor Platform\n  ServiceCategory: AI Governance / Control Plane\n  ProviderName: Barndoor\n  PublisherName: Barndoor AI, Inc.\n  InvoiceIssuerName: Barndoor AI, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: plan_subscription\n    description: >-\n      Recurring monthly subscription per plan tier (Trial / Team / Pro /\n      Enterprise).\
  \ Team is published at $500/month billed annually; Pro and\n      Enterprise are custom.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - organization_id\n      - plan_tier\n  - name: non_human_identities\n    description: >-\n      Registered agents (non-human identities). The published structural\n      quota: Trial unlimited, Team 250, Pro 1,000, Enterprise custom. Likely\n      acts as a seat license rather than a per-call meter.\n    unit: agent\n    aggregation: max\n    dimensions:\n      - organization_id\n      - agent_type\n  - name: mcp_server_registrations\n    description: >-\n      Registered MCP server instances under the organization. Not separately\n      priced today; included in the plan.\n    unit: mcp_server\n    aggregation: max\n    dimensions:\n      - organization_id\n      - server_type\n  - name: oauth_connections\n    description: >-\n      OAuth connections established from agents to backend SaaS through\n      Barndoor's connection broker.\
  \ Not separately priced today.\n    unit: connection\n    aggregation: sum\n    dimensions:\n      - organization_id\n      - mcp_server_id\n      - status\n  - name: governance_events\n    description: >-\n      Policy decisions emitted by the runtime enforcement engine (Cerbos PDP)\n      against agent actions. Surfaced through audit logs and dashboards; not\n      separately priced today.\n    unit: decision\n    aggregation: sum\n    dimensions:\n      - organization_id\n      - policy_id\n      - authorized\n  - name: mcp_proxy_requests\n    description: >-\n      Requests proxied through Barndoor's MCP / SSE endpoints\n      (`/mcp/{server}`, `/sse/{server}`) to backend MCP servers. Not\n      separately priced today.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - organization_id\n      - mcp_server_id\n      - agent_id\n  - name: audit_log_events_exported\n    description: >-\n      Audit events exported to S3-compatible storage. Batched every 30\n      seconds\
  \ or per 100 events. Not separately priced today; included in\n      Pro and Enterprise.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - organization_id\n      - bucket\n  - name: private_deployment\n    description: >-\n      Private cloud / on-premises deployment add-on (Enterprise only).\n      Custom-quoted.\n    unit: month\n    aggregation: max\n    dimensions:\n      - organization_id\nprinciples:\n  - name: Visibility\n    description: >-\n      Use Barndoor's audit dashboards plus the audit-log export to S3 /\n      Datadog-compatible JSON to reconcile policy decisions and proxied MCP\n      requests against agent attribution. Pull `getAgentCounts` for current\n      seat utilization.\n  - name: Allocation\n    description: >-\n      Tag agents by team / product via `application_directory_id` so MCP\n      proxy and policy-decision volume flows back to the right cost center.\n      Maintain separate test and production organizations to keep development\n     \
  \ activity off the production seat count.\n  - name: Optimization\n    description: >-\n      Right-size the plan tier to actual agent count (Trial -> Team -> Pro\n      -> Enterprise). Archive or unregister unused agents to stay within the\n      tier ceiling. Use ABAC conditions to scope tool exposure narrowly so\n      agents only consume the MCP tools they need.\n  - name: Accountability\n    description: >-\n      Assign an AI Governance owner per organization. Review SOC 2 evidence\n      and audit-log export config quarterly; track plan-tier renewals\n      against the agent seat trend.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/barndoor/refs/heads/main/finops/barndoor-finops.yml
sources:
- https://barndoor.ai/pricing
- https://docs.barndoor.ai/api-reference/introduction
- https://docs.barndoor.ai/how-tos/log-export
specification: FinOps Framework
tags:
- AI Agents
- AI Governance
- MCP
- Control Plane
- FinOps
- FOCUS
---
