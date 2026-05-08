---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: drift-openapi.yml
  format: yaml
  label: Drift REST API
  slug: drift-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/drift/refs/heads/main/openapi/drift-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Drift. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Drift
  ProviderName: Drift
  PublisherName: Drift
  ServiceCategory: Customer Support
  ServiceName: Drift
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Drift Finops
provider_name: Drift
provider_slug: drift
publisher_name: Drift
service_category: Customer Support
slug: drift-finops
source_filename: drift-finops.yml
source_heading: FinOps Profile
source_url: https://www.drift.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Drift\nproviderId: drift\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- Customer Support\n- Sales\n- Conversational\n- Chatbot\n- AI\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Drift. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.drift.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Drift\nserviceCategory: Customer Support\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  -\
  \ Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Drift\n  ServiceCategory: Customer Support\n  ProviderName: Drift\n  PublisherName: Drift\n  InvoiceIssuerName: Drift\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/drift/refs/heads/main/finops/drift-finops.yml
sources:
- https://www.drift.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Customer Support
- Sales
- Conversational
- Chatbot
- AI
- FinOps
- Cost Management
- FOCUS
---
