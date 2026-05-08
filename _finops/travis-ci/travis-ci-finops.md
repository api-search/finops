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
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps profile for Travis CI. Billing is plan-based with build credit consumption tracked against the plan's monthly/annual budget; Unlimited plans bill a flat seat fee. Server (on-prem) plans bill a flat monthly per-instance fee. The customer's own infrastructure cost applies only to Server deployments.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Travis CI
  PricingUnit: build-credit
  ProviderName: Travis CI
  PublisherName: Travis CI
  ServiceCategory: DevOps
  ServiceName: Travis CI
layout: finops
meters:
- aggregation: sum
  description: Linux/macOS/Windows/GPU build credits consumed by jobs.
  dimensions:
  - organization
  - repository
  - os
  name: build_credits
  unit: credit
- aggregation: max
  description: Peak concurrent jobs.
  dimensions:
  - organization
  name: concurrent_jobs
  unit: jobs
- aggregation: sum
  description: Monthly/annual subscription fee per plan.
  dimensions:
  - organization
  - plan
  name: subscription_seat
  unit: month
- aggregation: sum
  description: On-prem Travis CI Server license fee per instance.
  dimensions:
  - account
  name: server_instance_month
  unit: instance-month
name: Travis Ci Finops
provider_name: Travis CI
provider_slug: travis-ci
publisher_name: Travis CI
service_category: DevOps / CI/CD
slug: travis-ci-finops
source_filename: travis-ci-finops.yml
source_heading: FinOps Profile
source_url: https://www.travis-ci.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Travis CI\nproviderId: travis-ci\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- DevOps\n- CI/CD\n- Build\n- Open Source\n- Hosted\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Travis CI. Billing is plan-based with build\n  credit consumption tracked against the plan's monthly/annual budget;\n  Unlimited plans bill a flat seat fee. Server (on-prem) plans bill a flat\n  monthly per-instance fee. The customer's own infrastructure cost applies\n  only to Server deployments.\nnotes: >-\n  Build credits are the unit of consumption inside Travis. Premium VM jobs\n  consume credits at higher rates than Linux jobs; macOS / Windows / GPU\n  multipliers vary. The Travis dashboard exposes a per-organization usage page\n  for chargeback.\nsources:\n- https://www.travis-ci.com/pricing/\n- https://docs.travis-ci.com/user/billing-overview/\n\
  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Travis CI\nserviceCategory: DevOps / CI/CD\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly / Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Travis CI\n  ServiceCategory: DevOps\n  ProviderName: Travis CI\n  PublisherName: Travis CI\n  InvoiceIssuerName: Travis CI\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: build-credit\nmeters:\n- name: build_credits\n  description: Linux/macOS/Windows/GPU build credits consumed by jobs.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - organization\n  - repository\n  - os\n- name: concurrent_jobs\n  description: Peak concurrent jobs.\n\
  \  unit: jobs\n  aggregation: max\n  dimensions:\n  - organization\n- name: subscription_seat\n  description: Monthly/annual subscription fee per plan.\n  unit: month\n  aggregation: sum\n  dimensions:\n  - organization\n  - plan\n- name: server_instance_month\n  description: On-prem Travis CI Server license fee per instance.\n  unit: instance-month\n  aggregation: sum\n  dimensions:\n  - account\nprinciples:\n- name: Visibility\n  description: Use the Travis CI organization Usage page; reconcile against monthly invoice.\n- name: Allocation\n  description: Allocate by organization, then by repository; map to FOCUS ResourceTag.\n- name: Optimization\n  description: Cache aggressively; gate slow tests; use Linux instead of premium VMs where viable; right-size plan to actual concurrency.\n- name: Accountability\n  description: Assign organization owners; alert on credit burn-down toward plan ceiling.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/travis-ci/refs/heads/main/finops/travis-ci-finops.yml
sources:
- https://www.travis-ci.com/pricing/
- https://docs.travis-ci.com/user/billing-overview/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DevOps
- CI/CD
- Build
- Open Source
- Hosted
- FinOps
- Cost Management
- FOCUS
---
