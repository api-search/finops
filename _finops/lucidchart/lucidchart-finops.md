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
  - Adjustment
  pricingCategory: Subscription (Per Seat)
description: FOCUS-aligned FinOps profile for Lucidchart. Lucidchart bills as a per-user monthly subscription across Free, Individual, Team, and Enterprise. Team and Enterprise are sold as part of the Lucid Visual Collaboration Suite (Lucidchart + Lucidspark + Lucidscale) for a single per-user fee. Developer API use does not add metered API charges.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Lucid Software
  ProviderName: Lucid Software
  PublisherName: Lucid Software
  ServiceCategory: Productivity
  ServiceName: Lucidchart
layout: finops
meters:
- aggregation: sum
  description: Per-user monthly subscription. Individual $7.95, Team $9 (Lucidchart) or $12 (Suite), Enterprise contract.
  dimensions:
  - account
  - plan
  - product
  name: user_seats
  unit: seat
name: Lucidchart Finops
provider_name: Lucidchart
provider_slug: lucidchart
publisher_name: Lucid Software
service_category: Productivity
slug: lucidchart-finops
source_filename: lucidchart-finops.yml
source_heading: FinOps Profile
source_url: https://www.lucidchart.com/pages/pricing/lucidchart
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lucidchart\nproviderId: lucidchart\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Diagramming\n- Visualization\n- Visual Workspace\n- SaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Lucidchart. Lucidchart bills as a per-user\n  monthly subscription across Free, Individual, Team, and Enterprise. Team and Enterprise\n  are sold as part of the Lucid Visual Collaboration Suite (Lucidchart + Lucidspark +\n  Lucidscale) for a single per-user fee. Developer API use does not add metered API charges.\nsources:\n- https://www.lucidchart.com/pages/pricing/lucidchart\n- https://developer.lucid.co/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lucid Software\nserviceCategory: Productivity\nbillingModel:\n  pricingCategory: Subscription (Per Seat)\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Lucidchart\n  ServiceCategory: Productivity\n  ProviderName: Lucid Software\n  PublisherName: Lucid Software\n  InvoiceIssuerName: Lucid Software\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: user_seats\n  description: Per-user monthly subscription. Individual $7.95, Team $9 (Lucidchart)\n    or $12 (Suite), Enterprise contract.\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n  - product\nprinciples:\n- name: Visibility\n  description: Use Lucid admin console license reports to inventory active users and plan\n    tier.\n- name: Allocation\n  description: Allocate user seats by team membership; tag enterprise\
  \ contract spend to\n    procuring business units.\n- name: Optimization\n  description: Reclaim seats from inactive users; downgrade Suite seats to Lucidchart-only\n    where the user does not use Lucidspark/Lucidscale; choose annual billing for the\n    discount.\n- name: Accountability\n  description: Assign an admin owner per Lucid account; review quarterly seat counts\n    against active-user reports.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lucidchart/refs/heads/main/finops/lucidchart-finops.yml
sources:
- https://www.lucidchart.com/pages/pricing/lucidchart
- https://developer.lucid.co/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Diagramming
- Visualization
- Visual Workspace
- SaaS
- FinOps
- Cost Management
- FOCUS
---
