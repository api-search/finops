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
description: 'FOCUS-aligned FinOps placeholder for Snap-on: not a software / API vendor; tooling and diagnostics products ship as physical hardware plus bundled software, with no public API invoice-line catalog.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Snap-on Incorporated
  ProviderName: Snap-on
  PublisherName: Snap-on Incorporated
  ServiceCategory: Tools / Diagnostics
  ServiceName: Snap-on
layout: finops
meters:
- aggregation: sum
  description: Snap-on does not bill API consumption.
  dimensions: []
  name: not_applicable
  unit: varies
name: Snap On Finops
provider_name: Snap-on
provider_slug: snap-on
publisher_name: Snap-on Incorporated
service_category: Tools / Diagnostics
slug: snap-on-finops
source_filename: snap-on-finops.yml
source_heading: FinOps Profile
source_url: https://www.snapon.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Snap-on\nproviderId: snap-on\npublisherName: Snap-on Incorporated\nserviceCategory: Tools / Diagnostics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Tools\n  - Diagnostics\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Snap-on: not a software / API vendor; tooling and\n  diagnostics products ship as physical hardware plus bundled software, with no public API\n  invoice-line catalog.'\nsources:\n  - https://www.snapon.com\nnotes: |\n  Not a software / API vendor. Retained as a placeholder for catalog completeness only.\nbillingModel:\n  pricingCategory: Not Applicable\n  billingFrequency:\
  \ Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Snap-on\n  ServiceCategory: Tools / Diagnostics\n  ProviderName: Snap-on\n  PublisherName: Snap-on Incorporated\n  InvoiceIssuerName: Snap-on Incorporated\n  BillingCurrency: USD\nmeters:\n  - name: not_applicable\n    description: Snap-on does not bill API consumption.\n    unit: varies\n    aggregation: sum\n    dimensions: []\nprinciples:\n  - name: Visibility\n    description: Not applicable - Snap-on is a physical tool / diagnostics manufacturer, not an API\n      vendor.\n  - name: Allocation\n    description: Not applicable.\n  - name: Optimization\n    description: Not applicable.\n  - name: Accountability\n    description: Not applicable.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/snap-on/refs/heads/main/finops/snap-on-finops.yml
sources:
- https://www.snapon.com
specification: FinOps Framework
tags:
- Tools
- Diagnostics
- FinOps
- FOCUS
---
