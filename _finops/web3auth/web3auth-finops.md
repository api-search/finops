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
description: Web3Auth bills as monthly subscription with MAW-based overages.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Web3Auth
  ProviderName: Web3Auth
  PublisherName: Web3Auth
  ServiceCategory: Web3
  ServiceName: Web3Auth
layout: finops
meters:
- aggregation: count_distinct
  description: Distinct wallets active per month.
  dimensions:
  - client_id
  name: monthly_active_wallets
  unit: wallet
name: Web3Auth Finops
provider_name: Web3Auth
provider_slug: web3auth
publisher_name: Web3Auth (Torus Labs / MetaMask)
service_category: Web3
slug: web3auth-finops
source_filename: web3auth-finops.yml
source_heading: FinOps Profile
source_url: https://web3auth.io/pricing.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Web3Auth\nproviderId: web3auth\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Wallets\n- Authentication\n- MPC\n- Embedded Wallets\n- FinOps\n- FOCUS\ndescription: Web3Auth bills as monthly subscription with MAW-based overages.\nnotes: Invoiced via Web3Auth (Torus Labs / MetaMask).\nsources:\n- https://web3auth.io/pricing.html\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Web3Auth (Torus Labs / MetaMask)\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + MAW\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n\
  \  ServiceName: Web3Auth\n  ServiceCategory: Web3\n  ProviderName: Web3Auth\n  PublisherName: Web3Auth\n  InvoiceIssuerName: Web3Auth\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: monthly_active_wallets\n  description: Distinct wallets active per month.\n  unit: wallet\n  aggregation: count_distinct\n  dimensions:\n  - client_id\nprinciples:\n- name: Visibility\n  description: Web3Auth dashboard MAW view.\n- name: Allocation\n  description: One client per product/environment.\n- name: Optimization\n  description: Use long-lived sessions to reduce reauth.\n- name: Accountability\n  description: Project owners review MAW vs plan.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/web3auth/refs/heads/main/finops/web3auth-finops.yml
sources:
- https://web3auth.io/pricing.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Wallets
- Authentication
- MPC
- Embedded Wallets
- FinOps
- FOCUS
---
