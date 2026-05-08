---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: uniswap-trading-openapi.yaml
  format: yaml
  label: Uniswap Trading API
  slug: uniswap-trading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/uniswap/refs/heads/main/openapi/uniswap-trading-openapi.yaml
billing_model:
  billingCurrency: USD/ETH/GRT
  billingFrequency: Monthly (subgraph) + On-Demand (gas)
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Pay-As-You-Go
description: FOCUS-aligned FinOps for Uniswap consumers - on-chain trading cost is dominated by Ethereum / L2 gas plus pool fees that flow to liquidity providers, while data access cost is dominated by subgraph query usage billed through The Graph Network.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Graph (subgraph queries); on-chain costs are paid in network gas
  ProviderName: Uniswap
  PublisherName: Uniswap Labs
  ServiceCategory: DeFi
  ServiceName: Uniswap
layout: finops
meters:
- aggregation: sum
  description: GraphQL queries against Uniswap subgraphs on The Graph Network; billed at $2 per 100K beyond the free tier.
  dimensions:
  - subgraph
  - api_key
  name: subgraph_queries
  unit: query
- aggregation: sum
  description: Gas consumed by on-chain Uniswap protocol interactions, paid in the underlying network's gas token.
  dimensions:
  - chain
  - tx_type
  name: network_gas
  unit: gas
- aggregation: sum
  description: Notional swap volume passing through a Uniswap pool; pool fee tier (0.01% / 0.05% / 0.30% / 1.00%) determines LP payout.
  dimensions:
  - chain
  - pool
  - fee_tier
  name: pool_fee_volume
  unit: trade_volume
name: Uniswap Finops
provider_name: Uniswap
provider_slug: uniswap
publisher_name: Uniswap Labs (protocol); The Graph (subgraph queries)
service_category: DeFi / On-Chain Data
slug: uniswap-finops
source_filename: uniswap-finops.yml
source_heading: FinOps Profile
source_url: https://developers.uniswap.org/api/subgraph/overview
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Uniswap\nproviderId: uniswap\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Blockchain\n  - DeFi\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Uniswap consumers - on-chain trading cost is dominated by Ethereum\n  / L2 gas plus pool fees that flow to liquidity providers, while data access cost is dominated by\n  subgraph query usage billed through The Graph Network.\nsources:\n  - https://developers.uniswap.org/api/subgraph/overview\n  - https://thegraph.com/docs/en/subgraphs/billing/\n  - https://thegraph.com/studio-pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Uniswap Labs (protocol); The Graph (subgraph queries)\nserviceCategory:\
  \ DeFi / On-Chain Data\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n  billingFrequency: Monthly (subgraph) + On-Demand (gas)\n  billingCurrency: USD/ETH/GRT\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Uniswap\n  ServiceCategory: DeFi\n  ProviderName: Uniswap\n  PublisherName: Uniswap Labs\n  InvoiceIssuerName: The Graph (subgraph queries); on-chain costs are paid in network gas\n  BillingCurrency: USD\nmeters:\n  - name: subgraph_queries\n    description: GraphQL queries against Uniswap subgraphs on The Graph Network; billed at $2 per\n      100K beyond the free tier.\n    unit: query\n    aggregation: sum\n    dimensions:\n      - subgraph\n      - api_key\n  - name: network_gas\n    description: Gas consumed by on-chain Uniswap protocol interactions, paid in the underlying network's\n      gas token.\n    unit: gas\n    aggregation: sum\n    dimensions:\n      - chain\n      - tx_type\n  - name: pool_fee_volume\n    description: Notional swap\
  \ volume passing through a Uniswap pool; pool fee tier (0.01% / 0.05%\n      / 0.30% / 1.00%) determines LP payout.\n    unit: trade_volume\n    aggregation: sum\n    dimensions:\n      - chain\n      - pool\n      - fee_tier\nprinciples:\n  - name: Visibility\n    description: Track subgraph query volume in The Graph Studio per API key; track on-chain gas\n      and routing efficiency by indexing Uniswap router contract events per wallet or smart-account.\n  - name: Allocation\n    description: Issue separate Graph Studio API keys per consuming team, environment, or product\n      to attribute subgraph spend; tag wallets/relayers used for on-chain calls so gas can be allocated\n      per workload.\n  - name: Optimization\n    description: Cache subgraph results, prefer batched queries, and self-host high-volume subgraphs\n      using the official repos to escape per-query pricing. For trading, route via UniswapX or auto-router\n      to reduce gas and slippage; choose appropriate fee\
  \ tier and L2 deployment for the trade size.\n  - name: Accountability\n    description: Set Graph Studio billing alerts ahead of monthly query budgets; for on-chain workloads\n      assign wallet ownership and gas budgets per integration to detect runaway transactions.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/uniswap/refs/heads/main/finops/uniswap-finops.yml
sources:
- https://developers.uniswap.org/api/subgraph/overview
- https://thegraph.com/docs/en/subgraphs/billing/
- https://thegraph.com/studio-pricing/
specification: FinOps Framework
tags:
- Blockchain
- DeFi
- FinOps
- FOCUS
---
