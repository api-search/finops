---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: moralis-evm-api-openapi.json
  format: json
  label: Moralis EVM API
  slug: evm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/moralis/refs/heads/main/openapi/moralis-evm-api-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Subscription + Usage
description: Moralis bills as subscription + CU usage. Streams events and Datashare exports are metered separately.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Moralis
  ProviderName: Moralis
  PublisherName: Moralis
  ServiceCategory: Web3
  ServiceName: Moralis
layout: finops
meters:
- aggregation: sum
  description: Data API CUs.
  dimensions:
  - api_key
  - chain
  - endpoint
  name: compute_units
  unit: CU
- aggregation: sum
  description: Streams events delivered.
  dimensions:
  - stream
  - chain
  name: stream_events
  unit: event
name: Moralis Finops
provider_name: Moralis
provider_slug: moralis
publisher_name: Moralis Web3 Technology AB
service_category: Web3
slug: moralis-finops
source_filename: moralis-finops.yml
source_heading: FinOps Profile
source_url: https://moralis.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Moralis\nproviderId: moralis\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- Blockchain\n- Data API\n- Streams\n- Indexing\n- FinOps\n- FOCUS\ndescription: Moralis bills as subscription + CU usage. Streams events and Datashare\n  exports are metered separately.\nnotes: Usage in dashboard.\nsources:\n- https://moralis.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Moralis Web3 Technology AB\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n\
  \  ServiceName: Moralis\n  ServiceCategory: Web3\n  ProviderName: Moralis\n  PublisherName: Moralis\n  InvoiceIssuerName: Moralis\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: compute_units\n  description: Data API CUs.\n  unit: CU\n  aggregation: sum\n  dimensions:\n  - api_key\n  - chain\n  - endpoint\n- name: stream_events\n  description: Streams events delivered.\n  unit: event\n  aggregation: sum\n  dimensions:\n  - stream\n  - chain\nprinciples:\n- name: Visibility\n  description: Use Moralis dashboard; export usage CSVs.\n- name: Allocation\n  description: One API key per service/team for attribution.\n- name: Optimization\n  description: Cache responses; restrict chains in queries; use Streams instead of\n    polling.\n- name: Accountability\n  description: API key owners review monthly CU vs plan.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moralis/refs/heads/main/finops/moralis-finops.yml
sources:
- https://moralis.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- Blockchain
- Data API
- Streams
- Indexing
- FinOps
- FOCUS
---
