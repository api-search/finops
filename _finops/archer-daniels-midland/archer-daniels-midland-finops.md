---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: archer-daniels-midland-commodity-data-api-openapi.yml
  format: yaml
  label: Archer Daniels Midland Commodity Data API
  slug: commodity-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/archer-daniels-midland/refs/heads/main/openapi/archer-daniels-midland-commodity-data-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Archer Daniels Midland. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Archer-Daniels-Midland Company
  ProviderName: Archer Daniels Midland
  PublisherName: Archer-Daniels-Midland Company
  ServiceCategory: Agriculture / Food Processing
  ServiceName: Archer Daniels Midland
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Archer Daniels Midland Finops
provider_name: Archer Daniels Midland
provider_slug: archer-daniels-midland
publisher_name: Archer-Daniels-Midland Company
service_category: Industrial / Agriculture
slug: archer-daniels-midland-finops
source_filename: archer-daniels-midland-finops.yml
source_heading: FinOps Profile
source_url: https://www.adm.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Archer Daniels Midland\nproviderId: archer-daniels-midland\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Agriculture\n- Food Processing\n- Commodities\n- Supply Chain\n- Fortune 100\n- Nutrition\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Archer Daniels Midland. No public billing-model details,\n  meters, or invoice schema are published; this artifact records the absence so consumers know to source\n  commercial terms from the provider directly.\nnotes: ADM does not publish public API pricing. The Commodity Data API is a partner-integration surface;\n  commercial terms are negotiated directly with ADM and are not exposed via a public plans page.\nsources:\n- https://www.adm.com\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n\
  \  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Archer-Daniels-Midland Company\nserviceCategory: Industrial / Agriculture\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Archer Daniels Midland\n  ServiceCategory: Agriculture / Food Processing\n  ProviderName: Archer Daniels Midland\n  PublisherName: Archer-Daniels-Midland Company\n  InvoiceIssuerName: Archer-Daniels-Midland Company\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n\
  - name: Visibility\n  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/archer-daniels-midland/refs/heads/main/finops/archer-daniels-midland-finops.yml
sources:
- https://www.adm.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Agriculture
- Food Processing
- Commodities
- Supply Chain
- Fortune 100
- Nutrition
- FinOps
- Cost Management
- FOCUS
---
