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
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + AI Spend Pass-Through
description: FOCUS-aligned FinOps view of Botpress Cloud. Billing combines a base plan fee per tier with separate AI Spend (LLM token cost) drawn down from a $5/month credit on Pay-as-you-go and pass-through on paid tiers. Vector storage and seats are tier-gated. Self-hosted Botpress costs only your infra plus LLM bills.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Botpress
  ProviderName: Botpress
  PublisherName: Botpress
  ServiceCategory: AI
  ServiceName: Botpress Cloud
layout: finops
meters:
- aggregation: sum
  description: Monthly plan subscription fee.
  dimensions:
  - account
  - plan
  name: plan_fee
  unit: month
- aggregation: sum
  description: Incoming messages handled per month.
  dimensions:
  - account
  - bot
  name: incoming_messages
  unit: message
- aggregation: sum
  description: LLM token spend (provider pass-through).
  dimensions:
  - account
  - model
  name: ai_spend
  unit: USD
- aggregation: max
  description: Vector DB storage size.
  dimensions:
  - account
  name: vector_storage
  unit: gigabytes
- aggregation: max
  description: Workspace collaborator seats.
  dimensions:
  - account
  - plan
  name: seats
  unit: seat-month
name: Botpress Finops
provider_name: Botpress
provider_slug: botpress
publisher_name: Botpress
service_category: AI
slug: botpress-finops
source_filename: botpress-finops.yml
source_heading: FinOps Profile
source_url: https://botpress.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Botpress\nproviderId: botpress\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- Conversational\n- Chat\n- Open Source\n- Bot Builder\n- LLM\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Botpress Cloud. Billing combines a base plan fee per tier\n  with separate AI Spend (LLM token cost) drawn down from a $5/month credit on\n  Pay-as-you-go and pass-through on paid tiers. Vector storage and seats are tier-gated.\n  Self-hosted Botpress costs only your infra plus LLM bills.\nnotes: AI Spend is the variable cost; rightsize agent flow design and chosen LLM model to control burn.\nsources:\n- https://botpress.com/pricing\n- https://botpress.com/docs\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Botpress\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription + AI Spend Pass-Through\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Botpress Cloud\n  ServiceCategory: AI\n  ProviderName: Botpress\n  PublisherName: Botpress\n  InvoiceIssuerName: Botpress\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: plan_fee\n  description: Monthly plan subscription fee.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - account\n  - plan\n- name: incoming_messages\n  description: Incoming messages handled per month.\n  unit: message\n  aggregation: sum\n  dimensions:\n  - account\n  - bot\n- name: ai_spend\n  description: LLM token spend (provider pass-through).\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - account\n  - model\n\
  - name: vector_storage\n  description: Vector DB storage size.\n  unit: gigabytes\n  aggregation: max\n  dimensions:\n  - account\n- name: seats\n  description: Workspace collaborator seats.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - account\n  - plan\nprinciples:\n- name: Visibility\n  description: Track plan fee, incoming messages, AI Spend, and vector storage in Botpress workspace dashboard.\n- name: Allocation\n  description: Tag bots to consuming line of business / customer.\n- name: Optimization\n  description: Reduce AI Spend by selecting cheaper models for non-critical flows and pre-computing answers via vector DB.\n- name: Accountability\n  description: Assign owners for plan fee and AI Spend separately; PAYG tier offers $5 AI credit/month.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/botpress/refs/heads/main/finops/botpress-finops.yml
sources:
- https://botpress.com/pricing
- https://botpress.com/docs
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Conversational
- Chat
- Open Source
- Bot Builder
- LLM
- FinOps
- Cost Management
- FOCUS
---
