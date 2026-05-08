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
description: FOCUS-aligned FinOps placeholder for Energizer Holdings. The company does not publish public API pricing; integration cost is defined under the partner contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Energizer Holdings, Inc.
  ProviderName: Energizer Holdings
  PublisherName: Energizer Holdings, Inc.
  ServiceCategory: Consumer Products Integration
  ServiceName: Energizer Holdings API
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
  - partner
  name: contract_fee
  unit: month
name: Energizer Holdings Finops
provider_name: Energizer Holdings
provider_slug: energizer-holdings
publisher_name: Energizer Holdings, Inc.
service_category: Consumer Products Integration
slug: energizer-holdings-finops
source_filename: energizer-holdings-finops.yml
source_heading: FinOps Profile
source_url: https://www.energizer.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Energizer Holdings\nproviderId: energizer-holdings\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Consumer Products\n  - Batteries\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Energizer Holdings. The company does not publish public\n  API pricing; integration cost is defined under the partner contract.\nnotes: No public billing or usage API was located. Reconcile against the signed partner agreement.\nsources:\n  - https://www.energizer.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Energizer Holdings, Inc.\nserviceCategory: Consumer Products Integration\nbillingModel:\n  pricingCategory: Contract / Negotiated\n \
  \ billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Energizer Holdings API\n  ServiceCategory: Consumer Products Integration\n  ProviderName: Energizer Holdings\n  PublisherName: Energizer Holdings, Inc.\n  InvoiceIssuerName: Energizer Holdings, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Consumption visibility is delivered through partner reporting agreed in the contract;\n      no public usage API.\n  - name: Allocation\n    description: Allocate cost by partner agreement and business unit per the master services agreement.\n  - name: Optimization\n    description: Optimization levers are batching, caching,\
  \ and renegotiating contract terms at renewal.\n  - name: Accountability\n    description: The contracting business unit owns spend; reviews follow contract cadence with the Energizer\n      account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/energizer-holdings/refs/heads/main/finops/energizer-holdings-finops.yml
sources:
- https://www.energizer.com
specification: FinOps Framework
tags:
- Consumer Products
- Batteries
- FinOps
- FOCUS
---
