---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: To Be Reconciled
description: FOCUS-aligned FinOps placeholder for Weights & Biases. Pipeline will replace with real billing details.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Weights & Biases
  ProviderName: Weights & Biases
  PublisherName: Weights & Biases
  ServiceCategory: ML
  ServiceName: Weights & Biases
layout: finops
meters:
- aggregation: sum
  description: Catch-all meter pending reconciliation.
  dimensions:
  - account
  - resource
  name: api_usage
  unit: varies
name: Weights And Biases Finops
provider_name: Weights & Biases
provider_slug: weights-and-biases
publisher_name: Weights & Biases
service_category: ML
slug: weights-and-biases-finops
source_filename: weights-and-biases-finops.yml
source_heading: FinOps Profile
source_url: https://wandb.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Weights & Biases\nproviderId: weights-and-biases\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- ML\n- MLOps\n- Experiment Tracking\n- Model Registry\n- Inference\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps placeholder for Weights & Biases. Pipeline will replace with real billing details.\nnotes: Initial scaffold — billing model has not yet been reconciled.\nsources:\n- https://wandb.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Weights & Biases\nserviceCategory: ML\nbillingModel:\n  pricingCategory: To Be Reconciled\n  billingFrequency: Monthly\n  billingCurrency:\
  \ USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Weights & Biases\n  ServiceCategory: ML\n  ProviderName: Weights & Biases\n  PublisherName: Weights & Biases\n  InvoiceIssuerName: Weights & Biases\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: api_usage\n  description: Catch-all meter pending reconciliation.\n  unit: varies\n  aggregation: sum\n  dimensions:\n  - account\n  - resource\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/weights-and-biases/refs/heads/main/finops/weights-and-biases-finops.yml
sources:
- https://wandb.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- ML
- MLOps
- Experiment Tracking
- Model Registry
- Inference
- FinOps
- Cost Management
- FOCUS
---
