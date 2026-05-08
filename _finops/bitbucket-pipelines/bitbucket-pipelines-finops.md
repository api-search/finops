---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bitbucket-pipelines-openapi.json
  format: json
  label: Bitbucket Cloud REST API v2.0 (Pipelines)
  slug: rest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitbucket-pipelines/refs/heads/main/openapi/bitbucket-pipelines-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for Bitbucket Pipelines. Costs come from the Bitbucket Cloud per-user subscription (Standard/Premium), Pipelines build-minute consumption (with per-tier free allotment plus $10/1,000 minute add-on packs), Premium-only advanced security charges, plus the customer's own infrastructure cost for self-hosted runners (free at the Pipelines layer).
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Atlassian
  PricingUnit: user / minute
  ProviderName: Atlassian
  PublisherName: Atlassian
  ServiceCategory: DevOps
  ServiceName: Bitbucket Pipelines
layout: finops
meters:
- aggregation: max
  description: Active Bitbucket Cloud users in the billing month.
  dimensions:
  - workspace
  - tier
  name: bitbucket_users
  unit: user-month
- aggregation: sum
  description: Pipelines hosted-runner build minutes consumed.
  dimensions:
  - workspace
  - repository
  name: pipelines_build_minutes
  unit: minute
- aggregation: sum
  description: 1,000-minute packs purchased above the included allotment.
  dimensions:
  - workspace
  name: additional_minute_packs
  unit: pack-month
- aggregation: sum
  description: Underlying cloud compute hours for self-hosted Pipelines runners.
  dimensions:
  - cloud_account
  - runner_label
  name: self_hosted_runner_vm_hours
  unit: vm-hour
name: Bitbucket Pipelines Finops
provider_name: Bitbucket Pipelines
provider_slug: bitbucket-pipelines
publisher_name: Atlassian
service_category: DevOps / CI/CD
slug: bitbucket-pipelines-finops
source_filename: bitbucket-pipelines-finops.yml
source_heading: FinOps Profile
source_url: https://www.atlassian.com/software/bitbucket/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bitbucket Pipelines\nproviderId: bitbucket-pipelines\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- DevOps\n- CI/CD\n- Pipelines\n- Atlassian\n- Bitbucket\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Bitbucket Pipelines. Costs come from the\n  Bitbucket Cloud per-user subscription (Standard/Premium), Pipelines\n  build-minute consumption (with per-tier free allotment plus $10/1,000\n  minute add-on packs), Premium-only advanced security charges, plus the\n  customer's own infrastructure cost for self-hosted runners (free at the\n  Pipelines layer).\nnotes: >-\n  Atlassian invoices monthly in USD per workspace; the Bitbucket admin\n  Pipelines usage page shows minute consumption per repository, suitable for\n  chargeback. Self-hosted runner labels can also be used as cost-allocation\n  tags.\n\
  sources:\n- https://www.atlassian.com/software/bitbucket/pricing\n- https://support.atlassian.com/bitbucket-cloud/docs/build-minutes/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Atlassian\nserviceCategory: DevOps / CI/CD\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Bitbucket Pipelines\n  ServiceCategory: DevOps\n  ProviderName: Atlassian\n  PublisherName: Atlassian\n  InvoiceIssuerName: Atlassian\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: user / minute\nmeters:\n- name: bitbucket_users\n  description: Active Bitbucket Cloud users in the billing month.\n  unit: user-month\n\
  \  aggregation: max\n  dimensions:\n  - workspace\n  - tier\n- name: pipelines_build_minutes\n  description: Pipelines hosted-runner build minutes consumed.\n  unit: minute\n  aggregation: sum\n  dimensions:\n  - workspace\n  - repository\n- name: additional_minute_packs\n  description: 1,000-minute packs purchased above the included allotment.\n  unit: pack-month\n  aggregation: sum\n  dimensions:\n  - workspace\n- name: self_hosted_runner_vm_hours\n  description: Underlying cloud compute hours for self-hosted Pipelines runners.\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - runner_label\nprinciples:\n- name: Visibility\n  description: Use the Bitbucket admin Pipelines minutes page; reconcile against monthly Atlassian invoice.\n- name: Allocation\n  description: Allocate by repository / workspace; add cost-center tags via runner labels for self-hosted.\n- name: Optimization\n  description: Cache aggressively; use parallel steps wisely; switch heavy workloads\
  \ to free self-hosted runners; right-size 1,000-minute packs vs upgrading tier.\n- name: Accountability\n  description: Assign workspace admin owners; alert on minute-consumption trajectory toward plan ceiling.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bitbucket-pipelines/refs/heads/main/finops/bitbucket-pipelines-finops.yml
sources:
- https://www.atlassian.com/software/bitbucket/pricing
- https://support.atlassian.com/bitbucket-cloud/docs/build-minutes/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Pipelines
- Atlassian
- Bitbucket
- FinOps
- Cost Management
- FOCUS
---
