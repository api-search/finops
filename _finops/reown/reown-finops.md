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
description: Reown bills as monthly subscription plus MAW-based overages on production usage. Notify push messages may be metered separately.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Reown
  ProviderName: Reown
  PublisherName: Reown
  ServiceCategory: Web3
  ServiceName: Reown
layout: finops
meters:
- aggregation: count_distinct
  description: Distinct wallet sessions per month.
  dimensions:
  - project_id
  name: monthly_active_wallets
  unit: wallet
- aggregation: sum
  description: Notify push messages sent.
  dimensions:
  - project_id
  name: notify_messages
  unit: message
- aggregation: sum
  description: Blockchain RPC requests.
  dimensions:
  - project_id
  - chain
  name: rpc_requests
  unit: request
name: Reown Finops
provider_name: Reown
provider_slug: reown
publisher_name: Reown (WalletConnect Inc.)
service_category: Web3
slug: reown-finops
source_filename: reown-finops.yml
source_heading: FinOps Profile
source_url: https://reown.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Reown\nproviderId: reown\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Wallets\n- WalletConnect\n- AppKit\n- RPC\n- FinOps\n- FOCUS\ndescription: Reown bills as monthly subscription plus MAW-based overages on production\n  usage. Notify push messages may be metered separately.\nnotes: Invoiced via Reown.\nsources:\n- https://reown.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Reown (WalletConnect Inc.)\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + MAW\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n\
  focusColumns:\n  ServiceName: Reown\n  ServiceCategory: Web3\n  ProviderName: Reown\n  PublisherName: Reown\n  InvoiceIssuerName: Reown\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: monthly_active_wallets\n  description: Distinct wallet sessions per month.\n  unit: wallet\n  aggregation: count_distinct\n  dimensions:\n  - project_id\n- name: notify_messages\n  description: Notify push messages sent.\n  unit: message\n  aggregation: sum\n  dimensions:\n  - project_id\n- name: rpc_requests\n  description: Blockchain RPC requests.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - project_id\n  - chain\nprinciples:\n- name: Visibility\n  description: Reown dashboard surfaces MAW and Notify usage.\n- name: Allocation\n  description: One projectId per app/environment.\n- name: Optimization\n  description: Use AppKit's built-in caching; avoid redundant RPC calls.\n- name: Accountability\n  description: Project owners review usage.\nmaintainers:\n- FN: Kin Lane\n  email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/reown/refs/heads/main/finops/reown-finops.yml
sources:
- https://reown.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Wallets
- WalletConnect
- AppKit
- RPC
- FinOps
- FOCUS
---
