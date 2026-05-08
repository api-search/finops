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
description: Magic bills as monthly subscription with MAW-based overages. Server wallet operations and Magic Connect features may have separate metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Magic Labs
  ProviderName: Magic
  PublisherName: Magic Labs
  ServiceCategory: Web3
  ServiceName: Magic
layout: finops
meters:
- aggregation: count_distinct
  description: Distinct wallets active per month.
  dimensions:
  - app
  name: monthly_active_wallets
  unit: wallet
- aggregation: sum
  description: Authentication requests handled.
  dimensions:
  - app
  - method
  name: auth_requests
  unit: request
name: Magic Link Finops
provider_name: Magic
provider_slug: magic-link
publisher_name: Magic Labs, Inc.
service_category: Web3
slug: magic-link-finops
source_filename: magic-link-finops.yml
source_heading: FinOps Profile
source_url: https://magic.link/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Magic\nproviderId: magic-link\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Wallets\n- Authentication\n- Embedded Wallets\n- MPC\n- FinOps\n- FOCUS\ndescription: Magic bills as monthly subscription with MAW-based overages. Server wallet\n  operations and Magic Connect features may have separate metering.\nnotes: Invoiced via Magic Labs.\nsources:\n- https://magic.link/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Magic Labs, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + MAW\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: Magic\n  ServiceCategory: Web3\n  ProviderName: Magic\n  PublisherName: Magic Labs\n  InvoiceIssuerName: Magic Labs\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: monthly_active_wallets\n  description: Distinct wallets active per month.\n  unit: wallet\n  aggregation: count_distinct\n  dimensions:\n  - app\n- name: auth_requests\n  description: Authentication requests handled.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app\n  - method\nprinciples:\n- name: Visibility\n  description: Magic dashboard surfaces MAW and auth events.\n- name: Allocation\n  description: One Magic app per product/environment.\n- name: Optimization\n  description: Use session refresh to reduce repeat auth calls.\n- name: Accountability\n  description: App owners review MAW vs plan.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/magic-link/refs/heads/main/finops/magic-link-finops.yml
sources:
- https://magic.link/pricing
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
