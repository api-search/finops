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
  pricingCategory: Usage-Based (Per Conversation)
description: 'FOCUS-aligned FinOps view of Voiceflow. Voiceflow uses transparent usage-based billing scaled by conversation volume. Two purchase paths exist: agency/partner workspaces with white-labeling, and business/enterprise contracts with implementation support and multi-channel deployment. Per-conversation rate sheet not openly listed.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Voiceflow
  ProviderName: Voiceflow
  PublisherName: Voiceflow
  ServiceCategory: AI
  ServiceName: Voiceflow Conversations API
layout: finops
meters:
- aggregation: sum
  description: Conversation count.
  dimensions:
  - account
  - workspace
  - agent
  name: conversations
  unit: conversation
- aggregation: max
  description: Workspace seats / collaborators.
  dimensions:
  - account
  - workspace
  name: workspace_seats
  unit: seat-month
- aggregation: sum
  description: LLM tokens consumed (provider pass-through).
  dimensions:
  - account
  - model
  name: llm_tokens
  unit: token
name: Voiceflow Finops
provider_name: Voiceflow
provider_slug: voiceflow
publisher_name: Voiceflow
service_category: AI
slug: voiceflow-finops
source_filename: voiceflow-finops.yml
source_heading: FinOps Profile
source_url: https://www.voiceflow.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Voiceflow\nproviderId: voiceflow\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: partial\ntags:\n- AI\n- Conversational\n- Chat\n- Voice\n- Agent Builder\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps view of Voiceflow. Voiceflow uses transparent usage-based billing\n  scaled by conversation volume. Two purchase paths exist: agency/partner workspaces with\n  white-labeling, and business/enterprise contracts with implementation support and\n  multi-channel deployment. Per-conversation rate sheet not openly listed.\nnotes: Verify per-conversation cost in workspace dashboard; LLM tokens are passed through to underlying provider.\nsources:\n- https://www.voiceflow.com/pricing\n- https://docs.voiceflow.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl:\
  \ https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Voiceflow\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Usage-Based (Per Conversation)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Voiceflow Conversations API\n  ServiceCategory: AI\n  ProviderName: Voiceflow\n  PublisherName: Voiceflow\n  InvoiceIssuerName: Voiceflow\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: conversations\n  description: Conversation count.\n  unit: conversation\n  aggregation: sum\n  dimensions:\n  - account\n  - workspace\n  - agent\n- name: workspace_seats\n  description: Workspace seats / collaborators.\n  unit: seat-month\n  aggregation: max\n  dimensions:\n  - account\n  - workspace\n- name: llm_tokens\n  description: LLM tokens consumed (provider pass-through).\n  unit:\
  \ token\n  aggregation: sum\n  dimensions:\n  - account\n  - model\nprinciples:\n- name: Visibility\n  description: Track conversations per agent in Voiceflow workspace dashboard.\n- name: Allocation\n  description: Tag agents to consuming line of business / customer.\n- name: Optimization\n  description: Right-size agency vs business plan based on conversation volume; cap LLM token spend by tuning agent flows.\n- name: Accountability\n  description: Assign workspace owner per agent / customer; centralized billing on Team / Enterprise tiers.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/voiceflow/refs/heads/main/finops/voiceflow-finops.yml
sources:
- https://www.voiceflow.com/pricing
- https://docs.voiceflow.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- Conversational
- Chat
- Voice
- Agent Builder
- FinOps
- Cost Management
- FOCUS
---
