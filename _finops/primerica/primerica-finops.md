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
description: FOCUS-aligned FinOps shape for Primerica. No public API or usage-billing surface exists; any cost flow is governed by partner contracts.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Primerica, Inc.
  ProviderName: Primerica
  PublisherName: Primerica, Inc.
  ServiceCategory: Financial Services
  ServiceName: Primerica
layout: finops
meters:
- aggregation: sum
  name: contract_fees
  unit: varies
name: Primerica Finops
provider_name: Primerica
provider_slug: primerica
publisher_name: Primerica, Inc.
service_category: Financial Services
slug: primerica-finops
source_filename: primerica-finops.yml
source_heading: FinOps Profile
source_url: https://www.primerica.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Primerica\nproviderId: primerica\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Insurance\n  - Financial Services\n  - Life Insurance\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Primerica. No public API or usage-billing surface exists;\n  any cost flow is governed by partner contracts.\nnotes: No public billing or usage telemetry. The FinOps record is a placeholder pointing at contract-driven\n  cost rather than a metered API surface.\nsources:\n  - https://www.primerica.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Primerica, Inc.\nserviceCategory: Financial Services\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency:\
  \ Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Primerica\n  ServiceCategory: Financial Services\n  ProviderName: Primerica\n  PublisherName: Primerica, Inc.\n  InvoiceIssuerName: Primerica, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: contract_fees\n    unit: varies\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: No public usage telemetry; cost visibility flows from contract invoices and partner\n      reporting only.\n  - name: Allocation\n    description: Allocate by partner agreement and integration scope; no per-call attribution surface\n      is published.\n  - name: Optimization\n    description: Optimization is contractual — renegotiate volume, scope, and SLA at renewal; no public\n      autoscaling or commitment levers exist.\n  - name: Accountability\n    description: Spend is owned by the partnership / business-development relationship, not by an engineering\n      consumption budget.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/primerica/refs/heads/main/finops/primerica-finops.yml
sources:
- https://www.primerica.com/
specification: FinOps Framework
tags:
- Insurance
- Financial Services
- Life Insurance
- FinOps
- FOCUS
---
