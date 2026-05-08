---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD/EUR/JPY (varies)
  billingFrequency: Per-Purchase-Order
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable (Hardware Supplier)
description: FinOps is not applicable to Autoliv — it is a tier-1 automotive safety hardware supplier with no public API surface. Commerce with Autoliv is per-PO/per-program, governed by OEM contracts.
focus_columns:
  BillingCurrency: USD
  PricingCategory: Not Applicable
  ProviderName: Autoliv
  PublisherName: Autoliv, Inc.
  ServiceCategory: Automotive Manufacturing
  ServiceName: Autoliv
layout: finops
meters:
- aggregation: count
  description: No API metering; hardware is shipped per purchase order
  name: not_applicable
  unit: varies
name: Autoliv Finops
provider_name: Autoliv
provider_slug: autoliv
publisher_name: Autoliv, Inc.
service_category: Automotive Safety / Tier-1 Supplier
slug: autoliv-finops
source_filename: autoliv-finops.yml
source_heading: FinOps Profile
source_url: https://www.autoliv.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Autoliv\nproviderId: autoliv\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automotive\n  - Automotive Safety\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: FinOps is not applicable to Autoliv — it is a tier-1 automotive safety hardware supplier\n  with no public API surface. Commerce with Autoliv is per-PO/per-program, governed by OEM contracts.\nsources:\n  - https://www.autoliv.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nnotes: No API billing. Hardware programs are billed under OEM purchase orders.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Autoliv, Inc.\nserviceCategory: Automotive Safety / Tier-1 Supplier\nbillingModel:\n\
  \  pricingCategory: Not Applicable (Hardware Supplier)\n  billingFrequency: Per-Purchase-Order\n  billingCurrency: USD/EUR/JPY (varies)\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Autoliv\n  ServiceCategory: Automotive Manufacturing\n  ProviderName: Autoliv\n  PublisherName: Autoliv, Inc.\n  BillingCurrency: USD\n  PricingCategory: Not Applicable\nmeters:\n  - name: not_applicable\n    description: No API metering; hardware is shipped per purchase order\n    unit: varies\n    aggregation: count\nprinciples:\n  - name: Visibility\n    description: Not applicable to API.\n  - name: Allocation\n    description: Not applicable to API.\n  - name: Optimization\n    description: Not applicable to API.\n  - name: Accountability\n    description: Not applicable to API.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autoliv/refs/heads/main/finops/autoliv-finops.yml
sources:
- https://www.autoliv.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Automotive
- Automotive Safety
- Manufacturing
- FinOps
- FOCUS
---
