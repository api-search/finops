---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gitlab-ci-openapi.yml
  format: yaml
  label: GitLab REST API v4 (CI/CD endpoints)
  slug: rest-v4
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab-ci/refs/heads/main/openapi/gitlab-ci-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly / Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for GitLab CI/CD. Costs come from per-seat subscription (Free/Premium/Ultimate), CI compute minute consumption (with per-tier free allotment and $10/1,000-minute top-ups), storage, transfer, GitLab Credits for Duo Agent Platform, and self-managed runner infra costs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: GitLab
  PricingUnit: seat / minute / GiB
  ProviderName: GitLab
  PublisherName: GitLab
  ServiceCategory: DevOps
  ServiceName: GitLab CI/CD
layout: finops
meters:
- aggregation: max
  description: Active billable users per tier.
  dimensions:
  - tier
  - namespace
  name: seats
  unit: user-month
- aggregation: sum
  description: CI compute minutes consumed against the included monthly allotment.
  dimensions:
  - project
  - runner_type
  name: ci_compute_minutes
  unit: minute
- aggregation: sum
  description: One-time top-up of additional compute minutes (consumable balance).
  dimensions:
  - namespace
  name: ci_compute_topup
  unit: minute
- aggregation: avg
  description: Repository, registry, package and artifact storage in GiB.
  dimensions:
  - namespace
  name: storage_gib
  unit: GiB-month
- aggregation: sum
  description: Egress transfer for Pages, registry, etc.
  dimensions:
  - namespace
  name: transfer
  unit: GiB
- aggregation: sum
  description: Bundled credits for Duo Agent Platform usage.
  dimensions:
  - namespace
  name: gitlab_credits
  unit: USD
- aggregation: sum
  description: Underlying cloud VM hours for self-hosted runners (cloud-billed, not GitLab-billed).
  dimensions:
  - cloud_account
  - runner_label
  name: self_managed_runner_vm_hours
  unit: vm-hour
name: Gitlab Ci Finops
provider_name: GitLab CI/CD
provider_slug: gitlab-ci
publisher_name: GitLab
service_category: DevOps / CI/CD
slug: gitlab-ci-finops
source_filename: gitlab-ci-finops.yml
source_heading: FinOps Profile
source_url: https://about.gitlab.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: GitLab\nproviderId: gitlab-ci\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- DevOps\n- CI/CD\n- Pipelines\n- GitLab\n- DevSecOps\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for GitLab CI/CD. Costs come from per-seat\n  subscription (Free/Premium/Ultimate), CI compute minute consumption (with\n  per-tier free allotment and $10/1,000-minute top-ups), storage, transfer,\n  GitLab Credits for Duo Agent Platform, and self-managed runner infra costs.\nnotes: >-\n  GitLab dashboards expose CI minute usage per project/group; storage and\n  transfer are visible at namespace level. Self-managed runners typically\n  carry the bulk of compute spend on cloud-billed underlying VMs.\nsources:\n- https://about.gitlab.com/pricing/\n- https://docs.gitlab.com/ci/pipelines/cicd_minutes/\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: GitLab\nserviceCategory: DevOps / CI/CD\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: GitLab CI/CD\n  ServiceCategory: DevOps\n  ProviderName: GitLab\n  PublisherName: GitLab\n  InvoiceIssuerName: GitLab\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: seat / minute / GiB\nmeters:\n- name: seats\n  description: Active billable users per tier.\n  unit: user-month\n  aggregation: max\n  dimensions:\n  - tier\n  - namespace\n- name: ci_compute_minutes\n  description: CI compute minutes consumed against the included monthly allotment.\n  unit: minute\n  aggregation: sum\n  dimensions:\n\
  \  - project\n  - runner_type\n- name: ci_compute_topup\n  description: One-time top-up of additional compute minutes (consumable balance).\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - namespace\n- name: storage_gib\n  description: Repository, registry, package and artifact storage in GiB.\n  unit: GiB-month\n  aggregation: avg\n  dimensions:\n  - namespace\n- name: transfer\n  description: Egress transfer for Pages, registry, etc.\n  unit: GiB\n  aggregation: sum\n  dimensions:\n  - namespace\n- name: gitlab_credits\n  description: Bundled credits for Duo Agent Platform usage.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - namespace\n- name: self_managed_runner_vm_hours\n  description: Underlying cloud VM hours for self-hosted runners (cloud-billed, not GitLab-billed).\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - runner_label\nprinciples:\n- name: Visibility\n  description: Use the GitLab Usage Quotas page (CI minutes, storage) and namespace-level\
  \ usage exports.\n- name: Allocation\n  description: Allocate by namespace/group/project; map to FOCUS BillingAccountId / ResourceTag.\n- name: Optimization\n  description: Use cache, parent-child pipelines, fail-fast, larger runners on critical paths; switch high-volume jobs to self-hosted runners; right-size CI minute purchases.\n- name: Accountability\n  description: Assign group owners; alert when CI minutes consumption exceeds plan threshold.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab-ci/refs/heads/main/finops/gitlab-ci-finops.yml
sources:
- https://about.gitlab.com/pricing/
- https://docs.gitlab.com/ci/pipelines/cicd_minutes/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Pipelines
- GitLab
- DevSecOps
- FinOps
- Cost Management
- FOCUS
---
