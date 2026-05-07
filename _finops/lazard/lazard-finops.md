---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Engagement
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Engagement / Advisory Fee
description: Lazard publishes no public API pricing or billing documentation. This artifact is a placeholder FOCUS-aligned scaffold for any future private institutional integration; meters describe the kind of signal a consumer would track against an engagement agreement.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Lazard, Inc.
  ProviderName: Lazard
  PublisherName: Lazard, Inc.
  ServiceCategory: Financial Services / Advisory
  ServiceName: Lazard
layout: finops
meters:
- aggregation: sum
  dimensions:
  - integration
  - environment
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - engagement
  name: documents_exchanged
  unit: document
name: Lazard Finops
provider_name: Lazard
provider_slug: lazard
publisher_name: Lazard, Inc.
service_category: Financial Services / Advisory
slug: lazard-finops
source_filename: lazard-finops.yml
source_heading: FinOps Profile
source_url: https://www.lazard.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lazard\nproviderId: lazard\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Investment Banking\n  - Asset Management\ndescription: Lazard publishes no public API pricing or billing documentation. This artifact is a placeholder\n  FOCUS-aligned scaffold for any future private institutional integration; meters describe the kind of\n  signal a consumer would track against an engagement agreement.\nsources:\n  - https://www.lazard.com/\nnotes: No public pricing or billing model. FinOps shape can only be filled in once a private engagement\n  exists.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lazard, Inc.\nserviceCategory: Financial\
  \ Services / Advisory\nbillingModel:\n  pricingCategory: Engagement / Advisory Fee\n  billingFrequency: Per-Engagement\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Lazard\n  ServiceCategory: Financial Services / Advisory\n  ProviderName: Lazard\n  PublisherName: Lazard, Inc.\n  InvoiceIssuerName: Lazard, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - integration\n      - environment\n  - name: documents_exchanged\n    unit: document\n    aggregation: sum\n    dimensions:\n      - engagement\nprinciples:\n  - name: Visibility\n    description: No public consumption telemetry; integrators measure traffic and document volume client-side\n      against engagement scope.\n  - name: Allocation\n    description: Tag any private API calls with the consuming fund / mandate / deal so cost can be allocated\n      against the engagement fee.\n  - name:\
  \ Optimization\n    description: Cache low-volatility reference data; coordinate batch workflows over real-time polling;\n      reduce duplicate document exchanges.\n  - name: Accountability\n    description: Engagement owner and operations counterpart review integration metrics against the\n      advisory or fund agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lazard/refs/heads/main/finops/lazard-finops.yml
sources:
- https://www.lazard.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Investment Banking
- Asset Management
---
