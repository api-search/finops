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
description: FinOps view of Curve. There is no SaaS bill. Cost is on-chain gas (chain native token) and Curve protocol swap fee (typically 0.04%) per trade. FinOps allocation is therefore by wallet and by smart-contract interaction, not by API key.
focus_columns:
  BillingCurrency: Native Asset
  ChargeCategory: Usage
  InvoiceIssuerName: On-chain
  ProviderName: Curve Finance DAO
  PublisherName: Curve Finance DAO
  ServiceCategory: DeFi Protocol
  ServiceName: Curve Finance Pools
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
  description: Protocol-level swap fee (typically 0.04%).
  dimensions:
  - wallet
  - pool
  name: protocol_fee
  unit: percent_of_notional
name: Curve Finance Finops
provider_name: Curve Finance
provider_slug: curve-finance
publisher_name: Curve Finance DAO
service_category: DeFi Protocol
slug: curve-finance-finops
source_filename: curve-finance-finops.yml
source_heading: FinOps Profile
source_url: https://docs.curve.finance/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Curve Finance\nproviderId: curve-finance\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - DeFi\n  - DEX\n  - On-chain\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Curve. There is no SaaS bill. Cost is on-chain gas (chain native token) and\n  Curve protocol swap fee (typically 0.04%) per trade. FinOps allocation is therefore by wallet\n  and by smart-contract interaction, not by API key.\nsources:\n  - https://docs.curve.finance/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Curve Finance DAO\nserviceCategory: DeFi Protocol\nbillingModel:\n  pricingCategory: On-chain Usage Fee\n  billingFrequency:\
  \ Per Transaction\n  billingCurrency: Native Chain Asset\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Curve Finance Pools\n  ServiceCategory: DeFi Protocol\n  ProviderName: Curve Finance DAO\n  PublisherName: Curve Finance DAO\n  InvoiceIssuerName: On-chain\n  BillingCurrency: Native Asset\n  ChargeCategory: Usage\nmeters:\n  - name: gas\n    description: Native-asset gas cost per swap or LP operation.\n    unit: gas\n    aggregation: sum\n    dimensions:\n      - wallet\n      - chain\n      - pool\n  - name: protocol_fee\n    description: Protocol-level swap fee (typically 0.04%).\n    unit: percent_of_notional\n    aggregation: sum\n    dimensions:\n      - wallet\n      - pool\nprinciples:\n  - name: Visibility\n    description: Pull on-chain swap events into FinOps store; tag by wallet and pool.\n  - name: Allocation\n    description: Allocate gas and protocol fee to consuming desk by wallet.\n  - name: Optimization\n    description: Batch swaps; choose the cheapest\
  \ pool route; pay attention to gas-price strategy.\n  - name: Accountability\n    description: Assign a wallet owner per executing strategy; reconcile monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/curve-finance/refs/heads/main/finops/curve-finance-finops.yml
sources:
- https://docs.curve.finance/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DeFi
- DEX
- On-chain
- FinOps
- FOCUS
---
