---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: increase-openapi.json
  format: json
  label: Increase ACH API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/openapi/increase-openapi.json
- filename: increase-openapi.json
  format: json
  label: Increase Wire Transfers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/openapi/increase-openapi.json
- filename: increase-openapi.json
  format: json
  label: Increase Real-Time Payments API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/openapi/increase-openapi.json
- filename: increase-openapi.json
  format: json
  label: Increase Check API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/openapi/increase-openapi.json
- filename: increase-openapi.json
  format: json
  label: Increase Cards API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/openapi/increase-openapi.json
- filename: increase-openapi.json
  format: json
  label: Increase Accounts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/openapi/increase-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Increase. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Increase
  ProviderName: Increase
  PublisherName: Increase
  ServiceCategory: Fintech
  ServiceName: Increase
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Increase Finops
provider_name: Increase
provider_slug: increase
publisher_name: Increase
service_category: Fintech
slug: increase-finops
source_filename: increase-finops.yml
source_heading: FinOps Profile
source_url: https://increase.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Increase\nproviderId: increase\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Fintech\n- Banking\n- Payments\n- ACH\n- Wires\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Increase. Pipeline will replace with real billing details.\nnotes: \"Initial scaffold \\u2014 billing model has not yet been reconciled.\"\nsources:\n- https://increase.com/\n- https://increase.com/documentation\n- https://increase.com/documentation/api\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Increase\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory: To Be Reconciled\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Increase\n  ServiceCategory: Fintech\n  ProviderName: Increase\n  PublisherName: Increase\n  InvoiceIssuerName: Increase\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/increase/refs/heads/main/finops/increase-finops.yml
sources:
- https://increase.com/
- https://increase.com/documentation
- https://increase.com/documentation/api
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Banking
- Payments
- ACH
- Wires
- FinOps
- Cost Management
- FOCUS
---
