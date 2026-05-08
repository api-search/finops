---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rutter-unified-api-openapi.yml
  format: yaml
  label: Rutter Unified API
  slug: unified-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rutter/refs/heads/main/openapi/rutter-unified-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contact Sales / Custom Quote
description: 'FOCUS-aligned FinOps placeholder for Rutter: production pricing is custom-quoted (Contact Sales), so meters and FOCUS columns are minimal until contract terms are visible.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Rutter, Inc.
  ProviderName: Rutter
  PublisherName: Rutter, Inc.
  ServiceCategory: Unified API
  ServiceName: Rutter
layout: finops
meters:
- aggregation: sum
  name: contracted_access
  unit: varies
name: Rutter Finops
provider_name: Rutter
provider_slug: rutter
publisher_name: Rutter, Inc.
service_category: Unified API / Commerce + Accounting Integration
slug: rutter-finops
source_filename: rutter-finops.yml
source_heading: FinOps Profile
source_url: https://www.rutter.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Rutter\nproviderId: rutter\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Accounting\n  - Commerce\n  - Unified API\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Rutter: production pricing is custom-quoted (Contact\n  Sales), so meters and FOCUS columns are minimal until contract terms are visible.'\nsources:\n  - https://www.rutter.com/pricing\nnotes: Rutter does not publish unit prices, billing meters, or invoice line-item structure publicly. This\n  file is intentionally a Contact-Sales placeholder rather than a fabricated FinOps shape.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Rutter, Inc.\nserviceCategory: Unified\
  \ API / Commerce + Accounting Integration\nbillingModel:\n  pricingCategory: Contact Sales / Custom Quote\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Rutter\n  ServiceCategory: Unified API\n  ProviderName: Rutter\n  PublisherName: Rutter, Inc.\n  InvoiceIssuerName: Rutter, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contracted_access\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Without published meters, visibility depends on Rutter's customer dashboard and any usage\n      reports furnished under contract. Capture connection counts and call volumes from the Rutter dashboard.\n  - name: Allocation\n    description: Tag Rutter consumption by the internal product or workflow that triggers each connection\n      (e.g. onboarding, reconciliation) so contract spend can be attributed.\n  - name: Optimization\n    description: Reduce redundant connector polling,\
  \ prefer webhook-driven sync where Rutter supports it,\n      and consolidate connections per end-customer to keep contracted volume in line.\n  - name: Accountability\n    description: Assign an owner for the Rutter contract; reconcile invoiced amounts against the customer\n      dashboard and downstream platform usage during contract review cycles.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rutter/refs/heads/main/finops/rutter-finops.yml
sources:
- https://www.rutter.com/pricing
specification: FinOps Framework
tags:
- Accounting
- Commerce
- Unified API
- FinOps
- FOCUS
---
