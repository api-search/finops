---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Custom (Partner Contract)
description: FOCUS-aligned FinOps scaffold for Carter's. No public API pricing or invoice surface is published; meters and FOCUS columns are the recommended starting points for partners that have negotiated private B2B agreements.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Carter's, Inc.
  ProviderName: Carter's
  PublisherName: Carter's, Inc.
  ServiceCategory: Retail
  ServiceName: Carter's API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - partner
  name: api_requests
  unit: request
name: Carter Finops
provider_name: Carter's
provider_slug: carter
publisher_name: Carter's, Inc.
service_category: Retail
slug: carter-finops
source_filename: carter-finops.yml
source_heading: FinOps Profile
source_url: https://www.carters.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Carter's\nproviderId: carter\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Retail\n  - Children\n  - Apparel\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps scaffold for Carter''s. No public API pricing or invoice surface is\n  published; meters and FOCUS columns are the recommended starting points for partners that have negotiated\n  private B2B agreements.'\nnotes: Billing is private (partner contracts). Reconcile once Carter's publishes API or partner pricing.\nsources:\n  - https://www.carters.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Carter's, Inc.\nserviceCategory: Retail\nbillingModel:\n  pricingCategory: Custom (Partner\
  \ Contract)\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Carter's API\n  ServiceCategory: Retail\n  ProviderName: Carter's\n  PublisherName: Carter's, Inc.\n  InvoiceIssuerName: Carter's, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\nprinciples:\n  - name: Visibility\n    description: Track partner integration consumption through the negotiated reporting surface delivered\n      with the partner agreement; no public usage API is published.\n  - name: Allocation\n    description: Tag partner integration costs to the consuming retail / supply-chain function before\n      issuing chargeback.\n  - name: Optimization\n    description: Batch catalog and order updates; align polling cadence with Carter's published refresh\n      windows to avoid wasted requests.\n  - name: Accountability\n\
  \    description: Assign a procurement and IT owner for the Carter's partner relationship; review invoiced\n      partner fees against contractual SLAs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carter/refs/heads/main/finops/carter-finops.yml
sources:
- https://www.carters.com
specification: FinOps Framework
tags:
- Retail
- Children
- Apparel
- FinOps
- FOCUS
---
