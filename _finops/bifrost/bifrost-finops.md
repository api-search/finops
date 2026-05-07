---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bifrost-http-gateway-api.yaml
  format: yaml
  label: Bifrost HTTP Gateway API
  slug: bifrost-http-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bifrost/refs/heads/main/openapi/bifrost-http-gateway-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Open Source + Enterprise License
description: 'FOCUS-aligned FinOps for Bifrost: dual-track shape — free Apache 2.0 OSS edition (zero license cost; operator pays infrastructure + upstream LLM costs) and a custom-priced Enterprise edition for governed deployments. Bifrost itself is not a billable service; it is a cost-governance layer in front of upstream AI providers.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Maxim AI
  PricingCategory: License + Pass-Through
  PricingUnit: license-year
  ProviderName: Bifrost
  PublisherName: Maxim AI
  ServiceCategory: AI Infrastructure / Gateway
  ServiceName: Bifrost
layout: finops
meters:
- aggregation: sum
  description: Annual Enterprise license fee (custom-priced)
  dimensions:
  - tenant
  - deployment_type
  name: enterprise_license
  unit: license-year
- aggregation: sum
  description: Compute cost to run Bifrost gateway nodes (operator's cloud bill)
  dimensions:
  - region
  - instance_type
  - cluster
  name: self_hosted_compute
  unit: instance-hour
- aggregation: sum
  description: Token spend on upstream LLM providers, attributed to a virtual key
  dimensions:
  - upstream_provider
  - model
  - virtual_key
  - team
  name: upstream_llm_tokens
  unit: token
- aggregation: sum
  description: Request count to upstream LLM providers, attributed to a virtual key
  dimensions:
  - upstream_provider
  - model
  - virtual_key
  - team
  name: upstream_llm_requests
  unit: request
- aggregation: count
  description: Semantic-cache hits that avoided an upstream call (cost-savings meter)
  dimensions:
  - virtual_key
  - upstream_provider
  name: cache_hits
  unit: request
name: Bifrost Finops
provider_name: Bifrost
provider_slug: bifrost
publisher_name: Maxim AI (maximhq)
service_category: AI Infrastructure / Gateway
slug: bifrost-finops
source_filename: bifrost-finops.yml
source_heading: FinOps Profile
source_url: https://getbifrost.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bifrost\nproviderId: bifrost\npublisherName: Maxim AI (maximhq)\nserviceCategory: AI Infrastructure / Gateway\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Gateway\n  - LLM\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Bifrost: dual-track shape — free Apache 2.0 OSS edition (zero\n  license cost; operator pays infrastructure + upstream LLM costs) and a custom-priced Enterprise edition\n  for governed deployments. Bifrost itself is not a billable service; it is a cost-governance layer in\n  front of upstream AI providers.'\nsources:\n  - https://getbifrost.ai/pricing\n  - https://docs.getbifrost.ai/\nprinciples:\n  - name:\
  \ Visibility\n    description: Use Bifrost's OpenTelemetry exports to attribute requests, tokens, and upstream-provider\n      cost to virtual keys. The prompt repository and playground surface per-request cost.\n  - name: Allocation\n    description: Issue a virtual key per team/product/environment. Bifrost annotates every request with\n      the key, enabling chargeback by team or cost center even though Bifrost itself is free.\n  - name: Optimization\n    description: Use semantic caching to avoid upstream calls, automatic fallbacks to route to cheaper\n      providers/models, and adaptive load balancing (Enterprise) to redistribute load when an upstream\n      becomes expensive or rate-limited.\n  - name: Accountability\n    description: Set per-virtual-key budgets so each consuming team has a hard cap on upstream spend.\n      Audit logs (Enterprise) record who created keys and approved budget changes.\nbillingModel:\n  pricingCategory: Open Source + Enterprise License\n  billingFrequency:\
  \ Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bifrost\n  ServiceCategory: AI Infrastructure / Gateway\n  ProviderName: Bifrost\n  PublisherName: Maxim AI\n  InvoiceIssuerName: Maxim AI\n  PricingCategory: License + Pass-Through\n  PricingUnit: license-year\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: enterprise_license\n    description: Annual Enterprise license fee (custom-priced)\n    unit: license-year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - deployment_type\n  - name: self_hosted_compute\n    description: Compute cost to run Bifrost gateway nodes (operator's cloud bill)\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - instance_type\n      - cluster\n  - name: upstream_llm_tokens\n    description: Token spend on upstream LLM providers, attributed to a virtual key\n    unit:\
  \ token\n    aggregation: sum\n    dimensions:\n      - upstream_provider\n      - model\n      - virtual_key\n      - team\n  - name: upstream_llm_requests\n    description: Request count to upstream LLM providers, attributed to a virtual key\n    unit: request\n    aggregation: sum\n    dimensions:\n      - upstream_provider\n      - model\n      - virtual_key\n      - team\n  - name: cache_hits\n    description: Semantic-cache hits that avoided an upstream call (cost-savings meter)\n    unit: request\n    aggregation: count\n    dimensions:\n      - virtual_key\n      - upstream_provider\napis:\n  - name: Bifrost HTTP Gateway API\n    baseURL: http://localhost:8080\n    tags:\n      - AI Gateway\n      - LLM\n      - OpenAI Compatible\n      - REST\n    serviceName: Bifrost HTTP Gateway API\n    serviceCategory: API\n  - name: Bifrost Go SDK\n    baseURL: https://pkg.go.dev/github.com/maximhq/bifrost/core\n    tags:\n      - AI Gateway\n      - Go\n      - LLM\n      - SDK\n    serviceName:\
  \ Bifrost Go SDK\n    serviceCategory: API\n  - name: Bifrost MCP Gateway\n    baseURL: ''\n    tags:\n      - AI Agents\n      - MCP\n      - OAuth\n      - Tool Execution\n    serviceName: Bifrost MCP Gateway\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Cached Request Avoided\n    metric: upstream_savings / cache_hits\n    target: maximize cache hit rate\n  - name: Cost per Virtual Key\n    metric: (upstream_llm_cost + amortized_license) / active_virtual_keys\n    target: align with team/product P&L\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bifrost/refs/heads/main/finops/bifrost-finops.yml
sources:
- https://getbifrost.ai/pricing
- https://docs.getbifrost.ai/
specification: FinOps Framework
tags:
- AI Gateway
- LLM
- Open Source
- FinOps
- FOCUS
---
