---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: N/A or Monthly (Snowflake)
  chargeCategories:
  - Usage
  pricingCategory: Free OSS / Snowflake Credits
description: FOCUS-aligned FinOps profile for TruEra/TruLens. TruLens itself is free; cost flows to the underlying LLM/embedding provider used as the judge model. Commercial successor on Snowflake is billed in Snowflake credits and appears on the Snowflake invoice — manage there using standard Snowflake FinOps practices.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Snowflake
  ProviderName: Snowflake
  PublisherName: Snowflake (TruEra)
  ServiceCategory: AI Evaluation
  ServiceName: TruEra / TruLens
layout: finops
meters:
- aggregation: sum
  description: Tokens consumed by the LLM judge model during TruLens eval.
  dimensions:
  - provider
  - model
  name: judge_model_tokens
  unit: token
- aggregation: sum
  description: Snowflake credits consumed by hosted observability features.
  dimensions:
  - warehouse
  name: snowflake_credits
  unit: credit
name: Truera Finops
provider_name: TruEra (Snowflake)
provider_slug: truera
publisher_name: Snowflake (TruEra)
service_category: AI Observability
slug: truera-finops
source_filename: truera-finops.yml
source_heading: FinOps Profile
source_url: https://www.trulens.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TruEra (Snowflake)\nproviderId: truera\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI Evaluation\n- Observability\n- AI Governance\n- LLM\n- RAG\n- Snowflake\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for TruEra/TruLens. TruLens itself is free; cost flows to the\n  underlying LLM/embedding provider used as the judge model. Commercial successor on Snowflake is\n  billed in Snowflake credits and appears on the Snowflake invoice — manage there using standard\n  Snowflake FinOps practices.\nnotes: TruLens free; commercial cost is in Snowflake credits post-acquisition.\nsources:\n- https://www.trulens.org/\n- https://www.snowflake.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Snowflake (TruEra)\nserviceCategory: AI Observability\nbillingModel:\n  pricingCategory: Free OSS / Snowflake Credits\n  billingFrequency: N/A or Monthly (Snowflake)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\nfocusColumns:\n  ServiceName: TruEra / TruLens\n  ServiceCategory: AI Evaluation\n  ProviderName: Snowflake\n  PublisherName: Snowflake (TruEra)\n  InvoiceIssuerName: Snowflake\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: judge_model_tokens\n  description: Tokens consumed by the LLM judge model during TruLens eval.\n  unit: token\n  aggregation: sum\n  dimensions:\n  - provider\n  - model\n- name: snowflake_credits\n  description: Snowflake credits consumed by hosted observability features.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - warehouse\nprinciples:\n- name: Visibility\n  description: Track upstream LLM\
  \ usage and Snowflake credit burn.\n- name: Allocation\n  description: Allocate to the AI feature/team being evaluated.\n- name: Optimization\n  description: Choose cheaper judge models; size Snowflake warehouses appropriately.\n- name: Accountability\n  description: AI/ML team owns eval cost; data platform team owns Snowflake account.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/truera/refs/heads/main/finops/truera-finops.yml
sources:
- https://www.trulens.org/
- https://www.snowflake.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI Evaluation
- Observability
- AI Governance
- LLM
- RAG
- Snowflake
- FinOps
- Cost Management
- FOCUS
---
