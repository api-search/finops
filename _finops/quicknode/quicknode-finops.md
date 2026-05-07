---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: quicknode-ipfs-openapi.yml
  format: yaml
  label: QuickNode IPFS API
  slug: ipfs
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-ipfs-openapi.yml
- filename: quicknode-streams-openapi.yml
  format: yaml
  label: QuickNode Streams API
  slug: streams
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-streams-openapi.yml
- filename: quicknode-key-value-store-openapi.yml
  format: yaml
  label: QuickNode Key-Value Store API
  slug: key-value-store
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/openapi/quicknode-key-value-store-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go Overage
description: FOCUS-aligned FinOps for QuickNode - flat monthly subscription per tier plus a per-million-credit overage charge driven by method-weighted RPC consumption.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: QuickNode Labs, Inc.
  ProviderName: QuickNode
  PublisherName: QuickNode Labs, Inc.
  ServiceCategory: Blockchain Infrastructure
  ServiceName: QuickNode
layout: finops
meters:
- aggregation: sum
  description: Recurring monthly or annual plan fee for the active QuickNode tier (Build, Accelerate, Scale, Business, or Enterprise).
  dimensions:
  - plan_tier
  - billing_cycle
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Method-weighted credits consumed by RPC, REST, and gRPC requests against the QuickNode endpoint.
  dimensions:
  - endpoint_id
  - chain
  - method
  - plan_tier
  name: api_credits
  unit: credit
- aggregation: sum
  description: Credits consumed beyond the included monthly credit allowance for the active plan; billed per million credits at the plan-specific overage rate.
  dimensions:
  - endpoint_id
  - chain
  - plan_tier
  name: credit_overage
  unit: credit
- aggregation: max
  description: Active dedicated endpoints provisioned on the account; each plan caps the number permitted.
  dimensions:
  - chain
  - region
  name: endpoints
  unit: endpoint
- aggregation: sum
  description: Marketplace add-on consumption (e.g. Streams, Webhooks, IPFS pinning, Key-Value Store operations) billed by the add-on's own meter.
  dimensions:
  - addon_name
  - endpoint_id
  name: addon_usage
  unit: varies
name: Quicknode Finops
provider_name: QuickNode
provider_slug: quicknode
publisher_name: QuickNode Labs, Inc.
service_category: Blockchain Infrastructure
slug: quicknode-finops
source_filename: quicknode-finops.yml
source_heading: FinOps Profile
source_url: https://www.quicknode.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: QuickNode\nproviderId: quicknode\npublisherName: QuickNode Labs, Inc.\nserviceCategory: Blockchain Infrastructure\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Blockchain\n  - Web3\n  - RPC\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for QuickNode - flat monthly subscription per tier plus a per-million-credit\n  overage charge driven by method-weighted RPC consumption.\nsources:\n  - https://www.quicknode.com/pricing\n  - https://www.quicknode.com/docs/welcome\nbillingModel:\n  pricingCategory: Subscription + Pay-As-You-Go Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: QuickNode\n  ServiceCategory: Blockchain Infrastructure\n  ProviderName: QuickNode\n  PublisherName: QuickNode Labs, Inc.\n  InvoiceIssuerName: QuickNode Labs, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: subscription_fee\n    description: Recurring monthly or annual plan fee for the active QuickNode tier (Build, Accelerate,\n      Scale, Business, or Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_cycle\n  - name: api_credits\n    description: Method-weighted credits consumed by RPC, REST, and gRPC requests against the QuickNode\n      endpoint.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - endpoint_id\n      - chain\n      - method\n      - plan_tier\n  - name: credit_overage\n    description: Credits consumed beyond the included monthly credit allowance for the active plan;\n \
  \     billed per million credits at the plan-specific overage rate.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - endpoint_id\n      - chain\n      - plan_tier\n  - name: endpoints\n    description: Active dedicated endpoints provisioned on the account; each plan caps the number permitted.\n    unit: endpoint\n    aggregation: max\n    dimensions:\n      - chain\n      - region\n  - name: addon_usage\n    description: Marketplace add-on consumption (e.g. Streams, Webhooks, IPFS pinning, Key-Value Store\n      operations) billed by the add-on's own meter.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - addon_name\n      - endpoint_id\nprinciples:\n  - name: Visibility\n    description: Use the QuickNode dashboard to observe credit consumption per endpoint and per method;\n      method-level breakdowns highlight which RPC calls (trace_, debug_, archive) dominate spend.\n  - name: Allocation\n    description: Provision separate endpoints per consuming\
  \ team, environment, or chain so credit usage\n      and overage charges can be attributed; enterprise dedicated clusters allow per-tenant cost isolation.\n  - name: Optimization\n    description: Cache idempotent reads at the application or CDN tier, prefer batched JSON-RPC where\n      supported, choose a tier whose included credit allowance matches steady-state consumption to avoid\n      the overage rate, and configure method-level rate limits on Accelerate and above to cap expensive\n      methods.\n  - name: Accountability\n    description: Track subscription tier and overage charges separately; the platform bills overages\n      that exceed $200 in-month immediately on Build and above, so set spend alerts proactively. Enterprise\n      tenants negotiate dedicated cluster commitments and SOC2 attestation as part of the contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/quicknode/refs/heads/main/finops/quicknode-finops.yml
sources:
- https://www.quicknode.com/pricing
- https://www.quicknode.com/docs/welcome
specification: FinOps Framework
tags:
- Blockchain
- Web3
- RPC
- FinOps
- FOCUS
---
