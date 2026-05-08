---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: SOL
  billingFrequency: Per Transaction
  chargeCategories:
  - Usage
  pricingCategory: On-chain Usage Fee
description: FinOps view of Raydium. There is no SaaS bill. Cost is Solana priority-fee gas (paid in SOL) and per-pool swap fee (paid in trade asset). FinOps allocation is by wallet and by program interaction; the public REST API is free.
focus_columns:
  BillingCurrency: SOL
  ChargeCategory: Usage
  InvoiceIssuerName: On-chain
  ProviderName: Raydium DAO
  PublisherName: Raydium DAO
  ServiceCategory: DeFi Protocol
  ServiceName: Raydium AMM/CLMM
layout: finops
meters:
- aggregation: sum
  description: Solana priority-fee gas per swap or LP operation.
  dimensions:
  - wallet
  - pool
  name: priority_fee
  unit: lamport
- aggregation: sum
  description: Per-pool swap fee (typically 0.25% AMM, variable CLMM).
  dimensions:
  - wallet
  - pool
  name: pool_swap_fee
  unit: percent_of_notional
name: Raydium Finops
provider_name: Raydium
provider_slug: raydium
publisher_name: Raydium DAO
service_category: DeFi Protocol
slug: raydium-finops
source_filename: raydium-finops.yml
source_heading: FinOps Profile
source_url: https://docs.raydium.io/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Raydium\nproviderId: raydium\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Solana\n  - DEX\n  - On-chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Raydium. There is no SaaS bill. Cost is Solana priority-fee gas (paid in SOL)\n  and per-pool swap fee (paid in trade asset). FinOps allocation is by wallet and by program\n  interaction; the public REST API is free.\nsources:\n  - https://docs.raydium.io/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Raydium DAO\nserviceCategory: DeFi Protocol\nbillingModel:\n  pricingCategory: On-chain Usage Fee\n  billingFrequency: Per Transaction\n\
  \  billingCurrency: SOL\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Raydium AMM/CLMM\n  ServiceCategory: DeFi Protocol\n  ProviderName: Raydium DAO\n  PublisherName: Raydium DAO\n  InvoiceIssuerName: On-chain\n  BillingCurrency: SOL\n  ChargeCategory: Usage\nmeters:\n  - name: priority_fee\n    description: Solana priority-fee gas per swap or LP operation.\n    unit: lamport\n    aggregation: sum\n    dimensions:\n      - wallet\n      - pool\n  - name: pool_swap_fee\n    description: Per-pool swap fee (typically 0.25% AMM, variable CLMM).\n    unit: percent_of_notional\n    aggregation: sum\n    dimensions:\n      - wallet\n      - pool\nprinciples:\n  - name: Visibility\n    description: Pull on-chain swap events into FinOps store; tag by wallet and pool.\n  - name: Allocation\n    description: Allocate priority fees and swap fees to consuming desk by wallet.\n  - name: Optimization\n    description: Bundle swaps into single Solana transactions; tune priority fees.\n\
  \  - name: Accountability\n    description: Assign a wallet owner per executing strategy; reconcile monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/raydium/refs/heads/main/finops/raydium-finops.yml
sources:
- https://docs.raydium.io/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Solana
- DEX
- On-chain
- FinOps
- FOCUS
---
