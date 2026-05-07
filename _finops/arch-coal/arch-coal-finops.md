---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: arch-coal-investor-relations-api.yaml
  format: yaml
  label: Arch Coal Investor Relations
  slug: arch-coal-investor-relations
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/arch-coal/refs/heads/main/openapi/arch-coal-investor-relations-api.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Arch Coal. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Arch Resources, Inc.
  ProviderName: Arch Coal
  PublisherName: Arch Resources, Inc.
  ServiceCategory: Mining / Coal
  ServiceName: Arch Coal
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Arch Coal Finops
provider_name: Arch Coal
provider_slug: arch-coal
publisher_name: Arch Resources, Inc.
service_category: Industrial / Mining
slug: arch-coal-finops
source_filename: arch-coal-finops.yml
source_heading: FinOps Profile
source_url: https://archresources.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Arch Coal\nproviderId: arch-coal\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Mining\n- Coal\n- Metallurgical Coal\n- Thermal Coal\n- Energy\n- Fortune 500\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Arch Coal. No public billing-model details, meters,\n  or invoice schema are published; this artifact records the absence so consumers know to source commercial\n  terms from the provider directly.\nnotes: Arch Coal (now Arch Resources) does not operate a commercial API program. Investor-relations data\n  is published as filings and reports rather than through a paid API.\nsources:\n- https://archresources.com\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n \
  \ dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Arch Resources, Inc.\nserviceCategory: Industrial / Mining\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Arch Coal\n  ServiceCategory: Mining / Coal\n  ProviderName: Arch Coal\n  PublisherName: Arch Resources, Inc.\n  InvoiceIssuerName: Arch Resources, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n- name: Visibility\n  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies\
  \ and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/arch-coal/refs/heads/main/finops/arch-coal-finops.yml
sources:
- https://archresources.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Mining
- Coal
- Metallurgical Coal
- Thermal Coal
- Energy
- Fortune 500
- FinOps
- Cost Management
- FOCUS
---
