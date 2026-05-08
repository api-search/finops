---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: Native Chain Asset
  billingFrequency: Per Transaction
  chargeCategories:
  - Usage
  pricingCategory: On-chain Usage Fee
description: FinOps view of Balancer. There is no SaaS bill. Cost is on-chain gas (chain native token), the per-pool swap fee, and the protocol cut. FinOps allocation is by wallet and contract interaction; subgraph access via The Graph Network is a separate cost line if used.
focus_columns:
  BillingCurrency: Native Asset
  ChargeCategory: Usage
  InvoiceIssuerName: On-chain
  ProviderName: Balancer DAO
  PublisherName: Balancer DAO
  ServiceCategory: DeFi Protocol
  ServiceName: Balancer Vault and Pools
layout: finops
meters:
- aggregation: sum
  description: Native-asset gas cost per swap or LP operation.
  dimensions:
  - wallet
  - chain
  - pool
  name: gas
  unit: gas
- aggregation: sum
  description: Per-pool swap fee (set by pool creator).
  dimensions:
  - wallet
  - pool
  name: pool_swap_fee
  unit: percent_of_notional
- aggregation: sum
  description: Optional cost of Subgraph queries via The Graph Network.
  dimensions:
  - api_key
  name: subgraph_credits
  unit: credit
name: Balancer Finops
provider_name: Balancer
provider_slug: balancer
publisher_name: Balancer DAO
service_category: DeFi Protocol
slug: balancer-finops
source_filename: balancer-finops.yml
source_heading: FinOps Profile
source_url: https://docs.balancer.fi/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Balancer\nproviderId: balancer\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - DeFi\n  - DEX\n  - On-chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Balancer. There is no SaaS bill. Cost is on-chain gas (chain native token), the\n  per-pool swap fee, and the protocol cut. FinOps allocation is by wallet and contract\n  interaction; subgraph access via The Graph Network is a separate cost line if used.\nsources:\n  - https://docs.balancer.fi/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Balancer DAO\nserviceCategory: DeFi Protocol\nbillingModel:\n  pricingCategory: On-chain Usage\
  \ Fee\n  billingFrequency: Per Transaction\n  billingCurrency: Native Chain Asset\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Balancer Vault and Pools\n  ServiceCategory: DeFi Protocol\n  ProviderName: Balancer DAO\n  PublisherName: Balancer DAO\n  InvoiceIssuerName: On-chain\n  BillingCurrency: Native Asset\n  ChargeCategory: Usage\nmeters:\n  - name: gas\n    description: Native-asset gas cost per swap or LP operation.\n    unit: gas\n    aggregation: sum\n    dimensions:\n      - wallet\n      - chain\n      - pool\n  - name: pool_swap_fee\n    description: Per-pool swap fee (set by pool creator).\n    unit: percent_of_notional\n    aggregation: sum\n    dimensions:\n      - wallet\n      - pool\n  - name: subgraph_credits\n    description: Optional cost of Subgraph queries via The Graph Network.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Pull on-chain swap events into FinOps store;\
  \ tag by wallet and pool.\n  - name: Allocation\n    description: Allocate gas and swap fees to consuming desk by wallet.\n  - name: Optimization\n    description: Use SOR to find lowest-fee route; choose pools with lower swap fee where appropriate.\n  - name: Accountability\n    description: Assign a wallet owner per executing strategy; reconcile monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/balancer/refs/heads/main/finops/balancer-finops.yml
sources:
- https://docs.balancer.fi/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DeFi
- DEX
- On-chain
- FinOps
- FOCUS
---
