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
description: FOCUS-aligned FinOps placeholder for Ensign Group. The company does not publish public API pricing; cost is defined under the HIPAA partner agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The Ensign Group, Inc.
  ProviderName: Ensign Group
  PublisherName: The Ensign Group, Inc.
  ServiceCategory: Healthcare / Post-Acute Integration
  ServiceName: Ensign Group API
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
name: Ensign Group Finops
provider_name: Ensign Group
provider_slug: ensign-group
publisher_name: The Ensign Group, Inc.
service_category: Healthcare / Post-Acute Integration
slug: ensign-group-finops
source_filename: ensign-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.ensigngroup.net
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ensign Group\nproviderId: ensign-group\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Senior Living\n  - Healthcare\n  - Post-Acute\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Ensign Group. The company does not publish public API\n  pricing; cost is defined under the HIPAA partner agreement.\nnotes: No public billing or usage API was located. Reconcile against the signed Business Associate Agreement\n  and partner contract.\nsources:\n  - https://www.ensigngroup.net\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Ensign Group, Inc.\nserviceCategory: Healthcare / Post-Acute Integration\nbillingModel:\n  pricingCategory:\
  \ Contract / Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Ensign Group API\n  ServiceCategory: Healthcare / Post-Acute Integration\n  ProviderName: Ensign Group\n  PublisherName: The Ensign Group, Inc.\n  InvoiceIssuerName: The Ensign Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Visibility is delivered through partner reporting agreed in the BAA; no public usage API.\n  - name: Allocation\n    description: Allocate cost by partner agreement and operating subsidiary per the master services agreement.\n  - name: Optimization\n    description: Optimization levers are batching, caching,\
  \ and renegotiating partner terms at renewal.\n  - name: Accountability\n    description: The contracting partner owns spend; reviews follow contract cadence with the Ensign account\n      team and Privacy Officer.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ensign-group/refs/heads/main/finops/ensign-group-finops.yml
sources:
- https://www.ensigngroup.net
specification: FinOps Framework
tags:
- Senior Living
- Healthcare
- Post-Acute
- FinOps
- FOCUS
---
