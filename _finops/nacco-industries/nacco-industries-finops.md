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
description: Placeholder FinOps profile for NACCO Industries (NACCO Natural Resources). No public API billing surface or invoiced consumption API was located.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: NACCO Industries, Inc.
  ProviderName: NACCO Industries
  PublisherName: NACCO Industries, Inc.
  ServiceCategory: Mining / Natural Resources
  ServiceName: NACCO Industries
layout: finops
meters:
- aggregation: sum
  dimensions:
  - subsidiary
  - contract
  name: contract_fees
  unit: month
name: Nacco Industries Finops
provider_name: NACCO Industries
provider_slug: nacco-industries
publisher_name: NACCO Industries, Inc.
service_category: Mining / Natural Resources
slug: nacco-industries-finops
source_filename: nacco-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.nacco.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: NACCO Industries\nproviderId: nacco-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Mining\n  - Natural Resources\n  - Energy\ndescription: Placeholder FinOps profile for NACCO Industries (NACCO Natural Resources). No public API\n  billing surface or invoiced consumption API was located.\nsources:\n  - https://www.nacco.com\nnotes: Reconciliation deferred — populate when a public developer or billing portal is identified.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: NACCO Industries, Inc.\nserviceCategory: Mining / Natural Resources\nbillingModel:\n  pricingCategory: Contract / Custom\n  billingFrequency: Per-Invoice\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: NACCO Industries\n  ServiceCategory: Mining / Natural Resources\n  ProviderName: NACCO Industries\n  PublisherName: NACCO Industries, Inc.\n  InvoiceIssuerName: NACCO Industries, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - subsidiary\n      - contract\nprinciples:\n  - name: Visibility\n    description: Track NACCO commercial invoices in AP; no automated usage telemetry is published.\n  - name: Allocation\n    description: Allocate spend by subsidiary (North American Coal, North American Mining, Mitigation Resources,\n      Catapult Mineral Management) and project.\n  - name: Optimization\n    description: Optimization happens through procurement / contract negotiation rather than metered API\n      usage controls.\n  - name: Accountability\n    description: Procurement and the operating-subsidiary\
  \ contract owner reconcile invoices.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nacco-industries/refs/heads/main/finops/nacco-industries-finops.yml
sources:
- https://www.nacco.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Mining
- Natural Resources
- Energy
---
