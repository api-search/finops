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
  pricingCategory: Subscription + Storage
description: Pinata bills as monthly subscription with included storage and gateway bandwidth, plus per-GB overage.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Pinata
  ProviderName: Pinata
  PublisherName: Pinata
  ServiceCategory: Web3
  ServiceName: Pinata
layout: finops
meters:
- aggregation: max
  description: Bytes pinned to IPFS / Submarine.
  dimensions:
  - account
  - group
  name: pinned_storage
  unit: byte
- aggregation: sum
  description: Dedicated gateway requests served.
  dimensions:
  - gateway
  name: gateway_requests
  unit: request
- aggregation: sum
  description: Dedicated gateway bandwidth.
  dimensions:
  - gateway
  name: gateway_bandwidth
  unit: byte
name: Pinata Finops
provider_name: Pinata
provider_slug: pinata
publisher_name: Pinata Technologies, Inc.
service_category: Web3
slug: pinata-finops
source_filename: pinata-finops.yml
source_heading: FinOps Profile
source_url: https://www.pinata.cloud/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pinata\nproviderId: pinata\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Web3\n- IPFS\n- Storage\n- Gateway\n- FinOps\n- FOCUS\ndescription: Pinata bills as monthly subscription with included storage and gateway\n  bandwidth, plus per-GB overage.\nnotes: Usage in Pinata dashboard.\nsources:\n- https://www.pinata.cloud/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pinata Technologies, Inc.\nserviceCategory: Web3\nbillingModel:\n  pricingCategory: Subscription + Storage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\nfocusColumns:\n  ServiceName:\
  \ Pinata\n  ServiceCategory: Web3\n  ProviderName: Pinata\n  PublisherName: Pinata\n  InvoiceIssuerName: Pinata\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: pinned_storage\n  description: Bytes pinned to IPFS / Submarine.\n  unit: byte\n  aggregation: max\n  dimensions:\n  - account\n  - group\n- name: gateway_requests\n  description: Dedicated gateway requests served.\n  unit: request\n  aggregation: sum\n  dimensions:\n  - gateway\n- name: gateway_bandwidth\n  description: Dedicated gateway bandwidth.\n  unit: byte\n  aggregation: sum\n  dimensions:\n  - gateway\nprinciples:\n- name: Visibility\n  description: Pinata dashboard tracks storage, gateway requests, and bandwidth.\n- name: Allocation\n  description: Use Groups and API keys to attribute pins per app/team.\n- name: Optimization\n  description: Garbage-collect orphaned CIDs; serve through CDN; size files appropriately.\n- name: Accountability\n  description: Account owner reviews monthly bandwidth and storage.\n\
  maintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pinata/refs/heads/main/finops/pinata-finops.yml
sources:
- https://www.pinata.cloud/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Web3
- IPFS
- Storage
- Gateway
- FinOps
- FOCUS
---
