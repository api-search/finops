---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: eosio-nodeos-chain-api-openapi.yml
  format: yaml
  label: EOSIO Nodeos Chain API
  slug: nodeos-chain-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/eosio/refs/heads/main/openapi/eosio-nodeos-chain-api-openapi.yml
billing_model:
  billingCurrency: EOS (on-chain), USD (infra)
  billingFrequency: Continuous (on-chain)
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Open Source + On-Chain Resource Markets
description: 'FinOps view of EOSIO/Antelope: no vendor invoice. Direct costs are (a) infrastructure to run a self-hosted nodeos and (b) on-chain CPU/NET/RAM purchased through PowerUp, REX, or RAM market to submit transactions. There is no SaaS billing surface from the upstream project.'
focus_columns:
  BillingCurrency: EOS
  InvoiceIssuerName: N/A (open source / on-chain)
  ProviderName: EOSIO
  PublisherName: EOS Network Foundation
  ServiceCategory: Blockchain Infrastructure
  ServiceName: EOSIO
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  - action
  name: cpu_microseconds_consumed
  unit: microseconds
- aggregation: sum
  dimensions:
  - account
  - action
  name: net_bytes_consumed
  unit: bytes
- aggregation: max
  dimensions:
  - account
  name: ram_bytes_held
  unit: bytes
- aggregation: sum
  dimensions:
  - account
  - resource_type
  name: powerup_purchases
  unit: EOS
- aggregation: sum
  dimensions:
  - environment
  - region
  name: node_compute_hours
  unit: instance-hour
name: Eosio Finops
provider_name: EOSIO
provider_slug: eosio
publisher_name: EOS Network Foundation
service_category: Blockchain Infrastructure
slug: eosio-finops
source_filename: eosio-finops.yml
source_heading: FinOps Profile
source_url: https://eosnetwork.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: EOSIO\nproviderId: eosio\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Blockchain\n  - Antelope\n  - EOS\n  - Open Source\ndescription: 'FinOps view of EOSIO/Antelope: no vendor invoice. Direct costs are (a) infrastructure to\n  run a self-hosted nodeos and (b) on-chain CPU/NET/RAM purchased through PowerUp, REX, or RAM market\n  to submit transactions. There is no SaaS billing surface from the upstream project.'\nsources:\n  - https://eosnetwork.com/\n  - https://github.com/AntelopeIO/leap\nnotes: No vendor invoice exists for the EOSIO/Antelope protocol. Cost is split between infrastructure\n  (compute/storage) and on-chain resources (CPU/NET/RAM market prices, denominated in EOS).\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: EOS Network Foundation\nserviceCategory: Blockchain Infrastructure\nbillingModel:\n  pricingCategory: Open Source + On-Chain Resource Markets\n  billingFrequency: Continuous (on-chain)\n  billingCurrency: EOS (on-chain), USD (infra)\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: EOSIO\n  ServiceCategory: Blockchain Infrastructure\n  ProviderName: EOSIO\n  PublisherName: EOS Network Foundation\n  InvoiceIssuerName: N/A (open source / on-chain)\n  BillingCurrency: EOS\nmeters:\n  - name: cpu_microseconds_consumed\n    unit: microseconds\n    aggregation: sum\n    dimensions:\n      - account\n      - action\n  - name: net_bytes_consumed\n    unit: bytes\n    aggregation: sum\n    dimensions:\n      - account\n      - action\n  - name: ram_bytes_held\n    unit: bytes\n    aggregation: max\n    dimensions:\n      - account\n  - name: powerup_purchases\n\
  \    unit: EOS\n    aggregation: sum\n    dimensions:\n      - account\n      - resource_type\n  - name: node_compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - environment\n      - region\nprinciples:\n  - name: Visibility\n    description: Use get_account, get_powerup_state, and history APIs to track on-chain CPU/NET/RAM consumption\n      per account; monitor self-hosted nodeos cost via your cloud bill.\n  - name: Allocation\n    description: Use one EOS account per workload or team so on-chain resource burn is attributable;\n      tag self-hosted node compute by environment.\n  - name: Optimization\n    description: Prefer PowerUp rentals over staking when usage is bursty; batch actions per transaction\n      to amortize NET overhead; right-size nodeos hardware (history nodes are RAM-heavy).\n  - name: Accountability\n    description: Treasury or platform team owns nodeos infrastructure; product teams own their on-chain\n      account budgets and\
  \ PowerUp top-ups.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/eosio/refs/heads/main/finops/eosio-finops.yml
sources:
- https://eosnetwork.com/
- https://github.com/AntelopeIO/leap
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Blockchain
- Antelope
- EOS
- Open Source
---
