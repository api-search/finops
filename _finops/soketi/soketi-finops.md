---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A
  chargeCategories:
  - Usage
  pricingCategory: Open Source / Self-Host
description: FinOps view of Soketi. Open source - there is no Soketi SaaS bill. Cost is purely the cloud compute (VMs / containers), memory, network bandwidth, and (for horizontal scaling) Redis used to host the deployment.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cloud provider
  ProviderName: Cloud provider (operator's choice)
  PublisherName: Soketi (community)
  ServiceCategory: Realtime Infrastructure
  ServiceName: Soketi (self-hosted)
layout: finops
meters:
- aggregation: sum
  description: VM / container compute hours hosting Soketi.
  dimensions:
  - account
  - region
  name: compute
  unit: vcpu_hour
- aggregation: sum
  description: VM / container memory.
  dimensions:
  - account
  name: memory
  unit: gb_hour
- aggregation: sum
  description: WebSocket and REST egress bandwidth.
  dimensions:
  - account
  - region
  name: network_egress
  unit: gb
- aggregation: sum
  description: Redis instance / cluster cost for horizontal scaling.
  dimensions:
  - account
  name: redis
  unit: month
name: Soketi Finops
provider_name: Soketi
provider_slug: soketi
publisher_name: Soketi (community)
service_category: Realtime Infrastructure
slug: soketi-finops
source_filename: soketi-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/soketi/soketi
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Soketi\nproviderId: soketi\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Realtime\n  - Open Source\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Soketi. Open source - there is no Soketi SaaS bill. Cost is purely the cloud\n  compute (VMs / containers), memory, network bandwidth, and (for horizontal scaling) Redis used\n  to host the deployment.\nsources:\n  - https://github.com/soketi/soketi\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Soketi (community)\nserviceCategory: Realtime Infrastructure\nbillingModel:\n  pricingCategory: Open Source / Self-Host\n  billingFrequency: N/A\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Soketi (self-hosted)\n  ServiceCategory: Realtime Infrastructure\n  ProviderName: Cloud provider (operator's choice)\n  PublisherName: Soketi (community)\n  InvoiceIssuerName: Cloud provider\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: compute\n    description: VM / container compute hours hosting Soketi.\n    unit: vcpu_hour\n    aggregation: sum\n    dimensions:\n      - account\n      - region\n  - name: memory\n    description: VM / container memory.\n    unit: gb_hour\n    aggregation: sum\n    dimensions:\n      - account\n  - name: network_egress\n    description: WebSocket and REST egress bandwidth.\n    unit: gb\n    aggregation: sum\n    dimensions:\n      - account\n      - region\n  - name: redis\n    description: Redis instance / cluster cost for horizontal scaling.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\nprinciples:\n  - name:\
  \ Visibility\n    description: Tag Soketi infrastructure with a workload label; pull cloud-provider invoices into FinOps store.\n  - name: Allocation\n    description: Allocate compute and bandwidth to consuming product line.\n  - name: Optimization\n    description: Use spot instances where acceptable; right-size Redis for connection count.\n  - name: Accountability\n    description: Assign an SRE owner; review monthly compared to a Pusher / Ably TCO.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/soketi/refs/heads/main/finops/soketi-finops.yml
sources:
- https://github.com/soketi/soketi
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- Open Source
- FinOps
- FOCUS
---
