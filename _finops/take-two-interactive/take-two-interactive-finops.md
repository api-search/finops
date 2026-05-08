---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  pricingCategory: Custom / Contact Sales
description: FinOps placeholder for Take-Two Interactive. No corporate-level API billing surface is published; consumer-side cost mapping is governed by individual studio partner agreements.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Take-Two Interactive Software, Inc.
  ProviderName: Take-Two Interactive
  PublisherName: Take-Two Interactive Software, Inc.
  ServiceCategory: Interactive Entertainment
  ServiceName: Take-Two Interactive
layout: finops
meters:
- aggregation: sum
  name: custom_engagement
  unit: varies
name: Take Two Interactive Finops
provider_name: Take-Two Interactive Software
provider_slug: take-two-interactive
publisher_name: Take-Two Interactive Software, Inc.
service_category: Interactive Entertainment
slug: take-two-interactive-finops
source_filename: take-two-interactive-finops.yml
source_heading: FinOps Profile
source_url: https://www.take2games.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Take-Two Interactive Software\nproviderId: take-two-interactive\npublisherName: Take-Two Interactive Software, Inc.\nserviceCategory: Interactive Entertainment\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Gaming\n  - Interactive Entertainment\n  - FinOps\n  - FOCUS\ndescription: FinOps placeholder for Take-Two Interactive. No corporate-level API billing surface\n  is published; consumer-side cost mapping is governed by individual studio partner agreements.\nsources:\n  - https://www.take2games.com/\nnotes: No public billing telemetry at corporate level. Meter list collapsed to custom engagement\n  pending direct studio\
  \ or partner confirmation.\nbillingModel:\n  pricingCategory: Custom / Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\nfocusColumns:\n  ServiceName: Take-Two Interactive\n  ServiceCategory: Interactive Entertainment\n  ProviderName: Take-Two Interactive\n  PublisherName: Take-Two Interactive Software, Inc.\n  InvoiceIssuerName: Take-Two Interactive Software, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: custom_engagement\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Cost and consumption visibility is provided through individual studio partner\n      portals (Rockstar, 2K, Zynga) rather than a unified Take-Two surface.\n  - name: Allocation\n    description: Allocation is performed against studio-level invoices and partner statements in\n      the consumer's own finance system.\n  - name: Optimization\n    description: Optimization is handled through commercial review with the relevant\
  \ studio business\n      development team.\n  - name: Accountability\n    description: Accountability sits with the partner team that owns the studio relationship.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/take-two-interactive/refs/heads/main/finops/take-two-interactive-finops.yml
sources:
- https://www.take2games.com/
specification: FinOps Framework
tags:
- Gaming
- Interactive Entertainment
- FinOps
- FOCUS
---
