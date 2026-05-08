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
  pricingCategory: Subscription + MAU
description: Dynamic bills as monthly subscription with MAU-based overages and add-on features (server wallets, advanced auth).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Dynamic Labs
  ProviderName: Dynamic
  PublisherName: Dynamic Labs
  ServiceCategory: Web3
  ServiceName: Dynamic
layout: finops
meters:
- aggregation: count_distinct
  description: Distinct users active per month.
  dimensions:
  - environment
  name: monthly_active_users
  unit: user
- aggregation: sum
  description: Wallet signing operations.
  dimensions:
  - environment
  - wallet
  name: wallet_signs
  unit: operation
name: Dynamic Xyz Finops
provider_name: Dynamic
provider_slug: dynamic-xyz
publisher_name: Dynamic Labs, Inc.
service_category: Web3
slug: dynamic-xyz-finops
source_filename: dynamic-xyz-finops.yml
source_heading: FinOps Profile
source_url: https://www.dynamic.xyz/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Dynamic\nproviderId: dynamic-xyz\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Wallets\n- Authentication\n- Embedded Wallets\n- MPC\n- FinOps\n- FOCUS\ndescription: Dynamic bills as monthly subscription with MAU-based overages and add-on\n  features (server wallets, advanced auth).\nnotes: Usage in Dynamic dashboard.\nsources:\n- https://www.dynamic.xyz/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dynamic Labs, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + MAU\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n\
  \  - Purchase\nfocusColumns:\n  ServiceName: Dynamic\n  ServiceCategory: Web3\n  ProviderName: Dynamic\n  PublisherName: Dynamic Labs\n  InvoiceIssuerName: Dynamic Labs\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: monthly_active_users\n  description: Distinct users active per month.\n  unit: user\n  aggregation: count_distinct\n  dimensions:\n  - environment\n- name: wallet_signs\n  description: Wallet signing operations.\n  unit: operation\n  aggregation: sum\n  dimensions:\n  - environment\n  - wallet\nprinciples:\n- name: Visibility\n  description: Dynamic dashboard surfaces MAU per environment.\n- name: Allocation\n  description: Environment-per-product/env.\n- name: Optimization\n  description: Long-lived sessions; consolidate environments.\n- name: Accountability\n  description: Project owners review MAU vs plan.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dynamic-xyz/refs/heads/main/finops/dynamic-xyz-finops.yml
sources:
- https://www.dynamic.xyz/pricing
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
