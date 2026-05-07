---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: split-admin-api-openapi.yml
  format: yaml
  label: Split Admin API
  slug: split-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/openapi/split-admin-api-openapi.yml
- filename: split-feature-flag-api-openapi.yml
  format: yaml
  label: Split Feature Flag API
  slug: split-feature-flag-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/openapi/split-feature-flag-api-openapi.yml
- filename: split-evaluator-api-openapi.yml
  format: yaml
  label: Split Evaluator API
  slug: split-evaluator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/openapi/split-evaluator-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-MAU Annual Contract
description: FOCUS-aligned FinOps for Split.io (Harness FME).
focus_columns:
  BillingCurrency: USD
  ProviderName: Split.io (Harness FME)
  PublisherName: Split.io (Harness FME)
  ServiceCategory: Feature Management
  ServiceName: Split.io (Harness FME)
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: sum
  name: feature_flag_evaluations
  unit: evaluation
- aggregation: max
  name: experiments
  unit: experiment-month
- aggregation: max
  name: environments
  unit: env-month
name: Split Finops
provider_name: Split
provider_slug: split
publisher_name: Split.io (Harness FME)
service_category: Feature Management
slug: split-finops
source_filename: split-finops.yml
source_heading: FinOps Profile
source_url: https://www.harness.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Split.io (Harness FME)\nproviderId: split\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Feature Management\ndescription: FOCUS-aligned FinOps for Split.io (Harness FME).\nsources:\n  - https://www.harness.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Split.io (Harness FME)\nserviceCategory: Feature Management\nbillingModel:\n  pricingCategory: Per-MAU Annual Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Split.io (Harness FME)\n  ServiceCategory: Feature Management\n  ProviderName: Split.io (Harness FME)\n  PublisherName: Split.io (Harness FME)\n  BillingCurrency: USD\n\
  meters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name: feature_flag_evaluations\n    unit: evaluation\n    aggregation: sum\n  - name: experiments\n    unit: experiment-month\n    aggregation: max\n  - name: environments\n    unit: env-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Split.io (Harness FME) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/split/refs/heads/main/finops/split-finops.yml
sources:
- https://www.harness.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Feature Management
---
