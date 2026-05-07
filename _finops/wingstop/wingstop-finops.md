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
  - Purchase
  pricingCategory: Partner-Negotiated
description: FinOps shape for Wingstop is partner-contract-driven - no public per-call price exists. Cost lines for an integrating party are commission / fee structures negotiated with corporate or third-party delivery (3PD) partners.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Wingstop Restaurants Inc.
  ProviderName: Wingstop
  PublisherName: Wingstop Restaurants Inc.
  ServiceCategory: Restaurants
  ServiceName: Wingstop Integrations
layout: finops
meters:
- aggregation: sum
  dimensions:
  - channel
  - location
  name: orders_processed
  unit: order
- aggregation: sum
  dimensions:
  - partner_program
  name: integration_partner_fees
  unit: varies
name: Wingstop Finops
provider_name: Wingstop
provider_slug: wingstop
publisher_name: Wingstop Restaurants Inc.
service_category: Restaurants
slug: wingstop-finops
source_filename: wingstop-finops.yml
source_heading: FinOps Profile
source_url: https://www.wingstop.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Wingstop\nproviderId: wingstop\npublisherName: Wingstop Restaurants Inc.\nserviceCategory: Restaurants\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Restaurants\n  - QSR\n  - Food Service\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Wingstop is partner-contract-driven - no public per-call price exists. Cost lines for an integrating party are commission / fee structures negotiated with corporate or third-party delivery (3PD) partners.\nsources:\n  - https://www.wingstop.com\nnotes: No public pricing or billing surface. Populate meters once a corporate / franchisee / 3PD integration agreement\
  \ is in place.\nbillingModel:\n  pricingCategory: Partner-Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Wingstop Integrations\n  ServiceCategory: Restaurants\n  ProviderName: Wingstop\n  PublisherName: Wingstop Restaurants Inc.\n  InvoiceIssuerName: Wingstop Restaurants Inc.\n  BillingCurrency: USD\nmeters:\n  - name: orders_processed\n    unit: order\n    aggregation: sum\n    dimensions:\n      - channel\n      - location\n  - name: integration_partner_fees\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - partner_program\nprinciples:\n  - name: Visibility\n    description: Reconcile against POS / 3PD partner reports and corporate franchisee dashboards; there is no public Wingstop billing API.\n  - name: Allocation\n    description: Allocate by channel (web, app, 3PD partner) and store / location, matching how franchise reporting is structured.\n  - name: Optimization\n\
  \    description: Levers are commercial - 3PD commission negotiation, channel mix, and reducing failed-order retries.\n  - name: Accountability\n    description: Owned by the franchisee / corporate operations team; technical integrators own reliability, not unit cost.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wingstop/refs/heads/main/finops/wingstop-finops.yml
sources:
- https://www.wingstop.com
specification: FinOps Framework
tags:
- Restaurants
- QSR
- Food Service
- FinOps
- FOCUS
- Contact Sales
---
