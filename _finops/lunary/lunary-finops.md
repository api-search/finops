---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Subscription
  - Usage
  pricingCategory: Subscription + Usage / Free Self-Host
description: FOCUS-aligned FinOps profile for Lunary. Cost is driven by tier (seats) plus event volume on the hosted SaaS. Self-hosted under Apache 2.0 trades vendor cost for compute/storage cost on your own infrastructure. Optimize by sampling, batching, and self-hosting at high event scale.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Lunary
  ProviderName: Lunary
  PublisherName: Lunary
  ServiceCategory: AI Observability
  ServiceName: Lunary
layout: finops
meters:
- aggregation: sum
  description: Events (logs, traces) ingested per month.
  dimensions:
  - project
  name: events_ingested
  unit: event
- aggregation: max
  description: Active users.
  dimensions:
  - team
  name: seats
  unit: seat-month
name: Lunary Finops
provider_name: Lunary
provider_slug: lunary
publisher_name: Lunary
service_category: AI Observability
slug: lunary-finops
source_filename: lunary-finops.yml
source_heading: FinOps Profile
source_url: https://lunary.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lunary\nproviderId: lunary\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI Evaluation\n- Observability\n- Open Source\n- LLM\n- Tracing\n- Prompts\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Lunary. Cost is driven by tier (seats) plus event volume on the\n  hosted SaaS. Self-hosted under Apache 2.0 trades vendor cost for compute/storage cost on your own\n  infrastructure. Optimize by sampling, batching, and self-hosting at high event scale.\nnotes: Seat + event-volume hosted, or compute/storage self-hosted.\nsources:\n- https://lunary.ai/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Lunary\nserviceCategory: AI Observability\nbillingModel:\n  pricingCategory: Subscription + Usage / Free Self-Host\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Subscription\n  - Usage\nfocusColumns:\n  ServiceName: Lunary\n  ServiceCategory: AI Observability\n  ProviderName: Lunary\n  PublisherName: Lunary\n  InvoiceIssuerName: Lunary\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n- name: events_ingested\n  description: Events (logs, traces) ingested per month.\n  unit: event\n  aggregation: sum\n  dimensions:\n  - project\n- name: seats\n  description: Active users.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - team\nprinciples:\n- name: Visibility\n  description: Track event volume monthly via the Lunary console.\n- name: Allocation\n  description: Allocate per project/team using project tags.\n- name: Optimization\n  description: Sample production traffic; self-host at high scale.\n- name: Accountability\n\
  \  description: AI/ML team owns the Lunary deployment and cost.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lunary/refs/heads/main/finops/lunary-finops.yml
sources:
- https://lunary.ai/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI Evaluation
- Observability
- Open Source
- LLM
- Tracing
- Prompts
- FinOps
- Cost Management
- FOCUS
---
