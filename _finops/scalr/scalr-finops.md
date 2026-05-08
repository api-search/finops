---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: scalr-user-openapi.yml
  format: yaml
  label: Scalr User API
  slug: scalr-user-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scalr/refs/heads/main/openapi/scalr-user-openapi.yml
- filename: scalr-account-openapi.yml
  format: yaml
  label: Scalr Account API
  slug: scalr-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scalr/refs/heads/main/openapi/scalr-account-openapi.yml
- filename: scalr-global-openapi.yml
  format: yaml
  label: Scalr Global API
  slug: scalr-global-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/scalr/refs/heads/main/openapi/scalr-global-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Usage-Based
description: 'FOCUS-aligned FinOps for Scalr: Terraform / OpenTofu remote-operations platform billed on monthly runs, with unlimited users and resources included. Cost levers are run consumption (deduplication, drift-detection cadence) and tier choice (Business vs Enterprise commitment).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Scalr, Inc.
  ProviderName: Scalr
  PublisherName: Scalr, Inc.
  ServiceCategory: Developer Tools
  ServiceName: Scalr
layout: finops
meters:
- aggregation: sum
  dimensions:
  - workspace
  - environment
  - account
  name: terraform_runs
  unit: run
- aggregation: sum
  dimensions:
  - workspace
  - schedule
  name: drift_detection_runs
  unit: run
- aggregation: max
  dimensions:
  - account
  name: self_hosted_agents
  unit: agent
name: Scalr Finops
provider_name: Scalr
provider_slug: scalr
publisher_name: Scalr, Inc.
service_category: Developer Tools
slug: scalr-finops
source_filename: scalr-finops.yml
source_heading: FinOps Profile
source_url: https://www.scalr.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Scalr\nproviderId: scalr\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Terraform\n  - GitOps\ndescription: 'FOCUS-aligned FinOps for Scalr: Terraform / OpenTofu remote-operations platform\n  billed on monthly runs, with unlimited users and resources included. Cost levers are run\n  consumption (deduplication, drift-detection cadence) and tier choice (Business vs Enterprise\n  commitment).'\nsources:\n  - https://www.scalr.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Scalr, Inc.\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Scalr\n  ServiceCategory: Developer Tools\n  ProviderName: Scalr\n  PublisherName: Scalr, Inc.\n  InvoiceIssuerName: Scalr, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: terraform_runs\n    unit: run\n    aggregation: sum\n    dimensions:\n      - workspace\n      - environment\n      - account\n  - name: drift_detection_runs\n    unit: run\n    aggregation: sum\n    dimensions:\n      - workspace\n      - schedule\n  - name: self_hosted_agents\n    unit: agent\n    aggregation: max\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Track Terraform run counts per workspace and environment in the Scalr\n      UI; export run history for monthly reconciliation against the Scalr invoice.\n  - name: Allocation\n    description: Use Scalr environments and workspace ownership metadata to attribute runs\n      to teams or applications; tag downstream\
  \ cloud resources via Terraform for cross-platform\n      chargeback.\n  - name: Optimization\n    description: Reduce billable runs by tightening drift-detection cadence, using plan-only\n      runs for CI checks, batching changes, and consolidating workspaces where ownership\n      allows. Reserve Enterprise commitment for predictable workloads ≥20K runs/year.\n  - name: Accountability\n    description: Assign a workspace owner per environment; review monthly run counts against\n      the Business or Enterprise commitment and resize commitment annually.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalr/refs/heads/main/finops/scalr-finops.yml
sources:
- https://www.scalr.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Terraform
- GitOps
---
