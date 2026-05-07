---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sabre-bargain-finder-max-openapi.yml
  format: yaml
  label: Sabre Bargain Finder Max API
  slug: bargain-finder-max
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sabre/refs/heads/main/openapi/sabre-bargain-finder-max-openapi.yml
- filename: sabre-hotels-openapi.yml
  format: yaml
  label: Sabre Hotels API
  slug: hotels
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sabre/refs/heads/main/openapi/sabre-hotels-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Enterprise GDS Contract / Contact Sales
description: 'FOCUS-aligned FinOps placeholder for Sabre: GDS / NDC API access is sold under enterprise contracts with no public unit pricing or invoice schema. Meters and FOCUS columns reflect a contracted-spend posture rather than usage-based billing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sabre GLBL Inc.
  ProviderName: Sabre
  PublisherName: Sabre GLBL Inc.
  ServiceCategory: Travel / GDS
  ServiceName: Sabre
layout: finops
meters:
- aggregation: sum
  name: contracted_segments
  unit: varies
- aggregation: sum
  name: shopping_calls
  unit: varies
name: Sabre Finops
provider_name: Sabre
provider_slug: sabre
publisher_name: Sabre GLBL Inc.
service_category: Travel / GDS
slug: sabre-finops
source_filename: sabre-finops.yml
source_heading: FinOps Profile
source_url: https://developer.sabre.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sabre\nproviderId: sabre\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Travel\n  - GDS\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Sabre: GDS / NDC API access is sold under enterprise\n  contracts with no public unit pricing or invoice schema. Meters and FOCUS columns reflect a contracted-spend\n  posture rather than usage-based billing.'\nsources:\n  - https://developer.sabre.com/\nnotes: Sabre publishes no public per-call prices, plan tiers, billing meters, or FOCUS-friendly invoice\n  mappings. This file is a Contact-Sales placeholder.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Sabre GLBL Inc.\nserviceCategory:\
  \ Travel / GDS\nbillingModel:\n  pricingCategory: Enterprise GDS Contract / Contact Sales\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sabre\n  ServiceCategory: Travel / GDS\n  ProviderName: Sabre\n  PublisherName: Sabre GLBL Inc.\n  InvoiceIssuerName: Sabre GLBL Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_segments\n    unit: varies\n    aggregation: sum\n  - name: shopping_calls\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from Sabre's contracted reporting (segment / booking statements, PCC\n      activity reports). Combine those with internal app-side telemetry to attribute API consumption.\n  - name: Allocation\n    description: Allocate by PCC, agency branch, line of business, or product (air / hotel / car), aligned\n      to the Sabre contract's billing dimensions.\n  - name: Optimization\n    description: Optimize shopping-to-booking\
  \ conversion, cache low-volatility content where contractually\n      permitted, and consolidate PCCs where billing dimensions align to reduce contracted minimums.\n  - name: Accountability\n    description: Operations and procurement jointly own the Sabre contract; reconcile segment / booking\n      meters against monthly statements and review at contract renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sabre/refs/heads/main/finops/sabre-finops.yml
sources:
- https://developer.sabre.com/
specification: FinOps Framework
tags:
- Travel
- GDS
- B2B
- FinOps
- FOCUS
---
