---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Credits
description: Infura bills as monthly subscription with daily credit allotments. Overage handling depends on plan; Custom is contracted.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: ConsenSys
  ProviderName: Infura
  PublisherName: ConsenSys
  ServiceCategory: Web3
  ServiceName: Infura
layout: finops
meters:
- aggregation: sum
  description: Daily request credits weighted per method.
  dimensions:
  - api_key
  - network
  - method
  name: credits
  unit: credit
- aggregation: max
  description: IPFS pinned bytes.
  dimensions:
  - account
  name: ipfs_storage
  unit: byte
name: Infura Finops
provider_name: Infura
provider_slug: infura
publisher_name: ConsenSys (MetaMask)
service_category: Web3
slug: infura-finops
source_filename: infura-finops.yml
source_heading: FinOps Profile
source_url: https://docs.metamask.io/services/get-started/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Infura\nproviderId: infura\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- RPC\n- Infrastructure\n- MetaMask\n- ConsenSys\n- FinOps\n- FOCUS\ndescription: Infura bills as monthly subscription with daily credit allotments. Overage\n  handling depends on plan; Custom is contracted.\nnotes: Usage data viewable in MetaMask Developer dashboard. Invoiced via ConsenSys.\nsources:\n- https://docs.metamask.io/services/get-started/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ConsenSys (MetaMask)\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Credits\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: Infura\n  ServiceCategory: Web3\n  ProviderName: Infura\n  PublisherName: ConsenSys\n  InvoiceIssuerName: ConsenSys\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: credits\n  description: Daily request credits weighted per method.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - api_key\n  - network\n  - method\n- name: ipfs_storage\n  description: IPFS pinned bytes.\n  unit: byte\n  aggregation: max\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Monitor credit burn in the MetaMask Developer dashboard.\n- name: Allocation\n  description: Use one project key per environment/team to attribute credits.\n- name: Optimization\n  description: Cache responses; avoid archive unless required; use eth_getLogs windows\n    judiciously.\n- name: Accountability\n  description: Designate project owners; review against\
  \ daily allotment.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/infura/refs/heads/main/finops/infura-finops.yml
sources:
- https://docs.metamask.io/services/get-started/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- RPC
- Infrastructure
- MetaMask
- ConsenSys
- FinOps
- FOCUS
---
