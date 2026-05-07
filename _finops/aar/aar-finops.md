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
  pricingCategory: Contract
description: AAR's API surface is delivered as part of MRO services contracts and software product licenses (Trax, Aerostrat, Airinmar). There is no metered API invoice. FinOps mapping is structural only.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: AAR Corp.
  ProviderName: AAR Corp
  PublisherName: AAR Corp.
  ServiceCategory: Aerospace / MRO
  ServiceName: AAR Corp
layout: finops
meters:
- aggregation: count
  description: MRO services or software license contract — not a metered API unit.
  dimensions:
  - customer
  - product
  name: customer_contract
  unit: contract
name: Aar Finops
provider_name: AAR Corp
provider_slug: aar
publisher_name: AAR Corp.
service_category: Aerospace / MRO
slug: aar-finops
source_filename: aar-finops.yml
source_heading: FinOps Profile
source_url: https://www.aarcorp.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AAR Corp\nproviderId: aar\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Aviation\n  - MRO\n  - Aerospace\n  - FinOps\n  - FOCUS\ndescription: AAR's API surface is delivered as part of MRO services contracts and software product licenses\n  (Trax, Aerostrat, Airinmar). There is no metered API invoice. FinOps mapping is structural only.\nnotes: No public developer pricing — placeholder only. Costs flow through MRO service contracts and software\n  licenses, not a metered API line item.\nsources:\n  - https://www.aarcorp.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AAR Corp.\nserviceCategory: Aerospace / MRO\nbillingModel:\n  pricingCategory:\
  \ Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: AAR Corp\n  ServiceCategory: Aerospace / MRO\n  ProviderName: AAR Corp\n  PublisherName: AAR Corp.\n  InvoiceIssuerName: AAR Corp.\n  BillingCurrency: USD\nmeters:\n  - name: customer_contract\n    description: MRO services or software license contract — not a metered API unit.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - customer\n      - product\nprinciples:\n  - name: Visibility\n    description: Track integration cost as part of MRO operations spend; AAR does not provide a metered\n      API usage feed.\n  - name: Allocation\n    description: Allocate cost to the fleet operations or maintenance program that owns the AAR contract.\n  - name: Optimization\n    description: Optimize integration usage by aligning queries with maintenance cycles and using batched\n      parts requests where the contract allows.\n  - name: Accountability\n\
  \    description: Maintenance / operations leadership owns the AAR relationship; IT owns runtime. Review\n      activity at quarterly fleet reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aar/refs/heads/main/finops/aar-finops.yml
sources:
- https://www.aarcorp.com
specification: FinOps Framework
tags:
- Aviation
- MRO
- Aerospace
- FinOps
- FOCUS
---
