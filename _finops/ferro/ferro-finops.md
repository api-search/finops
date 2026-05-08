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
  - Tax
  - Adjustment
  pricingCategory: Procurement (Not API-Billed)
description: FOCUS-aligned FinOps stub for Ferro Corporation. The legacy Ferro brand was merged into Vibrantz Technologies in 2022 and there is no public developer API or developer marketplace. Cost related to Ferro/Vibrantz materials is procurement spend on raw chemicals/materials, not API consumption. This artifact captures only the API-FinOps shape, which is effectively N/A.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Vibrantz Technologies
  PricingCategory: Procurement
  PricingUnit: not applicable
  ProviderName: Vibrantz Technologies
  PublisherName: Vibrantz Technologies
  ServiceCategory: Specialty Chemicals
  ServiceName: Ferro / Vibrantz Materials
layout: finops
meters: []
name: Ferro Finops
provider_name: Ferro Corporation
provider_slug: ferro
publisher_name: Vibrantz Technologies (former Ferro Corporation)
service_category: Specialty Chemicals / Materials
slug: ferro-finops
source_filename: ferro-finops.yml
source_heading: FinOps Profile
source_url: https://vibrantz.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ferro Corporation\nproviderId: ferro\npublisherName: Vibrantz Technologies (former Ferro Corporation)\nserviceCategory: Specialty Chemicals / Materials\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Functional Materials\n  - Electronics\n  - Chemical\n  - Acquired\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps stub for Ferro Corporation. The legacy Ferro brand was merged into\n  Vibrantz Technologies in 2022 and there is no public developer API or developer marketplace. Cost related\n  to Ferro/Vibrantz materials is procurement spend on raw chemicals/materials, not API consumption. This\n  artifact captures only the API-FinOps\
  \ shape, which is effectively N/A.'\nnotes: No public API; FinOps is procurement-driven, not API-consumption-driven. Retained as a stub.\nsources:\n  - https://vibrantz.com/\nprinciples:\n  - name: Visibility\n    description: Not applicable to API consumption; visibility lives in the procurement system that records\n      raw-material POs from Vibrantz.\n  - name: Allocation\n    description: Allocation occurs at the BOM / cost-center level in the customer's ERP, not via API meters.\n  - name: Optimization\n    description: Optimization is a procurement function (volume contracts, supplier consolidation), not\n      API engineering.\n  - name: Accountability\n    description: Procurement / supply chain owns supplier relationship; no API budget owner exists.\nbillingModel:\n  pricingCategory: Procurement (Not API-Billed)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Ferro / Vibrantz\
  \ Materials\n  ServiceCategory: Specialty Chemicals\n  ProviderName: Vibrantz Technologies\n  PublisherName: Vibrantz Technologies\n  InvoiceIssuerName: Vibrantz Technologies\n  PricingCategory: Procurement\n  PricingUnit: not applicable\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters: []\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ferro/refs/heads/main/finops/ferro-finops.yml
sources:
- https://vibrantz.com/
specification: FinOps Framework
tags:
- Functional Materials
- Electronics
- Chemical
- Acquired
- FinOps
- Cost Management
- FOCUS
---
