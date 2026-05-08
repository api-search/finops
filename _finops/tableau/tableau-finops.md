---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tableau-rest-api-openapi.yml
  format: yaml
  label: Tableau REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tableau/refs/heads/main/openapi/tableau-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps shape for Tableau Cloud / Tableau Server: per-user role-based subscriptions (Creator / Explorer / Viewer) plus enterprise add-ons. The site-level capacity caps documented in Tableau Cloud (extract refresh, publish, VizQL Data Service) are operational ceilings, not separately metered billing lines.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Salesforce, Inc.
  PricingUnit: seat-month
  ProviderName: Tableau
  PublisherName: Salesforce, Inc.
  ServiceCategory: Analytics & Business Intelligence
  ServiceName: Tableau
layout: finops
meters:
- aggregation: max
  dimensions:
  - site
  name: creator_seats
  unit: seat
- aggregation: max
  dimensions:
  - site
  name: explorer_seats
  unit: seat
- aggregation: max
  dimensions:
  - site
  name: viewer_seats
  unit: seat
- aggregation: max
  dimensions:
  - site
  - addon
  name: enterprise_addons
  unit: varies
name: Tableau Finops
provider_name: Tableau
provider_slug: tableau
publisher_name: Salesforce, Inc.
service_category: Analytics & Business Intelligence
slug: tableau-finops
source_filename: tableau-finops.yml
source_heading: FinOps Profile
source_url: https://www.tableau.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tableau\nproviderId: tableau\npublisherName: Salesforce, Inc.\nserviceCategory: Analytics & Business Intelligence\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Analytics\n  - Business Intelligence\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps shape for Tableau Cloud / Tableau Server: per-user role-based\n  subscriptions (Creator / Explorer / Viewer) plus enterprise add-ons. The site-level capacity\n  caps documented in Tableau Cloud (extract refresh, publish, VizQL Data Service) are operational\n  ceilings, not separately metered billing lines.'\nsources:\n  - https://www.tableau.com/pricing\n  - https://help.tableau.com/current/online/en-us/to_site_capacity.htm\n\
  notes: Tableau pricing page is gated to automated fetchers; subscription tiers and FOCUS columns\n  are reconciled but exact per-seat prices are not asserted here. Reconciled left false until\n  a live price string can be captured.\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Tableau\n  ServiceCategory: Analytics & Business Intelligence\n  ProviderName: Tableau\n  PublisherName: Salesforce, Inc.\n  InvoiceIssuerName: Salesforce, Inc.\n  BillingCurrency: USD\n  PricingUnit: seat-month\nmeters:\n  - name: creator_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - site\n  - name: explorer_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - site\n  - name: viewer_seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - site\n  - name: enterprise_addons\n    unit: varies\n    aggregation: max\n    dimensions:\n  \
  \    - site\n      - addon\nprinciples:\n  - name: Visibility\n    description: Use the Tableau Cloud admin views and the REST API user-listing endpoints (with\n      the documented 3000-calls-per-minute Get Users cap) to enumerate active seats per role,\n      and reconcile against the Salesforce-issued Tableau invoice.\n  - name: Allocation\n    description: Allocate by Tableau Cloud site and by user role (Creator vs Explorer vs Viewer)\n      so chargeback reflects the actual seat mix rather than a flat per-user blend.\n  - name: Optimization\n    description: Right-size the Creator / Explorer / Viewer mix at renewal, retire dormant seats,\n      consolidate sites where governance allows, and respect the Cloud site-capacity limits to\n      avoid 429-driven inefficiency in extract refresh and publish workflows.\n  - name: Accountability\n    description: The analytics or BI platform owner who holds the Tableau Cloud site is the\n      accountable party for seat allocation and subscription\
  \ renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tableau/refs/heads/main/finops/tableau-finops.yml
sources:
- https://www.tableau.com/pricing
- https://help.tableau.com/current/online/en-us/to_site_capacity.htm
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- FinOps
- FOCUS
---
