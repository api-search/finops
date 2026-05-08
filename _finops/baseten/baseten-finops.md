---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: baseten-llm-openapi.json
  format: json
  label: Baseten LLM Inference API
  slug: llm-inference
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/baseten/refs/heads/main/openapi/baseten-llm-openapi.json
- filename: baseten-messages-openapi.json
  format: json
  label: Baseten Anthropic-Compatible Messages API
  slug: messages
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/baseten/refs/heads/main/openapi/baseten-messages-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Baseten. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Baseten
  ProviderName: Baseten
  PublisherName: Baseten
  ServiceCategory: AI
  ServiceName: Baseten
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Baseten Finops
provider_name: Baseten
provider_slug: baseten
publisher_name: Baseten
service_category: AI
slug: baseten-finops
source_filename: baseten-finops.yml
source_heading: FinOps Profile
source_url: https://www.baseten.co/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Baseten\nproviderId: baseten\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- AI\n- ML\n- Inference\n- Deployment\n- MLOps\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Baseten. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://www.baseten.co/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Baseten\nserviceCategory: AI\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n\
  \  - Adjustment\nfocusColumns:\n  ServiceName: Baseten\n  ServiceCategory: AI\n  ProviderName: Baseten\n  PublisherName: Baseten\n  InvoiceIssuerName: Baseten\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/baseten/refs/heads/main/finops/baseten-finops.yml
sources:
- https://www.baseten.co/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- ML
- Inference
- Deployment
- MLOps
- FinOps
- Cost Management
- FOCUS
---
