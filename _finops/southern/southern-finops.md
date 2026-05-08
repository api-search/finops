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
description: FOCUS-aligned FinOps placeholder for Southern Company. Southern is a regulated electric and gas utility holding company with no developer billing surface; this artifact captures the publisher entity only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Alabama Power / Georgia Power / Mississippi Power / Southern Company Gas
  ProviderName: Southern Company
  PublisherName: The Southern Company
  ServiceCategory: Regulated Electric and Gas Utility
  ServiceName: Southern Company Utility Service
layout: finops
meters: []
name: Southern Finops
provider_name: Southern Company
provider_slug: southern
publisher_name: The Southern Company
service_category: Regulated Electric and Gas Utility
slug: southern-finops
source_filename: southern-finops.yml
source_heading: FinOps Profile
source_url: https://www.southerncompany.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Southern Company\nproviderId: southern\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Electric Utility\n  - Energy\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for Southern Company. Southern is a regulated electric\n  and gas utility holding company with no developer billing surface; this artifact captures the publisher\n  entity only.'\nsources:\n  - https://www.southerncompany.com/\nnotes: Southern Company does not expose a public developer API or usage-based billing surface. Meters\n  cannot be reconciled because there are no published API consumption units. Customer rates are utility\n  tariffs filed with state regulators rather than FinOps meters.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n \
  \ dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Southern Company\nserviceCategory: Regulated Electric and Gas Utility\nbillingModel:\n  pricingCategory: Not Applicable (Regulated Utility)\n  billingFrequency: Per-Tariff\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Southern Company Utility Service\n  ServiceCategory: Regulated Electric and Gas Utility\n  ProviderName: Southern Company\n  PublisherName: The Southern Company\n  InvoiceIssuerName: Alabama Power / Georgia Power / Mississippi Power / Southern Company Gas\n  BillingCurrency: USD\nmeters: []\nprinciples:\n  - name: Visibility\n    description: Not applicable on a developer surface; electric and gas consumption is metered at the\n      customer premise and reported on the utility bill, not via an API.\n  - name: Allocation\n    description: Not applicable - Southern Company is a regulated utility holding company without developer/tenant\n     \
  \ cost-allocation semantics.\n  - name: Optimization\n    description: Not applicable at the API/FinOps layer.\n  - name: Accountability\n    description: Customer-level accountability is governed by the regulated utility tariff and the relevant\n      state public service commission, not by a developer/tenant contract.\nmaintainers:\n  - FN: API Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/southern/refs/heads/main/finops/southern-finops.yml
sources:
- https://www.southerncompany.com/
specification: FinOps Framework
tags:
- Electric Utility
- Energy
- FinOps
- FOCUS
---
