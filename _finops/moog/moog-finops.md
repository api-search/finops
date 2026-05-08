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
  pricingCategory: Contract / Custom
description: Placeholder FinOps profile for Moog Inc. No public API billing surface or invoiced consumption API was located; any API consumption flows through Moog's standard commercial / OEM contract billing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Moog Inc.
  ProviderName: Moog
  PublisherName: Moog Inc.
  ServiceCategory: Aerospace / Industrial OEM
  ServiceName: Moog
layout: finops
meters:
- aggregation: sum
  dimensions:
  - contract
  name: contract_fees
  unit: month
name: Moog Finops
provider_name: Moog
provider_slug: moog
publisher_name: Moog Inc.
service_category: Aerospace / Industrial Motion Control
slug: moog-finops
source_filename: moog-finops.yml
source_heading: FinOps Profile
source_url: https://www.moog.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Moog\nproviderId: moog\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Aerospace\n  - Defense\n  - Industrial\n  - Medical\ndescription: Placeholder FinOps profile for Moog Inc. No public API billing surface or invoiced consumption\n  API was located; any API consumption flows through Moog's standard commercial / OEM contract billing.\nsources:\n  - https://www.moog.com\nnotes: Reconciliation deferred — populate when a public developer or billing portal is identified.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Moog Inc.\nserviceCategory: Aerospace / Industrial Motion Control\nbillingModel:\n  pricingCategory: Contract /\
  \ Custom\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Moog\n  ServiceCategory: Aerospace / Industrial OEM\n  ProviderName: Moog\n  PublisherName: Moog Inc.\n  InvoiceIssuerName: Moog Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Track Moog invoices in AP; no automated developer-platform telemetry is published.\n  - name: Allocation\n    description: Allocate Moog spend against the engineering program (aerospace, defense, industrial, medical)\n      consuming the underlying products or services.\n  - name: Optimization\n    description: Optimization is realized through commercial negotiation and program-level requirements,\n      not metered usage levers.\n  - name: Accountability\n    description: Procurement and the program lead reconcile Moog invoices;\
  \ no developer-platform chargeback\n      applies absent a public billing API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moog/refs/heads/main/finops/moog-finops.yml
sources:
- https://www.moog.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Aerospace
- Defense
- Industrial
- Medical
---
