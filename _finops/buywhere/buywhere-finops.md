---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: buywhere-openapi.yml
  format: yaml
  label: BuyWhere Product Catalog API
  slug: product-catalog-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/buywhere/refs/heads/main/openapi/buywhere-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: NotPublished
  chargeCategories:
  - Usage
  pricingCategory: Freemium with Contact-Sales Paid Tiers
description: FOCUS-aligned FinOps profile for BuyWhere. BuyWhere publishes a free agent tier (60 rpm, 1,000 calls/month) and signals live and partner tiers in its MCP documentation; pricing for paid tiers has not been published on a formal pricing page and is contact-sales. This profile captures the metering surface (per-key, per-tier rate limits and monthly quotas) and is marked unreconciled until BuyWhere publishes a formal commercial pricing surface.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: BuyWhere
  ProviderName: BuyWhere
  PublisherName: BuyWhere
  ServiceCategory: Commerce / Product Catalog
  ServiceName: BuyWhere Product Catalog API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api_key_tier
  - api_key
  - operation
  - country_code
  - domain
  name: api_calls
  unit: request
- aggregation: sum
  dimensions:
  - api_key_tier
  - api_key
  - tool
  name: mcp_tool_invocations
  unit: invocation
- aggregation: sum
  dimensions:
  - api_key
  - api_key_tier
  name: monthly_quota_consumption
  unit: request
name: Buywhere Finops
provider_name: BuyWhere
provider_slug: buywhere
publisher_name: BuyWhere
service_category: Commerce / Product Catalog
slug: buywhere-finops
source_filename: buywhere-finops.yml
source_heading: FinOps Profile
source_url: https://api.buywhere.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: BuyWhere\nproviderId: buywhere\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\ntags:\n  - E-commerce\n  - Shopping\n  - AI Agents\n  - FinOps\n  - FOCUS\n  - MCP\ndescription: >-\n  FOCUS-aligned FinOps profile for BuyWhere. BuyWhere publishes a free\n  agent tier (60 rpm, 1,000 calls/month) and signals live and partner\n  tiers in its MCP documentation; pricing for paid tiers has not been\n  published on a formal pricing page and is contact-sales. This profile\n  captures the metering surface (per-key, per-tier rate limits and\n  monthly quotas) and is marked unreconciled until BuyWhere publishes a\n  formal commercial pricing surface.\nsources:\n  - https://api.buywhere.ai/\n  - https://api.buywhere.ai/llms.txt\n  - https://api.buywhere.ai/docs/guides/mcp\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: BuyWhere\nserviceCategory: Commerce / Product Catalog\nbillingModel:\n  pricingCategory: Freemium with Contact-Sales Paid Tiers\n  billingFrequency: NotPublished\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: BuyWhere Product Catalog API\n  ServiceCategory: Commerce / Product Catalog\n  ProviderName: BuyWhere\n  PublisherName: BuyWhere\n  InvoiceIssuerName: BuyWhere\n  BillingCurrency: USD\nmeters:\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key_tier\n      - api_key\n      - operation\n      - country_code\n      - domain\n  - name: mcp_tool_invocations\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - api_key_tier\n      - api_key\n      - tool\n  - name: monthly_quota_consumption\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n\
  \      - api_key_tier\nprinciples:\n  - name: Visibility\n    description: |\n      Track call volume per agent / API key per operation. The free tier exposes a 1,000\n      calls/month ceiling, so visibility is essential to predict upgrade timing.\n  - name: Allocation\n    description: |\n      Tag calls by agent application, MCP tool name, and country_code so usage is\n      attributable when paid tiers ship. The api_key prefix (`bw_free_`, `bw_live_`,\n      `bw_partner_`) is the primary cost-pool dimension.\n  - name: Optimization\n    description: |\n      Use `compact=true` on /products/search to lower per-call processing cost; respect\n      `meta.cached` to identify free cache hits; respect `Retry-After` to avoid 429-induced\n      retry storms. For agentic workflows, compose multiple operations into a single MCP\n      tool call (find_best_value) to amortize round-trip overhead.\n  - name: Accountability\n    description: |\n      Designate an owner for BuyWhere usage tracking;\
  \ revisit when BuyWhere publishes formal\n      pricing and metering policies.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/buywhere/refs/heads/main/finops/buywhere-finops.yml
sources:
- https://api.buywhere.ai/
- https://api.buywhere.ai/llms.txt
- https://api.buywhere.ai/docs/guides/mcp
specification: FinOps Framework
tags:
- E-commerce
- Shopping
- AI Agents
- FinOps
- FOCUS
- MCP
---
