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
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for Buildkite. Costs derive from per-active-user subscription, self-hosted agent fees above the included allowance, hosted vCPU minutes (Linux/Mac), Test Engine test executions, plus the customer's own cloud spend on self-hosted agent infrastructure.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Buildkite
  PricingUnit: active-user / agent / vCPU-minute
  ProviderName: Buildkite
  PublisherName: Buildkite
  ServiceCategory: DevOps
  ServiceName: Buildkite
layout: finops
meters:
- aggregation: max
  description: Active billable users in the billing month.
  dimensions:
  - organization
  name: active_users
  unit: user-month
- aggregation: max
  description: Self-hosted agent count above the Pro-included 10.
  dimensions:
  - organization
  - cluster
  name: self_hosted_agents
  unit: agent-month
- aggregation: sum
  description: Hosted Linux/Mac vCPU minutes consumed.
  dimensions:
  - organization
  - pipeline
  - os
  name: hosted_vcpu_minutes
  unit: vCPU-minute
- aggregation: sum
  description: Test Engine managed test executions.
  dimensions:
  - organization
  - suite
  name: test_executions
  unit: execution
- aggregation: sum
  description: Underlying cloud compute hours for self-hosted agents (cloud-billed).
  dimensions:
  - cloud_account
  - cluster
  name: self_hosted_runner_infra
  unit: vm-hour
name: Buildkite Finops
provider_name: Buildkite
provider_slug: buildkite
publisher_name: Buildkite
service_category: DevOps / CI/CD
slug: buildkite-finops
source_filename: buildkite-finops.yml
source_heading: FinOps Profile
source_url: https://buildkite.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Buildkite\nproviderId: buildkite\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- DevOps\n- CI/CD\n- Pipelines\n- Agents\n- Self-Hosted\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Buildkite. Costs derive from per-active-user\n  subscription, self-hosted agent fees above the included allowance, hosted\n  vCPU minutes (Linux/Mac), Test Engine test executions, plus the customer's\n  own cloud spend on self-hosted agent infrastructure.\nnotes: >-\n  Self-hosted agents shift the bulk of compute cost onto the customer's cloud\n  (AWS/GCP/Azure); Buildkite retains a small per-agent platform fee plus\n  hosted-minute overage. Test Engine adds independent test-execution metering.\nsources:\n- https://buildkite.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework:\
  \ FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Buildkite\nserviceCategory: DevOps / CI/CD\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Buildkite\n  ServiceCategory: DevOps\n  ProviderName: Buildkite\n  PublisherName: Buildkite\n  InvoiceIssuerName: Buildkite\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: active-user / agent / vCPU-minute\nmeters:\n- name: active_users\n  description: Active billable users in the billing month.\n  unit: user-month\n  aggregation: max\n  dimensions:\n  - organization\n- name: self_hosted_agents\n  description: Self-hosted agent count above the Pro-included 10.\n  unit: agent-month\n  aggregation: max\n  dimensions:\n  - organization\n\
  \  - cluster\n- name: hosted_vcpu_minutes\n  description: Hosted Linux/Mac vCPU minutes consumed.\n  unit: vCPU-minute\n  aggregation: sum\n  dimensions:\n  - organization\n  - pipeline\n  - os\n- name: test_executions\n  description: Test Engine managed test executions.\n  unit: execution\n  aggregation: sum\n  dimensions:\n  - organization\n  - suite\n- name: self_hosted_runner_infra\n  description: Underlying cloud compute hours for self-hosted agents (cloud-billed).\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - cluster\nprinciples:\n- name: Visibility\n  description: Use the Buildkite organization Usage page; export Test Engine usage; combine with cloud cost-export for self-hosted agents.\n- name: Allocation\n  description: Tag pipelines/clusters by team; map to FOCUS ResourceTag.\n- name: Optimization\n  description: Right-size hosted vs self-hosted balance; cache aggressively; prune flaky/slow tests; use cluster-level concurrency.\n- name: Accountability\n\
  \  description: Assign cluster owners; alert on user/agent count drift from plan.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/buildkite/refs/heads/main/finops/buildkite-finops.yml
sources:
- https://buildkite.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Pipelines
- Agents
- Self-Hosted
- FinOps
- Cost Management
- FOCUS
---
