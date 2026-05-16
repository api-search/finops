---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ghost-admin-api-openapi.yml
  format: yaml
  label: Ghost Admin API
  slug: ghost-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/openapi/ghost-admin-api-openapi.yml
- filename: ghost-content-api-openapi.yml
  format: yaml
  label: Ghost Content API
  slug: ghost-content-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/openapi/ghost-content-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Ghost(Pro)) or Self-Hosted Open Source
description: FOCUS-aligned FinOps profile for Ghost — open-source software with a hosted Ghost(Pro) tier.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ghost Foundation
  ProviderName: Ghost
  PublisherName: Ghost Foundation
  ServiceCategory: Publishing
  ServiceName: Ghost(Pro) Hosting
layout: finops
meters:
- aggregation: sum
  description: Monthly/annual plan fee for Ghost(Pro).
  dimensions:
  - plan_tier
  name: plan_subscription
  unit: months
- aggregation: max
  description: Member count drives plan-tier breakpoints.
  dimensions:
  - account
  name: members
  unit: members
- aggregation: sum
  description: When self-hosting, infrastructure costs (compute, storage, email) replace plan fees.
  dimensions:
  - cloud_provider
  - region
  name: self_host_infrastructure
  unit: varies
name: Ghost Finops
provider_name: Ghost
provider_slug: ghost
publisher_name: Ghost Foundation
service_category: Publishing
slug: ghost-finops
source_filename: ghost-finops.yml
source_heading: FinOps Profile
source_url: https://ghost.org/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ghost\nproviderId: ghost\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Publishing\n- Open Source\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Ghost — open-source software with a hosted Ghost(Pro) tier.\nnotes: >-\n  Ghost software is MIT-licensed and free to self-host (you pay only your infrastructure\n  costs). Ghost(Pro) is a flat-rate subscription with member-count breakpoints. APIs are\n  included with both options.\nsources:\n- https://ghost.org/pricing/\n- https://github.com/TryGhost/Ghost\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ghost Foundation\n\
  serviceCategory: Publishing\nbillingModel:\n  pricingCategory: Subscription (Ghost(Pro)) or Self-Hosted Open Source\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Ghost(Pro) Hosting\n  ServiceCategory: Publishing\n  ProviderName: Ghost\n  PublisherName: Ghost Foundation\n  InvoiceIssuerName: Ghost Foundation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: plan_subscription\n  description: Monthly/annual plan fee for Ghost(Pro).\n  unit: months\n  aggregation: sum\n  dimensions:\n  - plan_tier\n- name: members\n  description: Member count drives plan-tier breakpoints.\n  unit: members\n  aggregation: max\n  dimensions:\n  - account\n- name: self_host_infrastructure\n  description: When self-hosting, infrastructure costs (compute, storage, email) replace plan fees.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - cloud_provider\n  - region\nprinciples:\n\
  - name: Visibility\n  description: Track Ghost(Pro) invoices or self-host infra spend; correlate to member growth and email volume.\n- name: Allocation\n  description: Allocate publishing spend to the content/marketing cost center.\n- name: Optimization\n  description: For high-volume publishers, evaluate self-hosted vs. Ghost(Pro) at each tier breakpoint; manage email-send infrastructure costs.\n- name: Accountability\n  description: Assign a publishing-ops owner to review tier vs. members quarterly.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ghost/refs/heads/main/finops/ghost-finops.yml
sources:
- https://ghost.org/pricing/
- https://github.com/TryGhost/Ghost
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Publishing
- Open Source
- FinOps
- Cost Management
- FOCUS
---
