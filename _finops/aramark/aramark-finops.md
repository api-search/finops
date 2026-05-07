---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: marko-api.yml
  format: yaml
  label: Aramark Marko API
  slug: marko-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aramark/refs/heads/main/openapi/marko-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Aramark. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aramark Services, Inc.
  ProviderName: Aramark
  PublisherName: Aramark Services, Inc.
  ServiceCategory: Food, Facilities, and Uniform Services
  ServiceName: Aramark
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Aramark Finops
provider_name: Aramark
provider_slug: aramark
publisher_name: Aramark Services, Inc.
service_category: Enterprise Services
slug: aramark-finops
source_filename: aramark-finops.yml
source_heading: FinOps Profile
source_url: https://www.aramark.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Aramark\nproviderId: aramark\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Food Services\n- Facilities Management\n- Uniform Services\n- Data Platform\n- Fortune 500\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Aramark. No public billing-model details, meters, or\n  invoice schema are published; this artifact records the absence so consumers know to source commercial\n  terms from the provider directly.\nnotes: Aramark's Marko developer portal exposes a 70+ service catalog but does not publish pricing, plan\n  tiers, or commercial terms. Access appears to be partner/internal — pricing, if any, is negotiated rather\n  than self-serve.\nsources:\n- https://www.aramark.com\n- https://focus.finops.org/focus-specification/v1-3/\n- https://marko-developers.aramark.net/\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Aramark Services, Inc.\nserviceCategory: Enterprise Services\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Aramark\n  ServiceCategory: Food, Facilities, and Uniform Services\n  ProviderName: Aramark\n  PublisherName: Aramark Services, Inc.\n  InvoiceIssuerName: Aramark Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n- name: Visibility\n\
  \  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aramark/refs/heads/main/finops/aramark-finops.yml
sources:
- https://www.aramark.com
- https://focus.finops.org/focus-specification/v1-3/
- https://marko-developers.aramark.net/
specification: FinOps Framework
tags:
- Food Services
- Facilities Management
- Uniform Services
- Data Platform
- Fortune 500
- FinOps
- Cost Management
- FOCUS
---
