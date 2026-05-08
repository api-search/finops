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
  pricingCategory: Aggregator-Mediated Per-Generation Usage
description: FOCUS-aligned FinOps view of Suno. Suno does not bill API usage directly. Costs flow through whichever third-party aggregator the integrator selects (publisher and invoice issuer = aggregator). Consumer Suno subscription costs are non-API.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aggregator
  ProviderName: Suno
  PublisherName: Aggregator (e.g. sunoapi.org, AIMLAPI)
  ServiceCategory: AI
  ServiceName: Suno Music Generation
layout: finops
meters:
- aggregation: sum
  description: Suno song generations through aggregator.
  dimensions:
  - account
  - aggregator
  name: song_generations
  unit: song
name: Suno Finops
provider_name: Suno
provider_slug: suno
publisher_name: Aggregator (varies)
service_category: AI
slug: suno-finops
source_filename: suno-finops.yml
source_heading: FinOps Profile
source_url: https://suno.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Suno\nproviderId: suno\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: partial\ntags:\n- AI\n- Music Generation\n- Audio\n- Generative\n- TTS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Suno. Suno does not bill API usage directly. Costs flow\n  through whichever third-party aggregator the integrator selects (publisher and invoice\n  issuer = aggregator). Consumer Suno subscription costs are non-API.\nnotes: Treat aggregator as the publisher in FOCUS columns; consumer Pro/Premier credits cannot be allocated to API workloads.\nsources:\n- https://suno.com/\n- https://docs.sunoapi.org/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Aggregator (varies)\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Aggregator-Mediated Per-Generation Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Suno Music Generation\n  ServiceCategory: AI\n  ProviderName: Suno\n  PublisherName: Aggregator (e.g. sunoapi.org, AIMLAPI)\n  InvoiceIssuerName: Aggregator\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: song_generations\n  description: Suno song generations through aggregator.\n  unit: song\n  aggregation: sum\n  dimensions:\n  - account\n  - aggregator\nprinciples:\n- name: Visibility\n  description: Pull invoice from aggregator; correlate to song generation jobs.\n- name: Allocation\n  description: Tag aggregator API keys per consuming product.\n- name: Optimization\n  description: Aggregator selection is the largest cost lever; re-evaluate periodically.\n- name: Accountability\n  description:\
  \ Assign owner to manage aggregator account and contractual / TOS risk.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/suno/refs/heads/main/finops/suno-finops.yml
sources:
- https://suno.com/
- https://docs.sunoapi.org/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Music Generation
- Audio
- Generative
- TTS
- FinOps
- Cost Management
- FOCUS
---
