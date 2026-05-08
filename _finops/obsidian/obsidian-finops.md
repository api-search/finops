---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: obsidian-local-rest-api-openapi.yaml
  format: yaml
  label: Obsidian Local REST API
  slug: obsidian-local-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/obsidian/refs/heads/main/openapi/obsidian-local-rest-api-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual or Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Add-Ons) + One-Time Licenses
description: FOCUS-aligned FinOps profile for Obsidian. The core Obsidian app is free for personal use; commercial use is covered by an optional per-user annual license. Two managed add-ons (Sync, Publish) and a one-time Catalyst license are sold separately. There is no per-API or metered usage cost.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Dynalist Inc.
  ProviderName: Obsidian
  PublisherName: Dynalist Inc.
  ServiceCategory: Productivity
  ServiceName: Obsidian
layout: finops
meters:
- aggregation: sum
  description: Per-user commercial-use license at $50/user/year.
  dimensions:
  - organization
  name: commercial_license_seats
  unit: seat
- aggregation: sum
  description: Obsidian Sync per-user subscription ($4/user/mo annual, $5/user/mo monthly).
  dimensions:
  - account
  name: sync_seats
  unit: seat
- aggregation: sum
  description: Obsidian Publish per-site subscription ($8/site/mo annual, $10/site/mo monthly).
  dimensions:
  - account
  name: publish_sites
  unit: site
- aggregation: sum
  description: One-time Catalyst supporter license at $25.
  dimensions:
  - account
  name: catalyst_licenses
  unit: license
name: Obsidian Finops
provider_name: Obsidian
provider_slug: obsidian
publisher_name: Dynalist Inc. (Obsidian)
service_category: Productivity
slug: obsidian-finops
source_filename: obsidian-finops.yml
source_heading: FinOps Profile
source_url: https://obsidian.md/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Obsidian\nproviderId: obsidian\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Knowledge Management\n- Markdown\n- Notes\n- Local-First\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Obsidian. The core Obsidian app is free for\n  personal use; commercial use is covered by an optional per-user annual license. Two\n  managed add-ons (Sync, Publish) and a one-time Catalyst license are sold separately.\n  There is no per-API or metered usage cost.\nsources:\n- https://obsidian.md/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Dynalist Inc.\
  \ (Obsidian)\nserviceCategory: Productivity\nbillingModel:\n  pricingCategory: Subscription (Add-Ons) + One-Time Licenses\n  billingFrequency: Annual or Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Obsidian\n  ServiceCategory: Productivity\n  ProviderName: Obsidian\n  PublisherName: Dynalist Inc.\n  InvoiceIssuerName: Dynalist Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: commercial_license_seats\n  description: Per-user commercial-use license at $50/user/year.\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - organization\n- name: sync_seats\n  description: Obsidian Sync per-user subscription ($4/user/mo annual, $5/user/mo monthly).\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - account\n- name: publish_sites\n  description: Obsidian Publish per-site subscription ($8/site/mo annual, $10/site/mo monthly).\n  unit: site\n  aggregation: sum\n  dimensions:\n  - account\n- name: catalyst_licenses\n\
  \  description: One-time Catalyst supporter license at $25.\n  unit: license\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Track Sync seats, Publish sites, and Commercial licenses centrally; consolidate\n    Obsidian-related receipts in your AP/expense system.\n- name: Allocation\n  description: Allocate Commercial license cost to the employees and teams holding it; Sync\n    and Publish to specific users/sites.\n- name: Optimization\n  description: Use annual billing for Sync/Publish where committed; reclaim Sync seats from\n    inactive users; consolidate multiple personal Sync subscriptions if shifting to a single\n    org-managed plan.\n- name: Accountability\n  description: Assign an owner for organization-wide Obsidian licensing and review annually.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/obsidian/refs/heads/main/finops/obsidian-finops.yml
sources:
- https://obsidian.md/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Knowledge Management
- Markdown
- Notes
- Local-First
- FinOps
- Cost Management
- FOCUS
---
