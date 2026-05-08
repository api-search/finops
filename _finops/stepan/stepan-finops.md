---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: Stepan Company has no public, metered API surface. Costs land inside the broader B2B customer relationship (orders, product specs, SDS), not as a per-call API line; nothing public to reconcile against the FOCUS spec.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Stepan Company
  ProviderName: Stepan Company
  PublisherName: Stepan Company
  ServiceCategory: Specialty Chemicals / Manufacturing
  ServiceName: Stepan Company
layout: finops
meters:
- aggregation: sum
  description: Placeholder for line items defined in a Stepan customer / B2B contract.
  name: contracted_engagement
  unit: varies
name: Stepan Finops
provider_name: Stepan Company
provider_slug: stepan
publisher_name: Stepan Company
service_category: Specialty Chemicals / Manufacturing
slug: stepan-finops
source_filename: stepan-finops.yml
source_heading: FinOps Profile
source_url: https://www.stepan.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Stepan Company\nproviderId: stepan\npublisherName: Stepan Company\nserviceCategory: Specialty Chemicals / Manufacturing\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Specialty Chemicals\ndescription: Stepan Company has no public, metered API surface. Costs land inside the broader B2B\n  customer relationship (orders, product specs, SDS), not as a per-call API line; nothing public to\n  reconcile against the FOCUS spec.\nsources:\n  - https://www.stepan.com/\nnotes: No public Stepan API billing surface. Meters and FOCUS columns are placeholders pending a\n  contracted engagement.\nbillingModel:\n\
  \  pricingCategory: Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Stepan Company\n  ServiceCategory: Specialty Chemicals / Manufacturing\n  ProviderName: Stepan Company\n  PublisherName: Stepan Company\n  InvoiceIssuerName: Stepan Company\n  BillingCurrency: USD\nmeters:\n  - name: contracted_engagement\n    description: Placeholder for line items defined in a Stepan customer / B2B contract.\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility is whatever order / SDS / product-data reporting Stepan provides through\n      the customer relationship — there is no public API usage feed.\n  - name: Allocation\n    description: Allocate Stepan-related data and integration cost in your own ERP / procurement system\n      against the underlying chemical-supply contract.\n  - name: Optimization\n    description: Optimization happens via supplier / contract\
  \ negotiation, not via API plan changes.\n  - name: Accountability\n    description: A procurement / supply-chain owner should hold the Stepan engagement cost line and\n      renewal cycle.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stepan/refs/heads/main/finops/stepan-finops.yml
sources:
- https://www.stepan.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Specialty Chemicals
---
