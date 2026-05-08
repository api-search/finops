---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/GRT
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Pay-per-Query
description: The Graph bills query consumption per 100k queries in USD or GRT. Substreams bill on data egress; Token API bills per request.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The Graph
  ProviderName: The Graph
  PublisherName: Edge & Node
  ServiceCategory: Web3
  ServiceName: The Graph
layout: finops
meters:
- aggregation: sum
  description: GraphQL queries against subgraphs.
  dimensions:
  - api_key
  - subgraph
  name: subgraph_queries
  unit: query
- aggregation: sum
  description: Token API REST requests.
  dimensions:
  - api_key
  - endpoint
  name: token_api_requests
  unit: request
- aggregation: sum
  description: Substream gRPC bytes streamed.
  dimensions:
  - substream
  name: substream_egress
  unit: byte
name: The Graph Finops
provider_name: The Graph
provider_slug: the-graph
publisher_name: The Graph (Edge & Node)
service_category: Web3
slug: the-graph-finops
source_filename: the-graph-finops.yml
source_heading: FinOps Profile
source_url: https://thegraph.com/billing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: The Graph\nproviderId: the-graph\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Indexing\n- GraphQL\n- Subgraphs\n- Multi-chain\n- FinOps\n- FOCUS\ndescription: The Graph bills query consumption per 100k queries in USD or GRT. Substreams\n  bill on data egress; Token API bills per request.\nnotes: Invoiced via Edge & Node / Subgraph Studio billing.\nsources:\n- https://thegraph.com/billing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Graph (Edge & Node)\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Pay-per-Query\n  billingFrequency: Monthly\n  billingCurrency: USD/GRT\n\
  \  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName: The Graph\n  ServiceCategory: Web3\n  ProviderName: The Graph\n  PublisherName: Edge & Node\n  InvoiceIssuerName: The Graph\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subgraph_queries\n  description: GraphQL queries against subgraphs.\n  unit: query\n  aggregation: sum\n  dimensions:\n  - api_key\n  - subgraph\n- name: token_api_requests\n  description: Token API REST requests.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - api_key\n  - endpoint\n- name: substream_egress\n  description: Substream gRPC bytes streamed.\n  unit: byte\n  aggregation: sum\n  dimensions:\n  - substream\nprinciples:\n- name: Visibility\n  description: Subgraph Studio billing dashboard tracks queries by API key.\n- name: Allocation\n  description: API key per app/team.\n- name: Optimization\n  description: Cache GraphQL responses; collapse N+1 queries; choose subgraphs with\n    low query weight.\n- name:\
  \ Accountability\n  description: API key owners review weekly query burn.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/the-graph/refs/heads/main/finops/the-graph-finops.yml
sources:
- https://thegraph.com/billing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Indexing
- GraphQL
- Subgraphs
- Multi-chain
- FinOps
- FOCUS
---
