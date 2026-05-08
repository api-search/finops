---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alchemy-token-api-openapi.yml
  format: yaml
  label: Alchemy Token API
  slug: token-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-token-api-openapi.yml
- filename: alchemy-transfers-api-openapi.yml
  format: yaml
  label: Alchemy Transfers API
  slug: transfers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-transfers-api-openapi.yml
- filename: alchemy-gas-manager-api-openapi.yml
  format: yaml
  label: Alchemy Gas Manager API
  slug: gas-manager
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/openapi/alchemy-gas-manager-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage
description: Alchemy bills as monthly subscription plus CU overages on paid plans, with separate metering for Data APIs and Smart Wallets / Bundler usage.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Alchemy
  ProviderName: Alchemy
  PublisherName: Alchemy
  ServiceCategory: Web3
  ServiceName: Alchemy
layout: finops
meters:
- aggregation: sum
  description: RPC compute units consumed per request, weighted per method.
  dimensions:
  - app
  - network
  - method
  name: compute_units
  unit: CU
- aggregation: sum
  description: NFT/Token/Transfers/Portfolio/Prices API requests.
  dimensions:
  - app
  - api
  name: data_api_requests
  unit: request
- aggregation: sum
  description: Gas sponsored via the Gas Manager paymaster.
  dimensions:
  - policy
  - network
  name: gas_sponsored
  unit: wei
name: Alchemy Finops
provider_name: Alchemy
provider_slug: alchemy
publisher_name: Alchemy Insights, Inc.
service_category: Web3
slug: alchemy-finops
source_filename: alchemy-finops.yml
source_heading: FinOps Profile
source_url: https://www.alchemy.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Alchemy\nproviderId: alchemy\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- RPC\n- NFT\n- Indexing\n- Account Abstraction\n- FinOps\n- FOCUS\ndescription: Alchemy bills as monthly subscription plus CU overages on paid plans,\n  with separate metering for Data APIs and Smart Wallets / Bundler usage.\nnotes: Usage exports available via the Alchemy dashboard. No public usage API yet.\nsources:\n- https://www.alchemy.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Alchemy Insights, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Usage\n \
  \ billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: Alchemy\n  ServiceCategory: Web3\n  ProviderName: Alchemy\n  PublisherName: Alchemy\n  InvoiceIssuerName: Alchemy\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: compute_units\n  description: RPC compute units consumed per request, weighted per method.\n  unit: CU\n  aggregation: sum\n  dimensions:\n  - app\n  - network\n  - method\n- name: data_api_requests\n  description: NFT/Token/Transfers/Portfolio/Prices API requests.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app\n  - api\n- name: gas_sponsored\n  description: Gas sponsored via the Gas Manager paymaster.\n  unit: wei\n  aggregation: sum\n  dimensions:\n  - policy\n  - network\nprinciples:\n- name: Visibility\n  description: Use the Alchemy dashboard usage tab and per-app CU breakdown to monitor\n    spend.\n- name: Allocation\n  description: Tag apps per business unit;\
  \ one app per environment to attribute CU.\n- name: Optimization\n  description: Use eth_call batching, archive sparingly, prefer subscriptions over\n    polling, set Compute Budgets.\n- name: Accountability\n  description: Assign app owners; review monthly CU burn against budget.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alchemy/refs/heads/main/finops/alchemy-finops.yml
sources:
- https://www.alchemy.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- RPC
- NFT
- Indexing
- Account Abstraction
- FinOps
- FOCUS
---
