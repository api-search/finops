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
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: FOCUS-aligned FinOps shape for Akamai Technologies. Hybrid cloud platform — Akamai Cloud Computing on a published per-instance / per-GB rate card, plus CDN, edge, and security products on custom contracts with reserved-commitment discounts.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Akamai Technologies, Inc.
  ProviderName: Akamai Technologies
  PublisherName: Akamai Technologies, Inc.
  ServiceCategory: CDN + Edge + Cloud
  ServiceName: Akamai Connected Cloud
layout: finops
meters:
- aggregation: sum
  description: HTTP/S requests served from the Akamai edge
  dimensions:
  - product
  - region
  - cp_code
  name: cdn_requests
  unit: request
- aggregation: sum
  description: Bytes delivered from the Akamai edge to end users
  dimensions:
  - product
  - region
  - cp_code
  name: cdn_egress
  unit: GB
- aggregation: sum
  description: EdgeWorker function invocations
  dimensions:
  - worker
  - region
  name: edgeworker_invocations
  unit: invocation
- aggregation: sum
  description: Akamai Cloud Computing instance-hours
  dimensions:
  - plan
  - region
  - tag
  name: cloud_compute_hours
  unit: instance-hour
- aggregation: sum
  description: Block and Object Storage allocated and consumed
  dimensions:
  - storage_type
  - region
  name: cloud_storage
  unit: GB-month
- aggregation: sum
  description: Network egress beyond bundled allowance
  dimensions:
  - region
  - direction
  name: network_transfer
  unit: GB
- aggregation: sum
  description: WAF / Bot / DDoS rule evaluations and mitigations
  dimensions:
  - product
  - policy
  - severity
  name: security_events
  unit: event
- aggregation: sum
  description: Edge DNS queries served
  dimensions:
  - zone
  - region
  name: dns_queries
  unit: query
name: Akamai Technologies Finops
provider_name: Akamai Technologies
provider_slug: akamai-technologies
publisher_name: Akamai Technologies, Inc.
service_category: CDN + Edge + Cloud
slug: akamai-technologies-finops
source_filename: akamai-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.akamai.com/products/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Akamai Technologies\nproviderId: akamai-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Akamai Technologies, Inc.\nserviceCategory: CDN + Edge + Cloud\ntags:\n  - CDN\n  - Edge\n  - Cloud\n  - Security\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Akamai Technologies. Hybrid cloud platform — Akamai Cloud\n  Computing on a published per-instance / per-GB rate card, plus CDN, edge, and security products on\n  custom contracts with reserved-commitment discounts.\nsources:\n  - https://www.akamai.com/products/pricing\n  - https://www.akamai.com/cloud/pricing\nbillingModel:\n  pricingCategory:\
  \ Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Akamai Connected Cloud\n  ServiceCategory: CDN + Edge + Cloud\n  ProviderName: Akamai Technologies\n  PublisherName: Akamai Technologies, Inc.\n  InvoiceIssuerName: Akamai Technologies, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: cdn_requests\n    description: HTTP/S requests served from the Akamai edge\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - region\n      - cp_code\n  - name: cdn_egress\n    description: Bytes delivered from the Akamai edge to end users\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - product\n      - region\n      - cp_code\n  - name: edgeworker_invocations\n    description: EdgeWorker function invocations\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - worker\n\
  \      - region\n  - name: cloud_compute_hours\n    description: Akamai Cloud Computing instance-hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - plan\n      - region\n      - tag\n  - name: cloud_storage\n    description: Block and Object Storage allocated and consumed\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - storage_type\n      - region\n  - name: network_transfer\n    description: Network egress beyond bundled allowance\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\n  - name: security_events\n    description: WAF / Bot / DDoS rule evaluations and mitigations\n    unit: event\n    aggregation: sum\n    dimensions:\n      - product\n      - policy\n      - severity\n  - name: dns_queries\n    description: Edge DNS queries served\n    unit: query\n    aggregation: sum\n    dimensions:\n      - zone\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Akamai Control Center\
  \ reporting + the Reporting and Billing OPEN APIs for\n      programmatic visibility; on Akamai Cloud Computing, use the Linode billing endpoints. Tag\n      resources with cp_code (CDN / Security) and tags (Cloud Computing) for downstream allocation.\n  - name: Allocation\n    description: Allocate CDN and Security spend by cp_code and property; Cloud Computing by Linode\n      tags and resource group; EdgeWorkers by worker name; Reporting can be sliced per business unit\n      via cp_code grouping.\n  - name: Optimization\n    description: Optimize through committed-use / reserved tiers on CDN traffic and Cloud Computing,\n      right-sizing compute plans, choosing block vs object storage appropriately, leveraging cache-hit\n      ratio improvements to reduce origin egress, and tuning Image/Video Manager output formats.\n  - name: Accountability\n    description: Platform / SRE typically owns Akamai spend with finance partnering on reserved\n      commitments; review reserved tiers ahead\
  \ of contract renewal and after major launches that\n      change traffic baselines.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/akamai-technologies/refs/heads/main/finops/akamai-technologies-finops.yml
sources:
- https://www.akamai.com/products/pricing
- https://www.akamai.com/cloud/pricing
specification: FinOps Framework
tags:
- CDN
- Edge
- Cloud
- Security
- FinOps
- FOCUS
---
