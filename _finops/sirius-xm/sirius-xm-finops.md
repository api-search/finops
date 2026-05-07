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
  pricingCategory: Contact Sales
description: 'FOCUS-aligned FinOps placeholder for SiriusXM: no public API pricing or self-serve B2B catalog; spend and meters are determined by individual partner contracts.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sirius XM Holdings Inc.
  ProviderName: Sirius XM
  PublisherName: Sirius XM Holdings Inc.
  ServiceCategory: Audio Streaming / Advertising
  ServiceName: Sirius XM
layout: finops
meters:
- aggregation: sum
  description: Negotiated partner / API contract fees as itemized on the SiriusXM invoice.
  dimensions:
  - contract
  - product
  name: contract_fees
  unit: varies
name: Sirius Xm Finops
provider_name: Sirius XM
provider_slug: sirius-xm
publisher_name: Sirius XM Holdings Inc.
service_category: Audio Streaming / Advertising
slug: sirius-xm-finops
source_filename: sirius-xm-finops.yml
source_heading: FinOps Profile
source_url: https://www.siriusxm.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Sirius XM\nproviderId: sirius-xm\npublisherName: Sirius XM Holdings Inc.\nserviceCategory: Audio Streaming / Advertising\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Audio\n  - Advertising\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for SiriusXM: no public API pricing or self-serve\n  B2B catalog; spend and meters are determined by individual partner contracts.'\nsources:\n  - https://www.siriusxm.com/\nnotes: |\n  SiriusXM publishes consumer subscription pricing only. Pandora developer and AdsWizz partner APIs\n  use negotiated commercial terms, so meters and FOCUS columns below are stubs.\n\
  billingModel:\n  pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Sirius XM\n  ServiceCategory: Audio Streaming / Advertising\n  ProviderName: Sirius XM\n  PublisherName: Sirius XM Holdings Inc.\n  InvoiceIssuerName: Sirius XM Holdings Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    description: Negotiated partner / API contract fees as itemized on the SiriusXM invoice.\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - contract\n      - product\nprinciples:\n  - name: Visibility\n    description: Request usage exports from SiriusXM Media / AdsWizz account team; no self-serve\n      consumption dashboard is offered to partners.\n  - name: Allocation\n    description: Allocate per-contract fees to the consuming product line based on the line items\n      negotiated in the partner agreement.\n  - name: Optimization\n    description: Renegotiation cycle\
  \ is the primary lever; track delivered impressions / streams\n      against the contract minimum to inform renewal terms.\n  - name: Accountability\n    description: Partner-relationship owner reconciles monthly invoice line items against the signed\n      agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sirius-xm/refs/heads/main/finops/sirius-xm-finops.yml
sources:
- https://www.siriusxm.com/
specification: FinOps Framework
tags:
- Audio
- Advertising
- FinOps
- FOCUS
---
