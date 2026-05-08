---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hiro-stacks-blockchain-api-openapi.yaml
  format: yaml
  label: Stacks Blockchain API
  slug: stacks-blockchain-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hiro/refs/heads/main/openapi/hiro-stacks-blockchain-api-openapi.yaml
- filename: hiro-stacks-node-rpc-api-openapi.yaml
  format: yaml
  label: Stacks Node RPC API
  slug: stacks-node-rpc
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hiro/refs/heads/main/openapi/hiro-stacks-node-rpc-api-openapi.yaml
- filename: hiro-token-metadata-api-openapi.yaml
  format: yaml
  label: Hiro Token Metadata API
  slug: token-metadata-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hiro/refs/heads/main/openapi/hiro-token-metadata-api-openapi.yaml
- filename: hiro-signer-metrics-api-openapi.yaml
  format: yaml
  label: Hiro Signer Metrics API
  slug: signer-metrics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hiro/refs/heads/main/openapi/hiro-signer-metrics-api-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Free + Subscription
description: Hiro public APIs are free; paid usage flows through the Hiro Platform subscription.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Hiro Systems
  ProviderName: Hiro
  PublisherName: Hiro Systems
  ServiceCategory: Web3
  ServiceName: Hiro
layout: finops
meters:
- aggregation: sum
  description: Stacks API request count.
  dimensions:
  - api_key
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Chainhook events delivered.
  dimensions:
  - predicate
  name: chainhook_events
  unit: event
- aggregation: sum
  description: Managed devnet runtime hours.
  dimensions:
  - devnet
  name: devnet_hours
  unit: hour
name: Hiro Finops
provider_name: Hiro
provider_slug: hiro
publisher_name: Hiro Systems PBC
service_category: Web3
slug: hiro-finops
source_filename: hiro-finops.yml
source_heading: FinOps Profile
source_url: https://www.hiro.so/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hiro\nproviderId: hiro\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- Bitcoin\n- Stacks\n- sBTC\n- Indexing\n- FinOps\n- FOCUS\ndescription: Hiro public APIs are free; paid usage flows through the Hiro Platform\n  subscription.\nnotes: Bills issued by Hiro Systems for the Platform.\nsources:\n- https://www.hiro.so/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hiro Systems PBC\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Free + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName:\
  \ Hiro\n  ServiceCategory: Web3\n  ProviderName: Hiro\n  PublisherName: Hiro Systems\n  InvoiceIssuerName: Hiro Systems\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_requests\n  description: Stacks API request count.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - api_key\n  - endpoint\n- name: chainhook_events\n  description: Chainhook events delivered.\n  unit: event\n  aggregation: sum\n  dimensions:\n  - predicate\n- name: devnet_hours\n  description: Managed devnet runtime hours.\n  unit: hour\n  aggregation: sum\n  dimensions:\n  - devnet\nprinciples:\n- name: Visibility\n  description: Monitor API usage in the Hiro Platform dashboard.\n- name: Allocation\n  description: Tag projects/devnets per team.\n- name: Optimization\n  description: Use chainhooks instead of polling; cache token metadata.\n- name: Accountability\n  description: Project owners review monthly usage.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hiro/refs/heads/main/finops/hiro-finops.yml
sources:
- https://www.hiro.so/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- Bitcoin
- Stacks
- sBTC
- Indexing
- FinOps
- FOCUS
---
