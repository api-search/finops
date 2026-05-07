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
description: FOCUS-aligned FinOps placeholder for Ennis Inc. The company does not publish public API pricing; cost is defined under the distributor/partner contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ennis, Inc.
  ProviderName: Ennis Inc
  PublisherName: Ennis, Inc.
  ServiceCategory: Print & Forms Integration
  ServiceName: Ennis Inc API
layout: finops
meters:
- aggregation: sum
  dimensions:
  - endpoint
  - distributor
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - product
  - distributor
  name: print_orders
  unit: order
- aggregation: sum
  dimensions:
  - contract
  name: contract_fee
  unit: month
name: Ennis Finops
provider_name: Ennis Inc
provider_slug: ennis
publisher_name: Ennis, Inc.
service_category: Print & Forms Integration
slug: ennis-finops
source_filename: ennis-finops.yml
source_heading: FinOps Profile
source_url: https://www.ennis.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ennis Inc\nproviderId: ennis\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Business Forms\n  - Printing\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Ennis Inc. The company does not publish public API pricing;\n  cost is defined under the distributor/partner contract.\nnotes: No public billing or usage API was located. Reconcile against the signed distributor agreement.\nsources:\n  - https://www.ennis.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ennis, Inc.\nserviceCategory: Print & Forms Integration\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Ennis Inc API\n  ServiceCategory: Print & Forms Integration\n  ProviderName: Ennis Inc\n  PublisherName: Ennis, Inc.\n  InvoiceIssuerName: Ennis, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - distributor\n  - name: print_orders\n    unit: order\n    aggregation: sum\n    dimensions:\n      - product\n      - distributor\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - contract\nprinciples:\n  - name: Visibility\n    description: Visibility is delivered through distributor reporting and the monthly invoice; no public\n      usage API.\n  - name: Allocation\n    description: Allocate cost by distributor and product line per the distributor agreement.\n  - name: Optimization\n    description: Optimization levers are order batching,\
  \ plate reuse, and renegotiating distributor terms.\n  - name: Accountability\n    description: The contracting distributor owns spend; reviews follow the agreement cadence with the\n      Ennis account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ennis/refs/heads/main/finops/ennis-finops.yml
sources:
- https://www.ennis.com
specification: FinOps Framework
tags:
- Business Forms
- Printing
- FinOps
- FOCUS
---
