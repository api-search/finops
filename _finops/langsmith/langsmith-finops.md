---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Tracing API
  slug: langsmith-tracing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Datasets API
  slug: langsmith-datasets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Evaluations API
  slug: langsmith-evaluations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Prompt Hub API
  slug: langsmith-prompts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Feedback API
  slug: langsmith-feedback-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Annotation Queues API
  slug: langsmith-annotation-queues-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
- filename: langsmith-openapi.json
  format: json
  label: LangSmith Fleet (Agent Deployment) API
  slug: langsmith-fleet-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/openapi/langsmith-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for LangSmith. LangSmith billing combines a per-seat subscription with usage-based charges for base traces, Fleet agent runs, and production deployment uptime minutes.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: LangChain
  ProviderName: LangChain
  PublisherName: LangChain
  ServiceCategory: AI
  ServiceName: LangSmith
layout: finops
meters:
- aggregation: sum
  description: Per-seat monthly subscription on the Plus plan ($39/seat/month).
  dimensions:
  - workspace
  - user
  name: seats
  unit: seat
- aggregation: sum
  description: Billable base traces ingested in a month. Plus includes 10k; overage is $2.50 per 1,000.
  dimensions:
  - workspace
  - project
  name: base_traces
  unit: trace
- aggregation: sum
  description: Fleet agent runs executed in a month. Each plan includes a baseline allowance.
  dimensions:
  - workspace
  - agent
  name: fleet_runs
  unit: run
- aggregation: sum
  description: Minutes of production deployment uptime billed at $0.0036/min on the Plus plan.
  dimensions:
  - workspace
  - deployment
  name: deployment_uptime_minutes
  unit: minute
name: Langsmith Finops
provider_name: LangSmith
provider_slug: langsmith
publisher_name: LangChain
service_category: AI
slug: langsmith-finops
source_filename: langsmith-finops.yml
source_heading: FinOps Profile
source_url: https://www.langchain.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: LangSmith\nproviderId: langsmith\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- AI\n- LLM\n- Observability\n- Evaluations\n- LangChain\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for LangSmith. LangSmith billing combines a per-seat\n  subscription with usage-based charges for base traces, Fleet agent runs, and production\n  deployment uptime minutes.\nsources:\n- https://www.langchain.com/pricing\n- https://docs.langchain.com/langsmith\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: LangChain\nserviceCategory: AI\nbillingModel:\n  pricingCategory: Subscription\
  \ + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: LangSmith\n  ServiceCategory: AI\n  ProviderName: LangChain\n  PublisherName: LangChain\n  InvoiceIssuerName: LangChain\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: seats\n  description: Per-seat monthly subscription on the Plus plan ($39/seat/month).\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - workspace\n  - user\n- name: base_traces\n  description: Billable base traces ingested in a month. Plus includes 10k; overage is\n    $2.50 per 1,000.\n  unit: trace\n  aggregation: sum\n  dimensions:\n  - workspace\n  - project\n- name: fleet_runs\n  description: Fleet agent runs executed in a month. Each plan includes a baseline allowance.\n  unit: run\n  aggregation: sum\n  dimensions:\n  - workspace\n  - agent\n- name: deployment_uptime_minutes\n  description: Minutes of production deployment uptime billed\
  \ at $0.0036/min on the Plus plan.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - workspace\n  - deployment\nprinciples:\n- name: Visibility\n  description: Pull LangChain billing exports and tag traces by project to map spend to teams\n    and applications.\n- name: Allocation\n  description: Use workspace, project, and trace metadata to allocate trace, Fleet-run, and\n    deployment costs to consuming services.\n- name: Optimization\n  description: Sample or filter low-value traces, right-size Fleet agent concurrency, and\n    pause unused production deployments to reduce uptime minutes.\n- name: Accountability\n  description: Assign each LangSmith workspace to a budget owner and review monthly trace\n    and run consumption.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/langsmith/refs/heads/main/finops/langsmith-finops.yml
sources:
- https://www.langchain.com/pricing
- https://docs.langchain.com/langsmith
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- AI
- LLM
- Observability
- Evaluations
- LangChain
- FinOps
- Cost Management
- FOCUS
---
