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
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Aptiv. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aptiv PLC
  ProviderName: Aptiv
  PublisherName: Aptiv PLC
  ServiceCategory: Automotive / Mobility Tech
  ServiceName: Aptiv
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Aptiv Finops
provider_name: Aptiv
provider_slug: aptiv
publisher_name: Aptiv PLC
service_category: Industrial / Automotive
slug: aptiv-finops
source_filename: aptiv-finops.yml
source_heading: FinOps Profile
source_url: https://www.aptiv.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aptiv\nproviderId: aptiv\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Automotive\n- Electrical Systems\n- Technology\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Aptiv. No public billing-model details, meters, or invoice\n  schema are published; this artifact records the absence so consumers know to source commercial terms\n  from the provider directly.\nnotes: Aptiv does not publish a public developer pricing page. The developer.aptiv.com host did not respond\n  when probed; commercial terms for any platform integrations are negotiated directly.\nsources:\n- https://www.aptiv.com\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aptiv PLC\nserviceCategory: Industrial / Automotive\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Aptiv\n  ServiceCategory: Automotive / Mobility Tech\n  ProviderName: Aptiv\n  PublisherName: Aptiv PLC\n  InvoiceIssuerName: Aptiv PLC\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n- name: Visibility\n  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and\
  \ load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aptiv/refs/heads/main/finops/aptiv-finops.yml
sources:
- https://www.aptiv.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Automotive
- Electrical Systems
- Technology
- FinOps
- Cost Management
- FOCUS
---
