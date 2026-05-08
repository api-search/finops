---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: modern-treasury-openapi.yml
  format: yaml
  label: Modern Treasury Payments API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/modern-treasury/refs/heads/main/openapi/modern-treasury-openapi.yml
- filename: modern-treasury-openapi.yml
  format: yaml
  label: Modern Treasury Ledgers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/modern-treasury/refs/heads/main/openapi/modern-treasury-openapi.yml
- filename: modern-treasury-openapi.yml
  format: yaml
  label: Modern Treasury Counterparties API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/modern-treasury/refs/heads/main/openapi/modern-treasury-openapi.yml
- filename: modern-treasury-openapi.yml
  format: yaml
  label: Modern Treasury Connections & Webhooks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/modern-treasury/refs/heads/main/openapi/modern-treasury-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Modern Treasury. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Modern Treasury
  ProviderName: Modern Treasury
  PublisherName: Modern Treasury
  ServiceCategory: Fintech
  ServiceName: Modern Treasury
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Modern Treasury Finops
provider_name: Modern Treasury
provider_slug: modern-treasury
publisher_name: Modern Treasury
service_category: Fintech
slug: modern-treasury-finops
source_filename: modern-treasury-finops.yml
source_heading: FinOps Profile
source_url: https://www.moderntreasury.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Modern Treasury\nproviderId: modern-treasury\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Fintech\n- Payments\n- ACH\n- Wires\n- Treasury\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Modern Treasury. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://www.moderntreasury.com/\n- https://docs.moderntreasury.com/\n- https://docs.moderntreasury.com/reference\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Modern Treasury\nserviceCategory: Fintech\nbillingModel:\n\
  \  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Modern Treasury\n  ServiceCategory: Fintech\n  ProviderName: Modern Treasury\n  PublisherName: Modern Treasury\n  InvoiceIssuerName: Modern Treasury\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated\
  \ terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/modern-treasury/refs/heads/main/finops/modern-treasury-finops.yml
sources:
- https://www.moderntreasury.com/
- https://docs.moderntreasury.com/
- https://docs.moderntreasury.com/reference
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Payments
- ACH
- Wires
- Treasury
- FinOps
- Cost Management
- FOCUS
---
