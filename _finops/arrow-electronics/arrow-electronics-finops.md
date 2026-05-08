---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: arrow-electronics-openapi.yml
  format: yaml
  label: Arrow Electronics Pricing and Availability API
  slug: pricing-availability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/arrow-electronics/refs/heads/main/openapi/arrow-electronics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Custom / Contract
description: FOCUS-aligned FinOps placeholder for Arrow Electronics. No public billing-model details, meters, or invoice schema are published; this artifact records the absence so consumers know to source commercial terms from the provider directly.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Arrow Electronics, Inc.
  ProviderName: Arrow Electronics
  PublisherName: Arrow Electronics, Inc.
  ServiceCategory: Electronic Components Distribution
  ServiceName: Arrow Electronics
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter for contract-governed consumption. Replace with provider-specific line items once an invoice or usage schema is available.
  dimensions:
  - contract
  - consumer
  name: contract_usage
  unit: varies
name: Arrow Electronics Finops
provider_name: Arrow Electronics
provider_slug: arrow-electronics
publisher_name: Arrow Electronics, Inc.
service_category: Distribution / B2B Commerce
slug: arrow-electronics-finops
source_filename: arrow-electronics-finops.yml
source_heading: FinOps Profile
source_url: https://www.arrow.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Arrow Electronics\nproviderId: arrow-electronics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n- Electronics\n- Components\n- Supply Chain\n- Procurement\n- Distribution\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Arrow Electronics. No public billing-model details,\n  meters, or invoice schema are published; this artifact records the absence so consumers know to source\n  commercial terms from the provider directly.\nnotes: Arrow Electronics offers Pricing & Availability and Order APIs to approved customers. The developer\n  portal documents authentication (login + apikey via URI parameters, separate keys per API) but does\n  not publish plan tiers, per-call pricing, or quota numbers — API keys are issued via a Request API Key\n  flow rather than a self-serve plans page.\nsources:\n- https://www.arrow.com\n\
  - https://focus.finops.org/focus-specification/v1-3/\n- https://developers.arrow.com/api/index.php/site/page?view=Itemservice\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Arrow Electronics, Inc.\nserviceCategory: Distribution / B2B Commerce\nbillingModel:\n  pricingCategory: Custom / Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Arrow Electronics\n  ServiceCategory: Electronic Components Distribution\n  ProviderName: Arrow Electronics\n  PublisherName: Arrow Electronics, Inc.\n  InvoiceIssuerName: Arrow Electronics, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: contract_usage\n  description: Catch-all meter for contract-governed consumption. Replace with provider-specific\
  \ line\n    items once an invoice or usage schema is available.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - contract\n  - consumer\nprinciples:\n- name: Visibility\n  description: Because the provider does not publish a usage API or self-serve billing dashboard, request\n    invoice copies and contract usage exports directly from the account team and load them into your own\n    FinOps tooling.\n- name: Allocation\n  description: Allocate spend by tagging invoice line items to consuming business units in your ERP /\n    FinOps store; no provider-side tagging surface is available.\n- name: Optimization\n  description: Optimization levers are commercial — renegotiate volume commitments, consolidate accounts,\n    or align contract scope with actual usage at renewal.\n- name: Accountability\n  description: Assign a contract owner who reviews invoices against the negotiated agreement, since usage\n    drift cannot be detected from a published meter feed.\nmaintainers:\n- FN: Kin\
  \ Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/arrow-electronics/refs/heads/main/finops/arrow-electronics-finops.yml
sources:
- https://www.arrow.com
- https://focus.finops.org/focus-specification/v1-3/
- https://developers.arrow.com/api/index.php/site/page?view=Itemservice
specification: FinOps Framework
tags:
- Electronics
- Components
- Supply Chain
- Procurement
- Distribution
- FinOps
- Cost Management
- FOCUS
---
