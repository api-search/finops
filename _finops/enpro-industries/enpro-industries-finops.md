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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Contract / Negotiated
description: FOCUS-aligned FinOps placeholder for EnPro Industries. The company does not publish public API pricing; cost is defined under the partner contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Enpro Inc.
  ProviderName: EnPro Industries
  PublisherName: Enpro Inc.
  ServiceCategory: Industrial Manufacturing Integration
  ServiceName: EnPro Industries API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - partner
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - contract
  name: contract_fee
  unit: month
name: Enpro Industries Finops
provider_name: EnPro Industries
provider_slug: enpro-industries
publisher_name: Enpro Inc.
service_category: Industrial Manufacturing Integration
slug: enpro-industries-finops
source_filename: enpro-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.enproindustries.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: EnPro Industries\nproviderId: enpro-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Industrial\n  - Manufacturing\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for EnPro Industries. The company does not publish public\n  API pricing; cost is defined under the partner contract.\nnotes: No public billing or usage API was located. Reconcile against the signed partner agreement.\nsources:\n  - https://www.enproindustries.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Enpro Inc.\nserviceCategory: Industrial Manufacturing Integration\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Invoice\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: EnPro Industries API\n  ServiceCategory: Industrial Manufacturing Integration\n  ProviderName: EnPro Industries\n  PublisherName: Enpro Inc.\n  InvoiceIssuerName: Enpro Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Visibility is delivered through partner reporting and the monthly invoice; no public usage\n      API.\n  - name: Allocation\n    description: Allocate cost by partner agreement and EnPro segment (Sealing Technologies, Advanced Surface\n      Technologies) per the master services agreement.\n  - name: Optimization\n    description: Optimization levers are batching, EDI/integration\
  \ consolidation, and renegotiating contract\n      terms at renewal.\n  - name: Accountability\n    description: The contracting business unit owns spend; reviews follow the contract cadence with the\n      EnPro account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/enpro-industries/refs/heads/main/finops/enpro-industries-finops.yml
sources:
- https://www.enproindustries.com
specification: FinOps Framework
tags:
- Industrial
- Manufacturing
- FinOps
- FOCUS
---
