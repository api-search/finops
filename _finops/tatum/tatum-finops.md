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
  pricingCategory: Subscription + Usage
description: Tatum bills as monthly subscription with included credits.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tatum
  ProviderName: Tatum
  PublisherName: Tatum
  ServiceCategory: Web3
  ServiceName: Tatum
layout: finops
meters:
- aggregation: sum
  description: API credits consumed per request.
  dimensions:
  - api_key
  - chain
  - endpoint
  name: credits
  unit: credit
- aggregation: sum
  description: Webhook events delivered.
  dimensions:
  - subscription
  name: webhook_events
  unit: event
name: Tatum Finops
provider_name: Tatum
provider_slug: tatum
publisher_name: Tatum
service_category: Web3
slug: tatum-finops
source_filename: tatum-finops.yml
source_heading: FinOps Profile
source_url: https://tatum.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tatum\nproviderId: tatum\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- RPC\n- Multi-chain\n- Wallet\n- NFT\n- FinOps\n- FOCUS\ndescription: Tatum bills as monthly subscription with included credits.\nnotes: Usage in Tatum dashboard.\nsources:\n- https://tatum.io/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tatum\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: Tatum\n  ServiceCategory: Web3\n  ProviderName:\
  \ Tatum\n  PublisherName: Tatum\n  InvoiceIssuerName: Tatum\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: credits\n  description: API credits consumed per request.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - api_key\n  - chain\n  - endpoint\n- name: webhook_events\n  description: Webhook events delivered.\n  unit: event\n  aggregation: sum\n  dimensions:\n  - subscription\nprinciples:\n- name: Visibility\n  description: Tatum dashboard usage view.\n- name: Allocation\n  description: API key per service/team.\n- name: Optimization\n  description: Use Data API instead of raw RPC for indexed queries.\n- name: Accountability\n  description: API key owners review monthly credits.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tatum/refs/heads/main/finops/tatum-finops.yml
sources:
- https://tatum.io/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- RPC
- Multi-chain
- Wallet
- NFT
- FinOps
- FOCUS
---
