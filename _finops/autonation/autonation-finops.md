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
  pricingCategory: Bilateral Contract
description: AutoNation does not publish a public API or developer pricing. There is no FinOps surface to align with.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AutoNation, Inc.
  ProviderName: AutoNation
  PublisherName: AutoNation, Inc.
  ServiceCategory: Automotive Retail
  ServiceName: AutoNation
layout: finops
meters:
- aggregation: sum
  name: bilateral_integration
  unit: varies
name: Autonation Finops
provider_name: AutoNation
provider_slug: autonation
publisher_name: AutoNation, Inc.
service_category: Automotive Retail
slug: autonation-finops
source_filename: autonation-finops.yml
source_heading: FinOps Profile
source_url: https://www.autonation.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AutoNation\nproviderId: autonation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: AutoNation has no public API and no published developer pricing. This FinOps artifact is a\n  shell capturing the absence of a public commercial API surface.\ntags:\n  - FinOps\n  - FOCUS\n  - Automotive\n  - Retail\ndescription: AutoNation does not publish a public API or developer pricing. There is no FinOps surface\n  to align with.\nsources:\n  - https://www.autonation.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AutoNation, Inc.\nserviceCategory: Automotive Retail\nbillingModel:\n  pricingCategory: Bilateral Contract\n  billingFrequency: Per-Invoice\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: AutoNation\n  ServiceCategory: Automotive Retail\n  ProviderName: AutoNation\n  PublisherName: AutoNation, Inc.\n  InvoiceIssuerName: AutoNation, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: bilateral_integration\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: There is no public AutoNation usage API. Any reporting comes from the partner DMS or\n      OEM data feed.\n  - name: Allocation\n    description: Allocate via the partner integration contract; AutoNation is not a billed service for\n      most third parties.\n  - name: Optimization\n    description: Optimization, where applicable, is for the consuming integrator, not AutoNation.\n  - name: Accountability\n    description: Owned by the dealer-integration / partnerships team that manages the bilateral\n      agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/autonation/refs/heads/main/finops/autonation-finops.yml
sources:
- https://www.autonation.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Automotive
- Retail
---
