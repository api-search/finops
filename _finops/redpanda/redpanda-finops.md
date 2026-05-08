---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: redpanda-admin-cluster-openapi.json
  format: json
  label: Redpanda Admin API
  slug: redpanda-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/redpanda/refs/heads/main/openapi/redpanda-admin-cluster-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  billingTerm: Hourly metering with monthly invoice; annual term available
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  - Tax
  commitmentDiscount: Reserved-capacity / annual prepay discount on Cloud Dedicated and Enterprise.
  pricingCategory: Hybrid Subscription, Usage-Based, and Open-Source
description: Redpanda has a hybrid billing surface. The open-source Community Edition (BSL 1.1) generates no Redpanda invoice; cost flows through the operator's own cloud bill (compute, storage, networking). Redpanda Cloud Serverless bills usage-based (no base fee, $100 trial credit). Cloud Dedicated and BYOC are committed/throughput-tier subscriptions with separate charges for tiered storage, networking, and PrivateLink. BYOC additionally produces cloud-provider charges directly to the customer's AWS/GCP/Azure account, with Redpanda only invoicing a management fee. Self-managed Enterprise carries an annual license fee.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Redpanda Data
  PricingCategory: Standard Pricing
  ProviderName: Redpanda Data
  PublisherName: Redpanda Data
  ServiceCategory: Streaming
  ServiceName: Redpanda Cloud
layout: finops
meters:
- aggregation: sum
  description: Per-cluster active-hours billed by tier (Serverless, Dedicated tiers).
  dimensions:
  - organization
  - cluster
  - tier
  - region
  name: cluster_hours
  unit: cluster-hour
- aggregation: sum
  description: Bytes produced into Redpanda Cloud (Serverless usage-based component).
  dimensions:
  - organization
  - cluster
  - tenant
  name: ingress_bytes
  unit: byte
- aggregation: sum
  description: Bytes consumed from Redpanda Cloud (cross-AZ / cross-region egress may carry cloud-provider charges).
  dimensions:
  - organization
  - cluster
  - tenant
  - direction
  name: egress_bytes
  unit: byte
- aggregation: max
  description: Total partitions held by the cluster (Serverless / Dedicated quota element).
  dimensions:
  - organization
  - cluster
  name: partition_count
  unit: partition-month
- aggregation: max
  description: Storage used by tiered/object-storage retention.
  dimensions:
  - organization
  - cluster
  - storage_class
  name: tiered_storage_gb
  unit: gb-month
- aggregation: sum
  description: Active AWS PrivateLink / GCP PSC endpoint hours.
  dimensions:
  - organization
  - cluster
  - cloud
  name: privatelink_endpoints
  unit: endpoint-hour
- aggregation: max
  description: Per-cluster monthly management fee for BYOC deployments (cloud infrastructure billed separately to customer cloud account).
  dimensions:
  - organization
  - cluster
  - tier
  name: byoc_management_fee
  unit: cluster-month
- aggregation: max
  description: Self-managed Enterprise annual license, custom-quoted by capacity.
  dimensions:
  - customer
  - capacity
  name: enterprise_license
  unit: license-year
name: Redpanda Finops
provider_name: Redpanda
provider_slug: redpanda
publisher_name: Redpanda Data
service_category: Streaming
slug: redpanda-finops
source_filename: redpanda-finops.yml
source_heading: FinOps Profile
source_url: https://www.redpanda.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Redpanda\nproviderId: redpanda\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Streaming\n  - Kafka\n  - Event Streaming\n  - Open Source\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  Redpanda has a hybrid billing surface. The open-source Community Edition (BSL 1.1) generates no Redpanda invoice; cost flows through the operator's own cloud bill (compute, storage, networking). Redpanda Cloud Serverless bills usage-based (no base fee, $100 trial credit). Cloud Dedicated and BYOC are committed/throughput-tier subscriptions with separate charges for tiered storage, networking, and PrivateLink. BYOC additionally produces cloud-provider charges directly to the customer's AWS/GCP/Azure account, with Redpanda only invoicing a management fee. Self-managed Enterprise carries an annual license fee.\nnotes: >-\n  Reconciled at\
  \ the model level on 2026-05-08. Per-tier hourly rates for Dedicated/BYOC are quoted by Redpanda sales; the customer-facing price-estimator on redpanda.com produces project-specific quotes. No public FOCUS-format usage feed exists; usage data is available via the Cloud Console and contractual usage reports.\nsources:\n  - https://www.redpanda.com/pricing\n  - https://www.redpanda.com/redpanda-cloud\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Redpanda Data\nserviceCategory: Streaming\nbillingModel:\n  pricingCategory: Hybrid Subscription, Usage-Based, and Open-Source\n  billingFrequency: Monthly\n  billingTerm: Hourly metering with monthly invoice; annual term available\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n\
  \    - Adjustment\n    - Tax\n  commitmentDiscount: Reserved-capacity / annual prepay discount on Cloud Dedicated and Enterprise.\nfocusColumns:\n  ServiceName: Redpanda Cloud\n  ServiceCategory: Streaming\n  ProviderName: Redpanda Data\n  PublisherName: Redpanda Data\n  InvoiceIssuerName: Redpanda Data\n  BillingCurrency: USD\n  ChargeCategory: Subscription\n  PricingCategory: Standard Pricing\nmeters:\n  - name: cluster_hours\n    description: Per-cluster active-hours billed by tier (Serverless, Dedicated tiers).\n    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - organization\n      - cluster\n      - tier\n      - region\n  - name: ingress_bytes\n    description: Bytes produced into Redpanda Cloud (Serverless usage-based component).\n    unit: byte\n    aggregation: sum\n    dimensions:\n      - organization\n      - cluster\n      - tenant\n  - name: egress_bytes\n    description: Bytes consumed from Redpanda Cloud (cross-AZ / cross-region egress may carry cloud-provider\
  \ charges).\n    unit: byte\n    aggregation: sum\n    dimensions:\n      - organization\n      - cluster\n      - tenant\n      - direction\n  - name: partition_count\n    description: Total partitions held by the cluster (Serverless / Dedicated quota element).\n    unit: partition-month\n    aggregation: max\n    dimensions:\n      - organization\n      - cluster\n  - name: tiered_storage_gb\n    description: Storage used by tiered/object-storage retention.\n    unit: gb-month\n    aggregation: max\n    dimensions:\n      - organization\n      - cluster\n      - storage_class\n  - name: privatelink_endpoints\n    description: Active AWS PrivateLink / GCP PSC endpoint hours.\n    unit: endpoint-hour\n    aggregation: sum\n    dimensions:\n      - organization\n      - cluster\n      - cloud\n  - name: byoc_management_fee\n    description: Per-cluster monthly management fee for BYOC deployments (cloud infrastructure billed separately to customer cloud account).\n    unit: cluster-month\n\
  \    aggregation: max\n    dimensions:\n      - organization\n      - cluster\n      - tier\n  - name: enterprise_license\n    description: Self-managed Enterprise annual license, custom-quoted by capacity.\n    unit: license-year\n    aggregation: max\n    dimensions:\n      - customer\n      - capacity\nprinciples:\n  - name: Visibility\n    description: >-\n      Use the Redpanda Cloud Console for usage and invoice details. For BYOC, pair the Redpanda invoice with cost-allocation tags pulled from the customer's cloud bill (FOCUS-formatted exports from AWS/GCP/Azure cover the underlying infrastructure).\n  - name: Allocation\n    description: >-\n      Tag clusters by environment and business unit; on Cloud Serverless, dedicate clusters per tenant for clean attribution. For self-hosted, tag the underlying compute, EBS volumes, and S3 buckets used for tiered storage.\n  - name: Optimization\n    description: >-\n      Use tiered storage to cut hot-storage cost (8-9x savings claimed);\
  \ enable compression and right-size partitions; consolidate idle Serverless clusters; consider BYOC for very large workloads to leverage cloud committed-use discounts.\n  - name: Accountability\n    description: >-\n      Assign a cluster owner per environment; review monthly forecast versus invoice; alert on partition-count, ingress-throughput, and tiered-storage growth as leading cost indicators.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/redpanda/refs/heads/main/finops/redpanda-finops.yml
sources:
- https://www.redpanda.com/pricing
- https://www.redpanda.com/redpanda-cloud
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Streaming
- Kafka
- Event Streaming
- Open Source
- FinOps
- Cost Management
- FOCUS
---
