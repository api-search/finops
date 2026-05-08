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
description: FOCUS-aligned FinOps placeholder for Encompass Health. The company does not publish public API pricing; FinOps integration would be defined under the partner contract and invoiced by the operating entity.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Encompass Health Corporation
  ProviderName: Encompass Health
  PublisherName: Encompass Health Corporation
  ServiceCategory: Healthcare Integration
  ServiceName: Encompass Health API
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
name: Encompass Health Finops
provider_name: Encompass Health
provider_slug: encompass-health
publisher_name: Encompass Health Corporation
service_category: Healthcare Integration
slug: encompass-health-finops
source_filename: encompass-health-finops.yml
source_heading: FinOps Profile
source_url: https://www.encompasshealth.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Encompass Health\nproviderId: encompass-health\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Healthcare\n  - Rehabilitation\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Encompass Health. The company does not publish public\n  API pricing; FinOps integration would be defined under the partner contract and invoiced by the operating\n  entity.\nnotes: No public billing or usage API was located. Meters and billing model below are scaffold values;\n  reconcile against a signed partner agreement before relying on them.\nsources:\n  - https://www.encompasshealth.com\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Encompass Health\
  \ Corporation\nserviceCategory: Healthcare Integration\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Encompass Health API\n  ServiceCategory: Healthcare Integration\n  ProviderName: Encompass Health\n  PublisherName: Encompass Health Corporation\n  InvoiceIssuerName: Encompass Health Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner\n  - name: contract_fee\n    unit: month\n    aggregation: sum\n    dimensions:\n      - partner\nprinciples:\n  - name: Visibility\n    description: Consumption visibility is delivered through partner reporting cadences agreed in the contract;\n      there is no public usage API.\n  - name: Allocation\n    description: Allocate cost by partner agreement, business\
  \ unit, and integration use case as defined\n      in the master services agreement.\n  - name: Optimization\n    description: Optimization levers are batching, caching, and renegotiating contract terms at renewal;\n      no public discount programs are documented.\n  - name: Accountability\n    description: The contracting business unit owns the spend; reviews follow the contract cadence with\n      the Encompass Health account team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/encompass-health/refs/heads/main/finops/encompass-health-finops.yml
sources:
- https://www.encompasshealth.com
specification: FinOps Framework
tags:
- Healthcare
- Rehabilitation
- FinOps
- FOCUS
---
