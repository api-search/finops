---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: applied-materials-openapi.yaml
  format: yaml
  label: Applied Materials API
  slug: applied-materials-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/applied-materials/refs/heads/main/openapi/applied-materials-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Applied Materials. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Applied Materials, Inc.
  ProviderName: Applied Materials
  PublisherName: Applied Materials, Inc.
  ServiceCategory: Semiconductor Manufacturing Equipment
  ServiceName: Applied Materials
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Applied Materials Finops
provider_name: Applied Materials
provider_slug: applied-materials
publisher_name: Applied Materials, Inc.
service_category: Industrial / Manufacturing
slug: applied-materials-finops
source_filename: applied-materials-finops.yml
source_heading: FinOps Profile
source_url: https://www.applied-materials.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Applied Materials\nproviderId: applied-materials\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Semiconductor\n- Manufacturing\n- Equipment\n- Fab Operations\n- Materials Engineering\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Applied Materials. No public billing-model details,\n  meters, or invoice schema are published; this artifact records the absence so consumers know to source\n  commercial terms from the provider directly.\nnotes: Applied Materials does not publish a public API pricing page. Equipment integrations are negotiated\n  through enterprise sales and partner programs; commercial terms are governed by individual customer\n  agreements rather than a published plans surface.\nsources:\n- https://www.applied-materials.com\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Applied Materials, Inc.\nserviceCategory: Industrial / Manufacturing\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Applied Materials\n  ServiceCategory: Semiconductor Manufacturing Equipment\n  ProviderName: Applied Materials\n  PublisherName: Applied Materials, Inc.\n  InvoiceIssuerName: Applied Materials, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n\
  \  - contract\n  - consumer\nprinciples:\n- name: Visibility\n  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/applied-materials/refs/heads/main/finops/applied-materials-finops.yml
sources:
- https://www.applied-materials.com
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Semiconductor
- Manufacturing
- Equipment
- Fab Operations
- Materials Engineering
- FinOps
- Cost Management
- FOCUS
---
