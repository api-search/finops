---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: helpscout-openapi.yml
  format: yaml
  label: Help Scout Conversations API
  slug: helpscout-conversations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/helpscout/refs/heads/main/openapi/helpscout-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  pricingCategory: Subscription Per Seat
description: Help Scout's billing model is per-user-per-month subscription on Standard, Plus, and Pro tiers, plus AI Answers per-resolution usage and additional inbox / Docs site add-ons. Annual billing earns 16% off. This artifact maps Help Scout charges to FOCUS columns for FinOps allocation across customer-support cost centers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Help Scout
  ProviderName: Help Scout
  PublisherName: Help Scout
  ServiceCategory: Customer Support
  ServiceName: Help Scout
layout: finops
meters:
- aggregation: sum
  description: Active Standard / Plus / Pro user seats.
  dimensions:
  - tier
  - cost_center
  name: helpscout_seats
  unit: user-month
- aggregation: count
  description: AI Answers chatbot resolutions billed at $0.75 each.
  dimensions:
  - inbox
  - cost_center
  name: helpscout_ai_resolutions
  unit: resolutions
- aggregation: sum
  description: Additional mailbox / inbox seats above plan default ($10/mo each).
  dimensions:
  - team
  - cost_center
  name: helpscout_extra_inboxes
  unit: inbox-month
- aggregation: sum
  description: Additional Docs (knowledge base) sites above plan default ($20/mo each).
  dimensions:
  - product
  - cost_center
  name: helpscout_extra_docs_sites
  unit: docs_site-month
name: Helpscout Finops
provider_name: Help Scout
provider_slug: helpscout
publisher_name: Help Scout
service_category: Customer Support
slug: helpscout-finops
source_filename: helpscout-finops.yml
source_heading: FinOps Profile
source_url: https://www.helpscout.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Help Scout\nproviderId: helpscout\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Customer Support\n  - Help Desk\n  - FinOps\n  - FOCUS\ndescription: >-\n  Help Scout's billing model is per-user-per-month subscription on Standard,\n  Plus, and Pro tiers, plus AI Answers per-resolution usage and additional\n  inbox / Docs site add-ons. Annual billing earns 16% off. This artifact\n  maps Help Scout charges to FOCUS columns for FinOps allocation across\n  customer-support cost centers.\nsources:\n  - https://www.helpscout.com/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Help Scout\nserviceCategory:\
  \ Customer Support\nbillingModel:\n  pricingCategory: Subscription Per Seat\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Help Scout\n  ServiceCategory: Customer Support\n  ProviderName: Help Scout\n  PublisherName: Help Scout\n  InvoiceIssuerName: Help Scout\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: helpscout_seats\n    description: Active Standard / Plus / Pro user seats.\n    unit: user-month\n    aggregation: sum\n    dimensions:\n      - tier\n      - cost_center\n  - name: helpscout_ai_resolutions\n    description: AI Answers chatbot resolutions billed at $0.75 each.\n    unit: resolutions\n    aggregation: count\n    dimensions:\n      - inbox\n      - cost_center\n  - name: helpscout_extra_inboxes\n    description: Additional mailbox / inbox seats above plan default ($10/mo each).\n    unit: inbox-month\n    aggregation: sum\n    dimensions:\n\
  \      - team\n      - cost_center\n  - name: helpscout_extra_docs_sites\n    description: Additional Docs (knowledge base) sites above plan default ($20/mo each).\n    unit: docs_site-month\n    aggregation: sum\n    dimensions:\n      - product\n      - cost_center\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull Help Scout monthly invoices and AI Answers usage reports;\n      reconcile seats against the active user count in the Inbox API.\n  - name: Allocation\n    description: >-\n      Allocate seats by team or product (per inbox); allocate AI Answers\n      cost to the inbox driving the resolutions.\n  - name: Optimization\n    description: >-\n      Lock annual commitment for 16% discount; deactivate inactive\n      agents monthly; consolidate inboxes when possible.\n  - name: Accountability\n    description: >-\n      Designate Customer Support Operations as contract owner; review at\n      renewal and right-size tier (Standard vs Plus vs Pro).\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/helpscout/refs/heads/main/finops/helpscout-finops.yml
sources:
- https://www.helpscout.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Customer Support
- Help Desk
- FinOps
- FOCUS
---
