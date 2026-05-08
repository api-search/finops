---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: retool-management-api-openapi.yml
  format: yaml
  label: Retool Management API
  slug: retool-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/retool/refs/heads/main/openapi/retool-management-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Retool. Spend is per-builder subscription plus per-end-user (internal and external) charges and plan-bound workflow-run quotas. The Management and SCIM APIs are administrative and not separately metered.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Retool, Inc.
  ProviderName: Retool
  PublisherName: Retool, Inc.
  ServiceCategory: Internal Tools
  ServiceName: Retool
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: builder_seats
  unit: seat
- aggregation: sum
  dimensions:
  - tier
  name: internal_end_users
  unit: user
- aggregation: sum
  dimensions:
  - portal
  name: external_users
  unit: user
- aggregation: sum
  dimensions:
  - workflow
  name: workflow_runs
  unit: run
- aggregation: max
  name: retool_database
  unit: GB
name: Retool Finops
provider_name: Retool
provider_slug: retool
publisher_name: Retool, Inc.
service_category: Internal Tools
slug: retool-finops
source_filename: retool-finops.yml
source_heading: FinOps Profile
source_url: https://retool.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Retool\nproviderId: retool\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Internal Tools\n  - Low Code\ndescription: FOCUS-aligned FinOps for Retool. Spend is per-builder subscription plus per-end-user (internal\n  and external) charges and plan-bound workflow-run quotas. The Management and SCIM APIs are administrative\n  and not separately metered.\nsources:\n  - https://retool.com/pricing\n  - https://docs.retool.com/org-users/concepts/retool-api\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Retool, Inc.\nserviceCategory: Internal Tools\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: Retool\n  ServiceCategory: Internal Tools\n  ProviderName: Retool\n  PublisherName: Retool, Inc.\n  InvoiceIssuerName: Retool, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: builder_seats\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: internal_end_users\n    unit: user\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: external_users\n    unit: user\n    aggregation: sum\n    dimensions:\n      - portal\n  - name: workflow_runs\n    unit: run\n    aggregation: sum\n    dimensions:\n      - workflow\n  - name: retool_database\n    unit: GB\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Visibility comes from the Retool admin billing page and the Management API's user/group\n      endpoints; export builder, internal-user, and external-user counts to your finance pipeline.\n  - name: Allocation\n    description:\
  \ Allocate builder seats to the engineering or ops team that owns the apps, internal end-users\n      to the consuming line of business, and external users to the customer-facing product the portal\n      serves.\n  - name: Optimization\n    description: Optimization levers are seat hygiene (reclaim inactive builders), promoting builders\n      to internal end-users when they stop editing, sizing the Business external-user tier to the active\n      portal population, and consolidating workflows to stay under the plan's run quota.\n  - name: Accountability\n    description: Owner is the Retool admin / platform team that controls user provisioning (often via\n      the SCIM 2.0 API and SSO) and assigns workspaces to consuming teams.\nnotes: Per-builder + per-end-user subscription with workflow-run and database quotas; the Management\n  and SCIM APIs are administrative, not separately metered. Generic per-request meters and unit economics\n  removed.\nmaintainers:\n  - FN: Kin Lane\n    email:\
  \ kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/retool/refs/heads/main/finops/retool-finops.yml
sources:
- https://retool.com/pricing
- https://docs.retool.com/org-users/concepts/retool-api
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Internal Tools
- Low Code
---
