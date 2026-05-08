---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: quicknode-streams-openapi.yml
  format: yaml
  label: QuickNode Streams
  slug: streams
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-streams-openapi.yml
- filename: quicknode-ipfs-openapi.yml
  format: yaml
  label: QuickNode IPFS API
  slug: ipfs
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-ipfs-openapi.yml
- filename: quicknode-key-value-store-openapi.yml
  format: yaml
  label: QuickNode Key-Value Store
  slug: kv-store
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-key-value-store-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage
description: QuickNode bills as monthly subscription with included request credits; Marketplace add-ons are metered separately.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: QuickNode
  ProviderName: QuickNode
  PublisherName: QuickNode
  ServiceCategory: Web3
  ServiceName: QuickNode
layout: finops
meters:
- aggregation: sum
  description: Core RPC requests, weighted per method.
  dimensions:
  - endpoint
  - chain
  - method
  name: rpc_requests
  unit: request
- aggregation: sum
  description: Streams events delivered.
  dimensions:
  - stream
  - chain
  name: stream_events
  unit: event
- aggregation: max
  description: IPFS pinned bytes.
  dimensions:
  - account
  name: ipfs_storage
  unit: byte
- aggregation: sum
  description: Marketplace add-on calls.
  dimensions:
  - addon
  name: addon_calls
  unit: request
name: Quicknode Finops
provider_name: QuickNode
provider_slug: quicknode
publisher_name: QuickNode, Inc.
service_category: Web3
slug: quicknode-finops
source_filename: quicknode-finops.yml
source_heading: FinOps Profile
source_url: https://www.quicknode.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: QuickNode\nproviderId: quicknode\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- RPC\n- Streams\n- IPFS\n- Multi-chain\n- FinOps\n- FOCUS\ndescription: QuickNode bills as monthly subscription with included request credits;\n  Marketplace add-ons are metered separately.\nnotes: Usage visible in QuickNode dashboard; invoices via QuickNode.\nsources:\n- https://www.quicknode.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: QuickNode, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: QuickNode\n  ServiceCategory: Web3\n  ProviderName: QuickNode\n  PublisherName: QuickNode\n  InvoiceIssuerName: QuickNode\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: rpc_requests\n  description: Core RPC requests, weighted per method.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - endpoint\n  - chain\n  - method\n- name: stream_events\n  description: Streams events delivered.\n  unit: event\n  aggregation: sum\n  dimensions:\n  - stream\n  - chain\n- name: ipfs_storage\n  description: IPFS pinned bytes.\n  unit: byte\n  aggregation: max\n  dimensions:\n  - account\n- name: addon_calls\n  description: Marketplace add-on calls.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - addon\nprinciples:\n- name: Visibility\n  description: Monitor endpoint usage in the QuickNode dashboard; review per-add-on\n    billing line items.\n- name: Allocation\n  description: Tag endpoints\
  \ by app/team/env.\n- name: Optimization\n  description: Disable unused add-ons; batch requests; prefer Streams over polling.\n- name: Accountability\n  description: Endpoint owners review monthly usage vs allotment.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/finops/quicknode-finops.yml
sources:
- https://www.quicknode.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- RPC
- Streams
- IPFS
- Multi-chain
- FinOps
- FOCUS
---
