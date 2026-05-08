---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription (Per Site) + Per-Editor Add-On + Usage
description: FOCUS-aligned FinOps profile for Framer. Framer prices per site (Free/Basic $10 / Pro $30 / Scale $100 + usage / Enterprise custom). Additional editors are an add-on at $20-$40/editor/month depending on tier. Site bandwidth and pages are plan-level allowances; Scale and Enterprise add usage-based bandwidth components.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Framer B.V.
  ProviderName: Framer
  PublisherName: Framer B.V.
  ServiceCategory: Productivity
  ServiceName: Framer
layout: finops
meters:
- aggregation: sum
  description: Per-site monthly subscription (Basic $10, Pro $30, Scale $100, Enterprise contract).
  dimensions:
  - account
  - plan
  name: site_subscription
  unit: site
- aggregation: sum
  description: Add-on per-editor monthly fee ($20-$40 depending on tier).
  dimensions:
  - account
  - site
  name: editor_seats
  unit: seat
- aggregation: sum
  description: Site bandwidth usage in GB; included allowance per plan, overage on Scale and Enterprise.
  dimensions:
  - site
  name: bandwidth
  unit: gigabyte
name: Framer Finops
provider_name: Framer
provider_slug: framer
publisher_name: Framer B.V.
service_category: Productivity
slug: framer-finops
source_filename: framer-finops.yml
source_heading: FinOps Profile
source_url: https://www.framer.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Framer\nproviderId: framer\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Design\n- No-Code\n- Web Design\n- SaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Framer. Framer prices per site (Free/Basic\n  $10 / Pro $30 / Scale $100 + usage / Enterprise custom). Additional editors are an\n  add-on at $20-$40/editor/month depending on tier. Site bandwidth and pages are\n  plan-level allowances; Scale and Enterprise add usage-based bandwidth components.\nsources:\n- https://www.framer.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Framer B.V.\nserviceCategory: Productivity\nbillingModel:\n  pricingCategory: Subscription (Per Site) + Per-Editor Add-On + Usage\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Framer\n  ServiceCategory: Productivity\n  ProviderName: Framer\n  PublisherName: Framer B.V.\n  InvoiceIssuerName: Framer B.V.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: site_subscription\n  description: Per-site monthly subscription (Basic $10, Pro $30, Scale $100,\n    Enterprise contract).\n  unit: site\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n- name: editor_seats\n  description: Add-on per-editor monthly fee ($20-$40 depending on tier).\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - account\n  - site\n- name: bandwidth\n  description: Site bandwidth usage in GB; included allowance per plan, overage on Scale\n    and Enterprise.\n  unit: gigabyte\n\
  \  aggregation: sum\n  dimensions:\n  - site\nprinciples:\n- name: Visibility\n  description: Inventory all Framer sites under each account; tag sites to projects or\n    business owners.\n- name: Allocation\n  description: Allocate site subscriptions and editor add-ons to the team owning each site.\n- name: Optimization\n  description: Consolidate low-traffic sites onto Basic/Pro; downgrade Scale to Pro when\n    traffic permits; reclaim editor seats from inactive collaborators.\n- name: Accountability\n  description: Assign one Framer account owner per organization; review quarterly site\n    inventory and bandwidth usage.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/framer/refs/heads/main/finops/framer-finops.yml
sources:
- https://www.framer.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Design
- No-Code
- Web Design
- SaaS
- FinOps
- Cost Management
- FOCUS
---
