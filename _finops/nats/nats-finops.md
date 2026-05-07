---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: nats-monitoring-api-openapi.yml
  format: yaml
  label: NATS Monitoring API
  slug: nats-monitoring-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/nats/refs/heads/main/properties/nats-monitoring-api-openapi.yml
- filename: nats-messaging-asyncapi.yml
  format: yaml
  label: NATS Messaging API
  slug: nats-messaging-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/nats/refs/heads/main/properties/nats-messaging-asyncapi.yml
- filename: nats-jetstream-api-asyncapi.yml
  format: yaml
  label: NATS JetStream Management API
  slug: nats-jetstream-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/nats/refs/heads/main/properties/nats-jetstream-api-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Tiered Subscription + Add-ons
description: 'FOCUS-aligned FinOps for NATS: open-source server is free; commercial billing flows through Synadia Cloud as a tiered subscription with quota-based add-ons (connections, leaf nodes, storage, HA storage).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Synadia Communications, Inc.
  PricingCategory: Subscription
  PricingUnit: month
  ProviderName: Synadia
  PublisherName: Synadia Communications, Inc.
  ServiceCategory: Messaging
  ServiceName: NATS / Synadia Cloud
  ServiceSubcategory: Pub-Sub Streaming
layout: finops
meters:
- aggregation: sum
  description: Monthly Synadia Cloud Team subscription (Personal/Starter/Pro/Premium/Enterprise).
  dimensions:
  - tier
  - team
  name: team_subscription
  unit: month
- aggregation: max
  description: Concurrent NATS client connections; capped per tier.
  dimensions:
  - team
  - account
  name: connections
  unit: connection
- aggregation: max
  description: Active subject subscriptions; capped per tier.
  dimensions:
  - team
  - account
  name: subscriptions
  unit: subscription
- aggregation: sum
  description: Outbound message bytes counted against tier network-data quota.
  dimensions:
  - team
  - account
  name: network_data
  unit: GB
- aggregation: avg
  description: JetStream standard storage consumed.
  dimensions:
  - team
  - account
  - stream
  name: storage_gb_month
  unit: GB-month
- aggregation: avg
  description: JetStream high-availability (replicated) storage consumed.
  dimensions:
  - team
  - account
  - stream
  name: ha_storage_gb_month
  unit: GB-month
- aggregation: max
  description: Active leaf-node connections; charged per extra leaf node beyond tier inclusion.
  dimensions:
  - team
  name: leaf_nodes
  unit: leaf_node
- aggregation: sum
  description: 10-connection add-on packs.
  dimensions:
  - team
  name: connectivity_packs
  unit: pack
name: Nats Finops
provider_name: NATS
provider_slug: nats
publisher_name: Synadia Communications, Inc.
service_category: Messaging + Streaming
slug: nats-finops
source_filename: nats-finops.yml
source_heading: FinOps Profile
source_url: https://www.synadia.com/cloud
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: NATS\nproviderId: nats\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Message Broker\n  - Streaming\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for NATS: open-source server is free; commercial billing flows through\n  Synadia Cloud as a tiered subscription with quota-based add-ons (connections, leaf nodes, storage, HA\n  storage).'\nsources:\n  - https://www.synadia.com/cloud\n  - https://docs.synadia.com/cloud/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Synadia Communications, Inc.\nserviceCategory: Messaging + Streaming\nbillingModel:\n  pricingCategory: Tiered Subscription + Add-ons\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: NATS / Synadia Cloud\n  ServiceCategory: Messaging\n  ServiceSubcategory: Pub-Sub Streaming\n  ProviderName: Synadia\n  PublisherName: Synadia Communications, Inc.\n  InvoiceIssuerName: Synadia Communications, Inc.\n  BillingCurrency: USD\n  PricingCategory: Subscription\n  PricingUnit: month\nmeters:\n  - name: team_subscription\n    description: Monthly Synadia Cloud Team subscription (Personal/Starter/Pro/Premium/Enterprise).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - team\n  - name: connections\n    description: Concurrent NATS client connections; capped per tier.\n    unit: connection\n    aggregation: max\n    dimensions:\n      - team\n      - account\n  - name: subscriptions\n    description: Active subject subscriptions; capped per tier.\n    unit: subscription\n    aggregation: max\n \
  \   dimensions:\n      - team\n      - account\n  - name: network_data\n    description: Outbound message bytes counted against tier network-data quota.\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - team\n      - account\n  - name: storage_gb_month\n    description: JetStream standard storage consumed.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - team\n      - account\n      - stream\n  - name: ha_storage_gb_month\n    description: JetStream high-availability (replicated) storage consumed.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - team\n      - account\n      - stream\n  - name: leaf_nodes\n    description: Active leaf-node connections; charged per extra leaf node beyond tier inclusion.\n    unit: leaf_node\n    aggregation: max\n    dimensions:\n      - team\n  - name: connectivity_packs\n    description: 10-connection add-on packs.\n    unit: pack\n    aggregation: sum\n    dimensions:\n      - team\nprinciples:\n  - name:\
  \ Visibility\n    description: Use the Synadia Control Plane dashboard and `nsc describe` plus the NATS monitoring HTTP\n      endpoints (varz, accountz, jsz) to attribute connections, subscriptions, and JetStream storage by\n      account and stream.\n  - name: Allocation\n    description: Map Synadia Teams and NATS Accounts to internal cost centers; tag streams and KV buckets\n      with team metadata so JetStream storage rolls up correctly.\n  - name: Optimization\n    description: Right-size tier (Starter vs Pro vs Premium) based on actual concurrent connection peak;\n      consolidate low-volume accounts to share quota; prefer standard storage over HA where consistency\n      requirements allow; consider self-hosting OSS NATS for predictable, high-volume workloads.\n  - name: Accountability\n    description: Set monthly Synadia Cloud spend ceilings per Team; alert on connection or network-data\n      utilization above 80% of tier quota to avoid quota-exceeded incidents and unplanned\
  \ upgrades.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nats/refs/heads/main/finops/nats-finops.yml
sources:
- https://www.synadia.com/cloud
- https://docs.synadia.com/cloud/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Message Broker
- Streaming
- Cost Management
---
