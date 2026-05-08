---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Order
  chargeCategories:
  - Purchase
  - Tax
  pricingCategory: Not Applicable (Goods)
description: Innospec is a specialty chemistry company (NASDAQ:IOSP); it does not deliver a public commercial API. There is no usage-based billing model to FOCUS-map. This artifact records the non-API nature of the provider rather than fabricating meters, and is retained for inventory completeness.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Innospec Inc.
  PricingCategory: Goods
  PricingUnit: not-applicable
  ProviderName: Innospec
  PublisherName: Innospec Inc.
  ServiceCategory: Specialty Chemicals (Non-API)
  ServiceName: Innospec Specialty Chemicals
layout: finops
meters: []
name: Innospec Finops
provider_name: Innospec
provider_slug: innospec
publisher_name: Innospec Inc.
service_category: Specialty Chemicals (Non-API)
slug: innospec-finops
source_filename: innospec-finops.yml
source_heading: FinOps Profile
source_url: https://www.innospec.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Innospec\nproviderId: innospec\npublisherName: Innospec Inc.\nserviceCategory: Specialty Chemicals (Non-API)\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Specialty Chemicals\n  - Fuel Additives\n  - FinOps\n  - FOCUS\ndescription: Innospec is a specialty chemistry company (NASDAQ:IOSP); it does not deliver a public commercial\n  API. There is no usage-based billing model to FOCUS-map. This artifact records the non-API nature of\n  the provider rather than fabricating meters, and is retained for inventory completeness.\nnotes: Innospec is not an API provider; meters and FOCUS columns are placeholders reflecting that\
  \ there\n  is no API-level cost data to allocate. Reconcile flag is false to signal \"no applicable API billing\n  surface\".\nsources:\n  - https://www.innospec.com/\nprinciples:\n  - name: Not Applicable\n    description: Innospec does not operate an API surface; no API-cost FinOps practice applies.\nbillingModel:\n  pricingCategory: Not Applicable (Goods)\n  billingFrequency: Per-Order\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\nfocusColumns:\n  ServiceName: Innospec Specialty Chemicals\n  ServiceCategory: Specialty Chemicals (Non-API)\n  ProviderName: Innospec\n  PublisherName: Innospec Inc.\n  InvoiceIssuerName: Innospec Inc.\n  PricingCategory: Goods\n  PricingUnit: not-applicable\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters: []\napis: []\nunitEconomics: []\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/innospec/refs/heads/main/finops/innospec-finops.yml
sources:
- https://www.innospec.com/
specification: FinOps Framework
tags:
- Specialty Chemicals
- Fuel Additives
- FinOps
- FOCUS
---
