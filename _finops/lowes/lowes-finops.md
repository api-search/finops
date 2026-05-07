---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lowes-product-api-openapi.yml
  format: yaml
  label: Lowe's Product API
  slug: product-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lowes/refs/heads/main/openapi/lowes-product-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Contract
description: 'FOCUS-aligned FinOps stub for Lowe''s: APIs are partner-contracted rather than publicly priced; FinOps treatment is contract-driven with negotiated meters per integration.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lowe's Companies, Inc.
  ProviderName: Lowe's
  PublisherName: Lowe's Companies, Inc.
  ServiceCategory: Retail
  ServiceName: Lowe's APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - integration
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - integration
  name: contracted_volume
  unit: varies
name: Lowes Finops
provider_name: Lowe's
provider_slug: lowes
publisher_name: Lowe's Companies, Inc.
service_category: Retail
slug: lowes-finops
source_filename: lowes-finops.yml
source_heading: FinOps Profile
source_url: https://www.lowes.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lowe's\nproviderId: lowes\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Retail\ndescription: 'FOCUS-aligned FinOps stub for Lowe''s: APIs are partner-contracted rather than publicly\n  priced; FinOps treatment is contract-driven with negotiated meters per integration.'\nsources:\n  - https://www.lowes.com\nnotes: No public pricing / billing documentation; values are contract-driven scaffold pointers.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lowe's Companies, Inc.\nserviceCategory: Retail\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n\
  \    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Lowe's APIs\n  ServiceCategory: Retail\n  ProviderName: Lowe's\n  PublisherName: Lowe's Companies, Inc.\n  InvoiceIssuerName: Lowe's Companies, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - partner\n  - name: contracted_volume\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - integration\nprinciples:\n  - name: Visibility\n    description: Track partner-API consumption against contracted volume; reconcile against monthly\n      partner statements.\n  - name: Allocation\n    description: Tag requests by integration program (supplier, marketplace, fulfillment) for partner-side\n      chargeback.\n  - name: Optimization\n    description: Batch supplier feeds and marketplace updates; cache product data on the partner side to\n      stay within contracted volumes.\n  - name: Accountability\n    description: Partner-side\
  \ owners reconcile contract terms quarterly; escalate variances through the\n      Lowe's partner team.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lowes/refs/heads/main/finops/lowes-finops.yml
sources:
- https://www.lowes.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Retail
---
