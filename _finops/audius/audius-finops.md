---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: N/A
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Free / Self-Host
description: FOCUS-aligned FinOps profile for Audius. The protocol is decentralized, open-source, and free to consume. There is no invoice from Audius for API usage. Cost only arises if you self-host a content node or discovery node (compute/storage on your infrastructure).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Audius
  ProviderName: Audius
  PublisherName: Audius
  ServiceCategory: Music Streaming
  ServiceName: Audius API
layout: finops
meters:
- aggregation: sum
  description: API requests served by network discovery nodes (free; no charge).
  dimensions:
  - app_name
  - host
  name: api_requests
  unit: request
name: Audius Finops
provider_name: Audius
provider_slug: audius
publisher_name: Audius
service_category: Music Streaming
slug: audius-finops
source_filename: audius-finops.yml
source_heading: FinOps Profile
source_url: https://docs.audius.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Audius\nproviderId: audius\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Music\n- Streaming\n- Decentralized\n- Web3\n- Open Source\n- Blockchain\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Audius. The protocol is decentralized, open-source, and free to\n  consume. There is no invoice from Audius for API usage. Cost only arises if you self-host a content\n  node or discovery node (compute/storage on your infrastructure).\nnotes: Zero direct cost for API consumers; only self-hosting a node has cost (your own infra).\nsources:\n- https://docs.audius.org/\n- https://github.com/AudiusProject\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Audius\nserviceCategory: Music Streaming\nbillingModel:\n  pricingCategory: Free / Self-Host\n  billingFrequency: N/A\n  billingCurrency: N/A\n  chargeCategories:\n  - Usage\nfocusColumns:\n  ServiceName: Audius API\n  ServiceCategory: Music Streaming\n  ProviderName: Audius\n  PublisherName: Audius\n  InvoiceIssuerName: Audius\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_requests\n  description: API requests served by network discovery nodes (free; no charge).\n  unit: request\n  aggregation: sum\n  dimensions:\n  - app_name\n  - host\nprinciples:\n- name: Visibility\n  description: No invoice; track API usage in your own logs for performance tuning.\n- name: Allocation\n  description: If self-hosting nodes, allocate compute/storage to your team.\n- name: Optimization\n  description: Use the SDK's caching and host rotation to reduce per-host load.\n- name: Accountability\n  description: API consumers have no cost accountability; node operators\
  \ do.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/audius/refs/heads/main/finops/audius-finops.yml
sources:
- https://docs.audius.org/
- https://github.com/AudiusProject
specification: FinOps Framework
tags:
- Music
- Streaming
- Decentralized
- Web3
- Open Source
- Blockchain
- FinOps
- Cost Management
- FOCUS
---
