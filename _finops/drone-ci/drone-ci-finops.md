---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous (cloud-billed)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Self-Hosted (no SaaS billing)
description: FOCUS-aligned FinOps profile for Drone. As an open-source self-hosted CI, Drone has no SaaS invoice; the cost surface is the underlying cloud spend for the Drone server and runner pool. Customers needing commercial support pay Harness via Harness Continuous Integration contracts.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: cloud provider
  PricingUnit: vm-hour
  ProviderName: Harness
  PublisherName: Drone
  ServiceCategory: DevOps
  ServiceName: Drone CI (self-hosted)
layout: finops
meters:
- aggregation: sum
  description: Drone server VM hours (cloud-billed).
  dimensions:
  - cloud_account
  - region
  name: server_vm_hours
  unit: vm-hour
- aggregation: sum
  description: Drone runner VM hours (cloud-billed).
  dimensions:
  - cloud_account
  - runner_pool
  name: runner_vm_hours
  unit: vm-hour
- aggregation: avg
  description: Database, cache and artifact storage attached to Drone.
  dimensions:
  - cloud_account
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  description: Optional Harness CI subscription for the commercial successor.
  dimensions:
  - account
  name: harness_ci_subscription
  unit: contract-month
name: Drone Ci Finops
provider_name: Drone
provider_slug: drone-ci
publisher_name: Drone (Harness)
service_category: DevOps / CI/CD
slug: drone-ci-finops
source_filename: drone-ci-finops.yml
source_heading: FinOps Profile
source_url: https://github.com/harness/drone
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Drone\nproviderId: drone-ci\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- DevOps\n- CI/CD\n- Container-Native\n- Open Source\n- YAML\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Drone. As an open-source self-hosted CI,\n  Drone has no SaaS invoice; the cost surface is the underlying cloud spend\n  for the Drone server and runner pool. Customers needing commercial support\n  pay Harness via Harness Continuous Integration contracts.\nnotes: >-\n  Cost allocation is straightforward — the Drone server VM and runner VMs are\n  ordinary cloud resources tagged in your AWS/Azure/GCP account. Container/\n  registry storage and outbound network are usually a smaller fraction of\n  total spend than runner compute.\nsources:\n- https://github.com/harness/drone\n- https://www.harness.io/products/continuous-integration\n\
  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Drone (Harness)\nserviceCategory: DevOps / CI/CD\nbillingModel:\n  pricingCategory: Self-Hosted (no SaaS billing)\n  billingFrequency: Continuous (cloud-billed)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Drone CI (self-hosted)\n  ServiceCategory: DevOps\n  ProviderName: Harness\n  PublisherName: Drone\n  InvoiceIssuerName: cloud provider\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: vm-hour\nmeters:\n- name: server_vm_hours\n  description: Drone server VM hours (cloud-billed).\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - region\n- name: runner_vm_hours\n  description: Drone runner\
  \ VM hours (cloud-billed).\n  unit: vm-hour\n  aggregation: sum\n  dimensions:\n  - cloud_account\n  - runner_pool\n- name: storage_gb_month\n  description: Database, cache and artifact storage attached to Drone.\n  unit: GB-month\n  aggregation: avg\n  dimensions:\n  - cloud_account\n- name: harness_ci_subscription\n  description: Optional Harness CI subscription for the commercial successor.\n  unit: contract-month\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Tag Drone resources in your cloud account; consume FOCUS cost-export per cloud.\n- name: Allocation\n  description: Allocate runner-pool spend by team via runner labels and resource tags.\n- name: Optimization\n  description: Use spot/preemptible for runner pool; auto-scale to zero off-hours; right-size Drone server.\n- name: Accountability\n  description: Assign cluster/cloud-account owners; review CI runner spend monthly.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/drone-ci/refs/heads/main/finops/drone-ci-finops.yml
sources:
- https://github.com/harness/drone
- https://www.harness.io/products/continuous-integration
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Container-Native
- Open Source
- YAML
- FinOps
- Cost Management
- FOCUS
---
