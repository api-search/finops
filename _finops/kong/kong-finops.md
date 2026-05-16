---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kong-gateway-admin-api.yml
  format: yaml
  label: Kong Gateway Admin API
  slug: kong-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kong/refs/heads/main/openapi/kong-gateway-admin-api.yml
- filename: kong-konnect-platform-api.yml
  format: yaml
  label: Kong Konnect Platform API
  slug: kong-konnect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kong/refs/heads/main/openapi/kong-konnect-platform-api.yml
- filename: openapi.yaml
  format: yaml
  label: Kong Event Gateway
  slug: kong-event-gateway
  spec_type: OpenAPI
  url: https://developer.konghq.com/api/konnect/event-gateway/v1/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Credit
  pricingCategory: Subscription + Usage Overage
description: 'FOCUS-aligned FinOps for Kong Konnect: per-Gateway-per-month subscription with included request quotas (1M/mo) and per-million overages (capped at 10M/mo on Plus), plus per-LLM-model AI Gateway charges, per-portal and per-published-API overages, and seat-based Insomnia pricing. AI Gateway / Agent Gateway / MCP Registry / Event Gateway / Context Mesh ride inside the Plus or Enterprise envelope rather than as separate SKUs.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Kong Inc.
  ProviderName: Kong
  PublisherName: Kong Inc.
  ServiceCategory: Developer Tools
  ServiceName: Kong Konnect
  ServiceSubcategory: API Management
layout: finops
meters:
- aggregation: max
  dimensions:
  - gateway_type
  - region
  name: gateway_months
  unit: gateway-month
- aggregation: sum
  dimensions:
  - gateway
  - service
  - consumer
  name: api_requests
  unit: request
- aggregation: max
  dimensions:
  - provider
  - model
  name: ai_gateway_models
  unit: llm_model
- aggregation: max
  name: developer_portals
  unit: portal
- aggregation: max
  dimensions:
  - portal
  name: published_apis
  unit: api
- aggregation: max
  dimensions:
  - plan
  name: insomnia_seats
  unit: seat-month
- aggregation: max
  dimensions:
  - registry
  - tool_type
  name: mcp_registry_tools
  unit: tool
- aggregation: sum
  dimensions:
  - source_agent
  - destination_agent
  name: a2a_traffic
  unit: message
- aggregation: sum
  dimensions:
  - virtual_cluster
  - topic
  name: event_gateway_throughput
  unit: byte
name: Kong Finops
provider_name: Kong
provider_slug: kong
publisher_name: Kong Inc.
service_category: API Management
slug: kong-finops
source_filename: kong-finops.yml
source_heading: FinOps Profile
source_url: https://konghq.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kong\nproviderId: kong\ncreated: '2026-05-04'\nmodified: '2026-05-15'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - API Gateway\n  - API Management\n  - AI Gateway\n  - MCP Registry\ndescription: 'FOCUS-aligned FinOps for Kong Konnect: per-Gateway-per-month subscription with included\n  request quotas (1M/mo) and per-million overages (capped at 10M/mo on Plus), plus per-LLM-model AI\n  Gateway charges, per-portal and per-published-API overages, and seat-based Insomnia pricing.\n  AI Gateway / Agent Gateway / MCP Registry / Event Gateway / Context Mesh ride inside the Plus or\n  Enterprise envelope rather than as separate SKUs.'\nsources:\n  - https://konghq.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Kong Inc.\nserviceCategory: API Management\nbillingModel:\n  pricingCategory: Subscription + Usage Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Kong Konnect\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: API Management\n  ProviderName: Kong\n  PublisherName: Kong Inc.\n  InvoiceIssuerName: Kong Inc.\n  BillingCurrency: USD\nmeters:\n  - name: gateway_months\n    unit: gateway-month\n    aggregation: max\n    dimensions:\n      - gateway_type\n      - region\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - gateway\n      - service\n      - consumer\n  - name: ai_gateway_models\n    unit: llm_model\n    aggregation: max\n    dimensions:\n      - provider\n      - model\n  - name: developer_portals\n    unit: portal\n    aggregation: max\n  - name: published_apis\n    unit: api\n    aggregation:\
  \ max\n    dimensions:\n      - portal\n  - name: insomnia_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: mcp_registry_tools\n    unit: tool\n    aggregation: max\n    dimensions:\n      - registry\n      - tool_type\n  - name: a2a_traffic\n    unit: message\n    aggregation: sum\n    dimensions:\n      - source_agent\n      - destination_agent\n  - name: event_gateway_throughput\n    unit: byte\n    aggregation: sum\n    dimensions:\n      - virtual_cluster\n      - topic\nprinciples:\n  - name: Visibility\n    description: Use Konnect Analytics and the Konnect API to track per-gateway request counts, model\n      usage, and portal activity; export to your data warehouse for FOCUS-aligned roll-up.\n  - name: Allocation\n    description: Tag Konnect services and consumers with team / product metadata so per-million request\n      overages and AI-model fees can be allocated to the consuming team.\n  - name: Optimization\n    description: Consolidate\
  \ low-traffic services onto fewer Serverless gateways (each one billed); cap\n      AI Gateway to the 5 LLM models the team actually uses; collapse extra Developer Portals (each\n      additional portal is $200/mo) and prune low-traffic published APIs ($20 / $10 per API per portal);\n      move to Enterprise once you exceed Plus gateway/portal limits, hit the 10M/mo request ceiling, or\n      accrue meaningful overage spend.\n  - name: Accountability\n    description: Platform owners review monthly Konnect usage vs included quotas, alert on overage thresholds\n      via Konnect Analytics, and reconcile Insomnia seat counts with the IdP each renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kong/refs/heads/main/finops/kong-finops.yml
sources:
- https://konghq.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- API Gateway
- API Management
- AI Gateway
- MCP Registry
---
