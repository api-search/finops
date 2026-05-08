---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openpipe-openapi.json
  format: json
  label: OpenPipe Platform API
  slug: platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/openpipe/refs/heads/main/openapi/openpipe-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for OpenPipe. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: OpenPipe
  ProviderName: OpenPipe
  PublisherName: OpenPipe
  ServiceCategory: AI
  ServiceName: OpenPipe
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Openpipe Finops
provider_name: OpenPipe
provider_slug: openpipe
publisher_name: OpenPipe
service_category: AI
slug: openpipe-finops
source_filename: openpipe-finops.yml
source_heading: FinOps Profile
source_url: https://openpipe.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: OpenPipe\nproviderId: openpipe\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- AI\n- LLM\n- Fine-Tuning\n- Distillation\n- Inference\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for OpenPipe. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://openpipe.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: OpenPipe\nserviceCategory: AI\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  -\
  \ Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: OpenPipe\n  ServiceCategory: AI\n  ProviderName: OpenPipe\n  PublisherName: OpenPipe\n  InvoiceIssuerName: OpenPipe\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/openpipe/refs/heads/main/finops/openpipe-finops.yml
sources:
- https://openpipe.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Fine-Tuning
- Distillation
- Inference
- FinOps
- Cost Management
- FOCUS
---
