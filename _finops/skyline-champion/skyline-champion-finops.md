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
  pricingCategory: Not Applicable
description: 'FOCUS-aligned FinOps placeholder for Skyline Champion: no public API or programmatic pricing surface; this provider is a building-products manufacturer rather than a software vendor.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Skyline Champion Corporation
  ProviderName: Skyline Champion
  PublisherName: Skyline Champion Corporation
  ServiceCategory: Manufactured Housing
  ServiceName: Skyline Champion
layout: finops
meters:
- aggregation: sum
  description: Skyline Champion does not bill API consumption; physical product invoicing is outside the scope of this FinOps catalog.
  dimensions: []
  name: not_applicable
  unit: varies
name: Skyline Champion Finops
provider_name: Skyline Champion
provider_slug: skyline-champion
publisher_name: Skyline Champion Corporation
service_category: Manufactured Housing
slug: skyline-champion-finops
source_filename: skyline-champion-finops.yml
source_heading: FinOps Profile
source_url: https://ir.skylinechampion.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Skyline Champion\nproviderId: skyline-champion\npublisherName: Skyline Champion Corporation\nserviceCategory: Manufactured Housing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Manufactured Housing\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Skyline Champion: no public API or programmatic\n  pricing surface; this provider is a building-products manufacturer rather than a software vendor.'\nsources:\n  - https://ir.skylinechampion.com/\nnotes: |\n  Not a software / API vendor. No invoice-line catalog applicable; retained as a placeholder for\n  catalog completeness only.\nbillingModel:\n\
  \  pricingCategory: Not Applicable\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Skyline Champion\n  ServiceCategory: Manufactured Housing\n  ProviderName: Skyline Champion\n  PublisherName: Skyline Champion Corporation\n  InvoiceIssuerName: Skyline Champion Corporation\n  BillingCurrency: USD\nmeters:\n  - name: not_applicable\n    description: Skyline Champion does not bill API consumption; physical product invoicing is\n      outside the scope of this FinOps catalog.\n    unit: varies\n    aggregation: sum\n    dimensions: []\nprinciples:\n  - name: Visibility\n    description: Not applicable - no API consumption telemetry exists for a manufactured-housing\n      producer.\n  - name: Allocation\n    description: Not applicable.\n  - name: Optimization\n    description: Not applicable.\n  - name: Accountability\n    description: Not applicable.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/skyline-champion/refs/heads/main/finops/skyline-champion-finops.yml
sources:
- https://ir.skylinechampion.com/
specification: FinOps Framework
tags:
- Manufactured Housing
- FinOps
- FOCUS
---
