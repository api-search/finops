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
  - Purchase
  - Adjustment
  pricingCategory: Negotiated
description: 'FOCUS-aligned FinOps for Graco Inc: no public API price book is published. Cost shape is presumed to be a contract-level partner fee plus underlying product / service revenue, not a metered API line item. This document is a placeholder pending direct reconciliation with Graco.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Graco Inc
  ProviderName: Graco Inc
  PublisherName: Graco Inc
  ServiceCategory: Industrial Equipment / Manufacturing
  ServiceName: Graco Inc API
layout: finops
meters:
- aggregation: sum
  description: API request volume (presumed operational metric, not directly billed)
  dimensions:
  - partner
  - environment
  name: api_requests
  unit: request
name: Graco Finops
provider_name: Graco Inc
provider_slug: graco
publisher_name: Graco Inc
service_category: Industrial Equipment / Manufacturing
slug: graco-finops
source_filename: graco-finops.yml
source_heading: FinOps Profile
source_url: https://www.graco.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Graco Inc\nproviderId: graco\npublisherName: Graco Inc\nserviceCategory: Industrial Equipment / Manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Manufacturing\n  - Industrial\ndescription: 'FOCUS-aligned FinOps for Graco Inc: no public API price book is published. Cost shape\n  is presumed to be a contract-level partner fee plus underlying product / service revenue, not a\n  metered API line item. This document is a placeholder pending direct reconciliation with Graco.'\nnotes: No public pricing or billing documentation for Graco APIs. Reconcile when a developer portal\n  with pricing\
  \ is published.\nsources:\n  - https://www.graco.com\nbillingModel:\n  pricingCategory: Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Graco Inc API\n  ServiceCategory: Industrial Equipment / Manufacturing\n  ProviderName: Graco Inc\n  PublisherName: Graco Inc\n  InvoiceIssuerName: Graco Inc\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_requests\n    description: API request volume (presumed operational metric, not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - environment\nprinciples:\n  - name: Visibility\n    description: Until Graco exposes usage telemetry, partners should self-instrument calls to\n      api.graco.com to track consumption.\n  - name: Allocation\n    description: Tag integration code with partner / division so any future Graco invoice can be\n      mapped back to consuming business\
  \ units.\n  - name: Optimization\n    description: Cache catalog / static data; avoid polling; batch operations when the API supports\n      it.\n  - name: Accountability\n    description: Designate a partner / commercial owner inside the consumer org responsible for the\n      Graco contract and any volume escalations.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/graco/refs/heads/main/finops/graco-finops.yml
sources:
- https://www.graco.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Manufacturing
- Industrial
---
