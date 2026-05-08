---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (varies by contract)
  billingFrequency: Per-Contract
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Contract / Negotiated
description: 'FOCUS-aligned FinOps shape for SLB (Schlumberger) digital platform APIs: enterprise software licensed via SLB Digital Platform Partner Program / direct sales. Costs are negotiated under the master agreement; no public unit pricing.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SLB (Schlumberger Limited)
  ProviderName: SLB (Schlumberger)
  PublisherName: SLB (Schlumberger Limited)
  ServiceCategory: Energy Services
  ServiceName: SLB (Schlumberger)
layout: finops
meters:
- aggregation: sum
  name: contracted_consumption
  unit: varies
name: Schlumberger Finops
provider_name: SLB (Schlumberger)
provider_slug: schlumberger
publisher_name: SLB (Schlumberger Limited)
service_category: Energy Services
slug: schlumberger-finops
source_filename: schlumberger-finops.yml
source_heading: FinOps Profile
source_url: https://www.slb.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SLB (Schlumberger)\nproviderId: schlumberger\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- FinOps\n- FOCUS\n- Energy\n- Enterprise\ndescription: 'FOCUS-aligned FinOps shape for SLB (Schlumberger) digital platform APIs: enterprise software\n  licensed via SLB Digital Platform Partner Program / direct sales. Costs are negotiated under the master\n  agreement; no public unit pricing.'\nnotes: SLB (Schlumberger) is an energy services and software vendor; platform / digital APIs (e.g. DELFI,\n  OSDU-aligned services) are sold via the SLB Digital Platform Partner Program and enterprise sales engagement.\n  There is no public self-service pricing page.\nsources:\n- https://www.slb.com/\n- https://software.slb.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n\
  \  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SLB (Schlumberger Limited)\nserviceCategory: Energy Services\nbillingModel:\n  pricingCategory: Contract / Negotiated\n  billingFrequency: Per-Contract\n  billingCurrency: USD (varies by contract)\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: SLB (Schlumberger)\n  ServiceCategory: Energy Services\n  ProviderName: SLB (Schlumberger)\n  PublisherName: SLB (Schlumberger Limited)\n  InvoiceIssuerName: SLB (Schlumberger Limited)\n  BillingCurrency: USD\nmeters:\n- name: contracted_consumption\n  unit: varies\n  aggregation: sum\nprinciples:\n- name: Visibility\n  description: Consumption visibility comes from the SLB (Schlumberger) account / partner reporting surface\n    (invoices, account dashboards) rather than a public usage API.\n- name: Allocation\n  description: Allocate cost through the SLB (Schlumberger) contract structure (entitlement,\
  \ project,\n    business unit) and reconcile against internal cost centers.\n- name: Optimization\n  description: 'Optimization levers are commercial: renegotiation cadence, commitment sizing, and consolidation\n    of SLB (Schlumberger) entitlements.'\n- name: Accountability\n  description: Assign a contract owner who reconciles SLB (Schlumberger) invoices against contracted entitlements\n    each billing cycle.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n  url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/schlumberger/refs/heads/main/finops/schlumberger-finops.yml
sources:
- https://www.slb.com/
- https://software.slb.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Energy
- Enterprise
---
