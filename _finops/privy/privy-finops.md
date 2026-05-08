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
  pricingCategory: Subscription + MAW
description: Privy bills as monthly subscription with included MAW plus per-MAW overages. Wallet RPC calls and webhook deliveries may have separate metering on Enterprise contracts.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Privy
  ProviderName: Privy
  PublisherName: Privy
  ServiceCategory: Web3
  ServiceName: Privy
layout: finops
meters:
- aggregation: count_distinct
  description: Distinct wallets active in a billing period.
  dimensions:
  - app
  name: monthly_active_wallets
  unit: wallet
- aggregation: sum
  description: Wallet RPC calls.
  dimensions:
  - app
  - wallet
  name: wallet_rpc_calls
  unit: call
name: Privy Finops
provider_name: Privy
provider_slug: privy
publisher_name: Privy Technology, Inc.
service_category: Web3
slug: privy-finops
source_filename: privy-finops.yml
source_heading: FinOps Profile
source_url: https://www.privy.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Privy\nproviderId: privy\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Wallets\n- Authentication\n- Embedded Wallets\n- MPC\n- FinOps\n- FOCUS\ndescription: Privy bills as monthly subscription with included MAW plus per-MAW overages.\n  Wallet RPC calls and webhook deliveries may have separate metering on Enterprise\n  contracts.\nnotes: Usage in Privy dashboard.\nsources:\n- https://www.privy.io/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Privy Technology, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + MAW\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: Privy\n  ServiceCategory: Web3\n  ProviderName: Privy\n  PublisherName: Privy\n  InvoiceIssuerName: Privy\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: monthly_active_wallets\n  description: Distinct wallets active in a billing period.\n  unit: wallet\n  aggregation: count_distinct\n  dimensions:\n  - app\n- name: wallet_rpc_calls\n  description: Wallet RPC calls.\n  unit: call\n  aggregation: sum\n  dimensions:\n  - app\n  - wallet\nprinciples:\n- name: Visibility\n  description: Privy dashboard surfaces MAW per app per month.\n- name: Allocation\n  description: Use one Privy app per product/environment.\n- name: Optimization\n  description: Reduce MAW by deduplicating accounts; archive inactive apps.\n- name: Accountability\n  description: App owners review MAW vs plan.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/privy/refs/heads/main/finops/privy-finops.yml
sources:
- https://www.privy.io/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Wallets
- Authentication
- Embedded Wallets
- MPC
- FinOps
- FOCUS
---
