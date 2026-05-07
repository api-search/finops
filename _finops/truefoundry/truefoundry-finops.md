---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: truefoundry-ai-gateway-openapi.yml
  format: yaml
  label: TrueFoundry AI Gateway API
  slug: truefoundry-ai-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/truefoundry/refs/heads/main/openapi/truefoundry-ai-gateway-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription + Overage
description: FOCUS-aligned FinOps for TrueFoundry's AI Gateway and MLOps platform — a tiered monthly subscription ($0 / $499 / $2,999 / custom) with included request allowances per tier and per-request overage on Pro; Enterprise adds VPC, on-prem, and air-gapped deployments with custom commercial terms.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: TrueFoundry, Inc.
  ProviderName: TrueFoundry
  PublisherName: TrueFoundry, Inc.
  ServiceCategory: AI Gateway / LLMOps
  ServiceName: TrueFoundry AI Gateway
layout: finops
meters:
- aggregation: sum
  description: Monthly tier subscription (Developer free, Pro $499, Pro Plus $2,999, Enterprise custom).
  dimensions:
  - tier
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Requests routed through the AI Gateway; counts toward each tier's monthly allowance and drives overage on Pro.
  dimensions:
  - tier
  - model
  - virtual_key
  name: gateway_requests
  unit: request
- aggregation: max
  description: Active platform users (3 Developer, 10 Pro, 25 Pro Plus, unlimited Enterprise).
  dimensions:
  - tier
  name: seats
  unit: seat
- aggregation: sum
  description: MCP gateway tool calls; included up to 5M/month on Pro Plus.
  dimensions:
  - mcp_server
  name: mcp_tool_calls
  unit: call
- aggregation: max
  description: Distinct MCP servers configured under the gateway (up to 50 on Pro Plus).
  name: mcp_servers
  unit: server
name: Truefoundry Finops
provider_name: TrueFoundry
provider_slug: truefoundry
publisher_name: TrueFoundry, Inc.
service_category: AI Gateway / LLMOps
slug: truefoundry-finops
source_filename: truefoundry-finops.yml
source_heading: FinOps Profile
source_url: https://www.truefoundry.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TrueFoundry\nproviderId: truefoundry\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Gateway\n  - LLMOps\n  - GenAI\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for TrueFoundry's AI Gateway and MLOps platform — a tiered monthly subscription\n  ($0 / $499 / $2,999 / custom) with included request allowances per tier and per-request overage on Pro;\n  Enterprise adds VPC, on-prem, and air-gapped deployments with custom commercial terms.\nsources:\n  - https://www.truefoundry.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: TrueFoundry, Inc.\nserviceCategory: AI Gateway / LLMOps\nbillingModel:\n  pricingCategory: Tiered Subscription\
  \ + Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: TrueFoundry AI Gateway\n  ServiceCategory: AI Gateway / LLMOps\n  ProviderName: TrueFoundry\n  PublisherName: TrueFoundry, Inc.\n  InvoiceIssuerName: TrueFoundry, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    description: Monthly tier subscription (Developer free, Pro $499, Pro Plus $2,999, Enterprise custom).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: gateway_requests\n    description: Requests routed through the AI Gateway; counts toward each tier's monthly allowance and\n      drives overage on Pro.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n      - model\n      - virtual_key\n  - name: seats\n    description: Active platform users (3 Developer, 10 Pro, 25 Pro Plus, unlimited Enterprise).\n    unit: seat\n    aggregation: max\n    dimensions:\n   \
  \   - tier\n  - name: mcp_tool_calls\n    description: MCP gateway tool calls; included up to 5M/month on Pro Plus.\n    unit: call\n    aggregation: sum\n    dimensions:\n      - mcp_server\n  - name: mcp_servers\n    description: Distinct MCP servers configured under the gateway (up to 50 on Pro Plus).\n    unit: server\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Use the TrueFoundry control center to track gateway request volume, virtual-key spend,\n      and per-model usage in real time.\n  - name: Allocation\n    description: Tag virtual keys by team, environment, and product so gateway requests and overage charges\n      can be charged back; group requests by model and route in dashboards.\n  - name: Optimization\n    description: Lever semantic caching, request routing, and tier selection (Developer for prototyping,\n      Pro for production with overage controls, Enterprise for committed-use VPC/on-prem) to keep cost\n      per useful inference low.\n\
  \  - name: Accountability\n    description: Assign virtual-key ownership to engineering teams and configure gateway-side rate limits\n      and budgets per key; finance reviews the monthly subscription and overage line on the TrueFoundry\n      invoice.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/truefoundry/refs/heads/main/finops/truefoundry-finops.yml
sources:
- https://www.truefoundry.com/pricing
specification: FinOps Framework
tags:
- AI Gateway
- LLMOps
- GenAI
- FinOps
- FOCUS
---
