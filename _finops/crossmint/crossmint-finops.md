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
  pricingCategory: Usage-Based
description: Crossmint bills production usage per operation with checkout transaction fees and minting fees on top of any gas pass-through.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Crossmint
  ProviderName: Crossmint
  PublisherName: Crossmint
  ServiceCategory: Web3
  ServiceName: Crossmint
layout: finops
meters:
- aggregation: sum
  description: Wallet operations (create, sign, send).
  dimensions:
  - project
  - chain
  name: wallet_operations
  unit: operation
- aggregation: sum
  description: NFT mints.
  dimensions:
  - project
  - collection
  - chain
  name: mints
  unit: mint
- aggregation: sum
  description: Checkout dollar volume.
  dimensions:
  - project
  name: checkout_volume
  unit: USD
- aggregation: sum
  description: Gas reimbursed/sponsored.
  dimensions:
  - chain
  name: gas_pass_through
  unit: USD
name: Crossmint Finops
provider_name: Crossmint
provider_slug: crossmint
publisher_name: Crossmint, Inc.
service_category: Web3
slug: crossmint-finops
source_filename: crossmint-finops.yml
source_heading: FinOps Profile
source_url: https://www.crossmint.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Crossmint\nproviderId: crossmint\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Wallets\n- NFT\n- Payments\n- Checkout\n- FinOps\n- FOCUS\ndescription: Crossmint bills production usage per operation with checkout transaction\n  fees and minting fees on top of any gas pass-through.\nnotes: Invoiced via Crossmint.\nsources:\n- https://www.crossmint.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Crossmint, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n\
  focusColumns:\n  ServiceName: Crossmint\n  ServiceCategory: Web3\n  ProviderName: Crossmint\n  PublisherName: Crossmint\n  InvoiceIssuerName: Crossmint\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: wallet_operations\n  description: Wallet operations (create, sign, send).\n  unit: operation\n  aggregation: sum\n  dimensions:\n  - project\n  - chain\n- name: mints\n  description: NFT mints.\n  unit: mint\n  aggregation: sum\n  dimensions:\n  - project\n  - collection\n  - chain\n- name: checkout_volume\n  description: Checkout dollar volume.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - project\n- name: gas_pass_through\n  description: Gas reimbursed/sponsored.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - chain\nprinciples:\n- name: Visibility\n  description: Use Crossmint dashboard usage tab and invoices.\n- name: Allocation\n  description: Tag projects per app/team.\n- name: Optimization\n  description: Batch mints; use Solana for low-fee high-volume.\n\
  - name: Accountability\n  description: Project owners review monthly spend.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/crossmint/refs/heads/main/finops/crossmint-finops.yml
sources:
- https://www.crossmint.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Wallets
- NFT
- Payments
- Checkout
- FinOps
- FOCUS
---
