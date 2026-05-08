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
  pricingCategory: Aggregator-Mediated Per-Call Usage
description: FOCUS-aligned FinOps view of Pika Labs. Pika does not bill API usage directly; integrators pay the chosen aggregator (fal.ai) which invoices Pika model calls separately. FinOps centers on tracking aggregator invoices and tagging Pika-specific calls.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: fal.ai (or chosen aggregator)
  ProviderName: Pika Labs
  PublisherName: fal.ai (or chosen aggregator)
  ServiceCategory: AI
  ServiceName: Pika Video Generation
layout: finops
meters:
- aggregation: sum
  description: Pika model invocations through aggregator (per call, sometimes per second of video).
  dimensions:
  - account
  - aggregator
  - model
  name: video_generations
  unit: video
name: Pika Labs Finops
provider_name: Pika Labs
provider_slug: pika-labs
publisher_name: Aggregator (fal.ai)
service_category: AI
slug: pika-labs-finops
source_filename: pika-labs-finops.yml
source_heading: FinOps Profile
source_url: https://pika.art/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pika Labs\nproviderId: pika-labs\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: partial\ntags:\n- AI\n- Video Generation\n- Text-to-Video\n- Multimodal\n- Generative\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Pika Labs. Pika does not bill API usage directly; integrators\n  pay the chosen aggregator (fal.ai) which invoices Pika model calls separately. FinOps\n  centers on tracking aggregator invoices and tagging Pika-specific calls.\nnotes: Publisher and Invoice Issuer is the aggregator (e.g. fal.ai), not Pika Labs.\nsources:\n- https://pika.art/\n- https://fal.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Aggregator (fal.ai)\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Aggregator-Mediated Per-Call Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Pika Video Generation\n  ServiceCategory: AI\n  ProviderName: Pika Labs\n  PublisherName: fal.ai (or chosen aggregator)\n  InvoiceIssuerName: fal.ai (or chosen aggregator)\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: video_generations\n  description: Pika model invocations through aggregator (per call, sometimes per second of video).\n  unit: video\n  aggregation: sum\n  dimensions:\n  - account\n  - aggregator\n  - model\nprinciples:\n- name: Visibility\n  description: Pull aggregator invoice line items filtered to Pika-tagged calls.\n- name: Allocation\n  description: Tag aggregator API keys per consuming product surface.\n- name: Optimization\n  description: Compare aggregator price sheets if multiple\
  \ host Pika models.\n- name: Accountability\n  description: Assign owner of aggregator account that invoices Pika usage.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pika-labs/refs/heads/main/finops/pika-labs-finops.yml
sources:
- https://pika.art/
- https://fal.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Video Generation
- Text-to-Video
- Multimodal
- Generative
- FinOps
- Cost Management
- FOCUS
---
