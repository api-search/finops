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
  - Adjustment
  pricingCategory: Subscription-Based
description: FinOps view of Character.AI spend. Character.AI is a consumer subscription product - the only chargeable surface is the c.ai+ monthly subscription per user. There is no public developer API and no token / call metering. In a corporate FinOps view, c.ai+ should be treated as an end-user SaaS subscription tracked in the SaaS-management category.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Character.AI / Apple App Store / Google Play
  PricingCategory: Subscription-Based
  ProviderName: Character.AI
  PublisherName: Character.AI
  ServiceCategory: AI and Machine Learning
  ServiceName: Character.AI Consumer App
layout: finops
meters:
- aggregation: sum
  description: c.ai+ monthly subscription per user (consumer SaaS).
  dimensions:
  - user
  name: c_ai_plus_subscription
  unit: subscription_months
name: Character Ai Finops
provider_name: Character.AI
provider_slug: character-ai
publisher_name: Character.AI
service_category: AI and Machine Learning
slug: character-ai-finops
source_filename: character-ai-finops.yml
source_heading: FinOps Profile
source_url: https://character.ai/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Character.AI\nproviderId: character-ai\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Chatbots\n- Personas\n- Consumer\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FinOps view of Character.AI spend. Character.AI is a consumer subscription\n  product - the only chargeable surface is the c.ai+ monthly subscription\n  per user. There is no public developer API and no token / call metering.\n  In a corporate FinOps view, c.ai+ should be treated as an end-user SaaS\n  subscription tracked in the SaaS-management category.\nnotes: >-\n  No public developer API; charges appear as recurring per-seat consumer\n  subscription line items charged to the user's payment method (or app\n  store).\nsources:\n- https://character.ai/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation\
  \ Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Character.AI\nserviceCategory: AI and Machine Learning\nbillingModel:\n  pricingCategory: Subscription-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Character.AI Consumer App\n  ServiceCategory: AI and Machine Learning\n  ProviderName: Character.AI\n  PublisherName: Character.AI\n  InvoiceIssuerName: Character.AI / Apple App Store / Google Play\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription-Based\nmeters:\n- name: c_ai_plus_subscription\n  description: c.ai+ monthly subscription per user (consumer SaaS).\n  unit: subscription_months\n  aggregation: sum\n  dimensions:\n  - user\nprinciples:\n- name: Visibility\n  description: Track c.ai+ subscriptions through expense /\
  \ SaaS-management tooling.\n- name: Allocation\n  description: Allocate to individual employee or department if expensed.\n- name: Optimization\n  description: Cancel inactive c.ai+ subscriptions; consumer product not intended for production workloads.\n- name: Accountability\n  description: Owners are individual subscribers; no enterprise contract surface today.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/character-ai/refs/heads/main/finops/character-ai-finops.yml
sources:
- https://character.ai/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Chatbots
- Personas
- Consumer
- FinOps
- Cost Management
- FOCUS
---
