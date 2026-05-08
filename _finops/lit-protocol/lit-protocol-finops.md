---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lit-protocol-core-v1-openapi.json
  format: json
  label: Lit Protocol Chipotle Express API (Core v1)
  slug: chipotle-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lit-protocol/refs/heads/main/openapi/lit-protocol-core-v1-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: On Top-up
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Prepaid Credits
description: Lit Protocol bills as a prepaid credit balance. FinOps levers focus on credit consumption per Lit Action and sign operation.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lit Protocol
  ProviderName: Lit Protocol
  PublisherName: Lit Protocol
  ServiceCategory: Web3
  ServiceName: Lit Protocol
layout: finops
meters:
- aggregation: sum
  description: Credits consumed per operation.
  dimensions:
  - api_key
  - operation
  name: credits_consumed
  unit: credit
- aggregation: sum
  description: Lit Action executions.
  dimensions:
  - account
  - ipfs_id
  name: lit_action_executions
  unit: execution
name: Lit Protocol Finops
provider_name: Lit Protocol
provider_slug: lit-protocol
publisher_name: Lit Protocol Inc.
service_category: Web3
slug: lit-protocol-finops
source_filename: lit-protocol-finops.yml
source_heading: FinOps Profile
source_url: https://developer.litprotocol.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lit Protocol\nproviderId: lit-protocol\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Key Management\n- MPC\n- Programmable Keys\n- Lit Actions\n- FinOps\n- FOCUS\ndescription: Lit Protocol bills as a prepaid credit balance. FinOps levers focus on\n  credit consumption per Lit Action and sign operation.\nnotes: Add Funds via dashboard; usage history visible there.\nsources:\n- https://developer.litprotocol.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lit Protocol Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Prepaid Credits\n  billingFrequency: On Top-up\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Purchase\n  - Usage\nfocusColumns:\n  ServiceName: Lit Protocol\n  ServiceCategory: Web3\n  ProviderName: Lit Protocol\n  PublisherName: Lit Protocol\n  InvoiceIssuerName: Lit Protocol\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: credits_consumed\n  description: Credits consumed per operation.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - api_key\n  - operation\n- name: lit_action_executions\n  description: Lit Action executions.\n  unit: execution\n  aggregation: sum\n  dimensions:\n  - account\n  - ipfs_id\nprinciples:\n- name: Visibility\n  description: Use the Lit dashboard usage view.\n- name: Allocation\n  description: API key per app/environment.\n- name: Optimization\n  description: Cache decrypted material client-side; minimize PKP signs; prefer batched\n    Lit Actions.\n- name: Accountability\n  description: Account owner monitors prepaid balance and refills.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lit-protocol/refs/heads/main/finops/lit-protocol-finops.yml
sources:
- https://developer.litprotocol.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Key Management
- MPC
- Programmable Keys
- Lit Actions
- FinOps
- FOCUS
---
