---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: One-Time
  chargeCategories:
  - Adjustment
  pricingCategory: Other
description: FinOps view of Adept "spend." Adept does not invoice customers - it has no commercial API. The only direct cost surface is downloading the open- source Fuyu-8B and Persimmon-8B models from Hugging Face (free) and the customer's own self-hosted GPU inference cost (or third-party inference provider cost). Those costs appear under the inference provider's ServiceName, not Adept's.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: Not Applicable
  PricingCategory: Other
  ProviderName: Adept
  PublisherName: Adept
  ServiceCategory: AI and Machine Learning
  ServiceName: Adept Open-Source Models
layout: finops
meters:
- aggregation: sum
  description: Adept open-source model downloads (free) used for cost-free attribution / inventory tracking only.
  dimensions:
  - team
  - model
  name: model_downloads
  unit: downloads
- aggregation: sum
  description: Customer's own GPU inference cost when serving Adept open-source models (recorded under the inference provider, not Adept).
  dimensions:
  - team
  - model
  - inference_provider
  name: self_hosted_inference_cost
  unit: usd
name: Adept Finops
provider_name: Adept
provider_slug: adept
publisher_name: Adept
service_category: AI and Machine Learning
slug: adept-finops
source_filename: adept-finops.yml
source_heading: FinOps Profile
source_url: https://www.adept.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Adept\nproviderId: adept\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Agents\n- Foundation Models\n- Action Models\n- Open Source\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of Adept \"spend.\" Adept does not invoice customers - it has\n  no commercial API. The only direct cost surface is downloading the open-\n  source Fuyu-8B and Persimmon-8B models from Hugging Face (free) and the\n  customer's own self-hosted GPU inference cost (or third-party inference\n  provider cost). Those costs appear under the inference provider's\n  ServiceName, not Adept's.\nnotes: >-\n  In a corporate FOCUS dataset there is typically no Adept-issued invoice\n  line item. Track the Adept models via tagging on the inference provider's\n  spend (e.g., AWS / Together / Fireworks running Fuyu-8B).\nsources:\n- https://www.adept.ai/\n\
  - https://huggingface.co/adept\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Adept\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Other\n  billingFrequency: One-Time\n  billingCurrency: USD\n  chargeCategories:\n  - Adjustment\nfocusColumns:\n  ServiceName: Adept Open-Source Models\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Adept\n  PublisherName: Adept\n  InvoiceIssuerName: Not Applicable\n  BillingCurrency: USD\n  ChargeCategory: Adjustment\n  PricingCategory: Other\nmeters:\n- name: model_downloads\n  description: Adept open-source model downloads (free) used for cost-free attribution / inventory tracking only.\n  unit: downloads\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n- name: self_hosted_inference_cost\n\
  \  description: Customer's own GPU inference cost when serving Adept open-source models (recorded under the inference provider, not Adept).\n  unit: usd\n  aggregation: sum\n  dimensions:\n  - team\n  - model\n  - inference_provider\nprinciples:\n- name: Visibility\n  description: Inventory which teams downloaded Adept models; correlate with self-hosted GPU spend tagged to those models.\n- name: Allocation\n  description: Tag GPU inference workloads with the model name (Fuyu-8B / Persimmon-8B) for chargeback.\n- name: Optimization\n  description: Quantize or distill Adept open-source models if hosting cost exceeds value; consider replacing with newer open-source action models.\n- name: Accountability\n  description: No Adept invoice to reconcile; owners are the teams running self-hosted inference.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/adept/refs/heads/main/finops/adept-finops.yml
sources:
- https://www.adept.ai/
- https://huggingface.co/adept
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Agents
- Foundation Models
- Action Models
- Open Source
- FinOps
- Cost Management
- FOCUS
---
