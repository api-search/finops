---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Tariff
  chargeCategories:
  - Purchase
  pricingCategory: Not Applicable (Regulated Utility)
description: FOCUS-aligned FinOps placeholder for South Jersey Industries. SJI is a regulated natural-gas utility holding company with no developer billing surface; this artifact captures the publisher entity only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: South Jersey Gas / Elizabethtown Gas
  ProviderName: South Jersey Industries
  PublisherName: South Jersey Industries, Inc.
  ServiceCategory: Regulated Natural Gas Utility
  ServiceName: South Jersey Industries Utility Service
layout: finops
meters: []
name: South Jersey Industries Finops
provider_name: South Jersey Industries
provider_slug: south-jersey-industries
publisher_name: South Jersey Industries, Inc.
service_category: Regulated Natural Gas Utility
slug: south-jersey-industries-finops
source_filename: south-jersey-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.sjindustries.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: South Jersey Industries\nproviderId: south-jersey-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Utilities\n  - Natural Gas\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for South Jersey Industries. SJI is a regulated natural-gas\n  utility holding company with no developer billing surface; this artifact captures the publisher entity\n  only.'\nsources:\n  - https://www.sjindustries.com/\nnotes: SJI does not expose a public developer API or usage-based billing surface. Meters cannot be reconciled\n  because there are no published API consumption units. Customer-facing rates are utility tariffs filed\n  with state regulators rather than FinOps meters.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: South Jersey Industries, Inc.\nserviceCategory: Regulated Natural Gas Utility\nbillingModel:\n  pricingCategory: Not Applicable (Regulated Utility)\n  billingFrequency: Per-Tariff\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: South Jersey Industries Utility Service\n  ServiceCategory: Regulated Natural Gas Utility\n  ProviderName: South Jersey Industries\n  PublisherName: South Jersey Industries, Inc.\n  InvoiceIssuerName: South Jersey Gas / Elizabethtown Gas\n  BillingCurrency: USD\nmeters: []\nprinciples:\n  - name: Visibility\n    description: Not applicable on a developer surface; gas-service consumption is metered at the customer\n      premise and reported on the utility bill, not via an API.\n  - name: Allocation\n    description: Not applicable - SJI is a regulated utility holding company without developer/tenant\n      cost-allocation semantics.\n  -\
  \ name: Optimization\n    description: Not applicable at the API/FinOps layer.\n  - name: Accountability\n    description: Customer-level accountability is governed by the utility tariff and the New Jersey Board\n      of Public Utilities, not by a developer/tenant contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/south-jersey-industries/refs/heads/main/finops/south-jersey-industries-finops.yml
sources:
- https://www.sjindustries.com/
specification: FinOps Framework
tags:
- Utilities
- Natural Gas
- FinOps
- FOCUS
---
