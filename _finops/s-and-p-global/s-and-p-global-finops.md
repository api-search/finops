---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: servicecatalog
  format: yaml
  label: S&P Global Commodity Insights API
  slug: commodity-insights
  spec_type: OpenAPI
  url: https://developer.spglobal.com/commodityinsights/servicecatalog
- filename: s-and-p-global-kensho-link-openapi.yml
  format: yaml
  label: Kensho Link API
  slug: kensho-link
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/s-and-p-global/refs/heads/main/openapi/s-and-p-global-kensho-link-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise License / Contact Sales
description: 'FOCUS-aligned FinOps placeholder for S&P Global: enterprise-licensed data and API products with no public unit pricing or invoice-line schema. Meters and FOCUS columns reflect a contracted-spend posture rather than usage-based billing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: S&P Global Inc.
  ProviderName: S&P Global
  PublisherName: S&P Global Inc.
  ServiceCategory: Financial Data
  ServiceName: S&P Global
layout: finops
meters:
- aggregation: max
  name: licensed_seats
  unit: seat
- aggregation: sum
  name: licensed_feed
  unit: varies
name: S And P Global Finops
provider_name: S&P Global
provider_slug: s-and-p-global
publisher_name: S&P Global Inc.
service_category: Financial Data / Capital Markets
slug: s-and-p-global-finops
source_filename: s-and-p-global-finops.yml
source_heading: FinOps Profile
source_url: https://www.spglobal.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: S&P Global\nproviderId: s-and-p-global\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Data\n  - Capital Markets\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for S&P Global: enterprise-licensed data and API products\n  with no public unit pricing or invoice-line schema. Meters and FOCUS columns reflect a contracted-spend\n  posture rather than usage-based billing.'\nsources:\n  - https://www.spglobal.com/\nnotes: S&P Global publishes no public unit prices, billing meters, or FOCUS-friendly invoice mappings.\n  This file is a Contact-Sales placeholder.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: S&P Global\
  \ Inc.\nserviceCategory: Financial Data / Capital Markets\nbillingModel:\n  pricingCategory: Enterprise License / Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: S&P Global\n  ServiceCategory: Financial Data\n  ProviderName: S&P Global\n  PublisherName: S&P Global Inc.\n  InvoiceIssuerName: S&P Global Inc.\n  BillingCurrency: USD\nmeters:\n  - name: licensed_seats\n    unit: seat\n    aggregation: max\n  - name: licensed_feed\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from S&P Global's contracted customer portals and entitlement reports;\n      consumers should pull seat / feed usage from the relevant product portal (Capital IQ Pro, Platts\n      Connect, etc.) rather than expect a unified usage API.\n  - name: Allocation\n    description: Allocate by business unit and use-case bound to the license; capture which desks, products,\n\
  \      or research workflows consume which feeds, since licenses are contractually scoped.\n  - name: Optimization\n    description: Right-size seats, retire unused feeds at renewal, consolidate overlapping product subscriptions\n      across business units, and monitor contract auto-escalators.\n  - name: Accountability\n    description: Procurement and the data office jointly own renewal and entitlement audits. Establish\n      a recurring license review at least quarterly given high contract value.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/s-and-p-global/refs/heads/main/finops/s-and-p-global-finops.yml
sources:
- https://www.spglobal.com/
specification: FinOps Framework
tags:
- Financial Data
- Capital Markets
- B2B
- FinOps
- FOCUS
---
