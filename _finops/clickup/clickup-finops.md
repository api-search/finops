---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: clickup-tasks-openapi.yml
  format: yaml
  label: ClickUp Tasks API
  slug: tasks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-tasks-openapi.yml
- filename: clickup-spaces-openapi.yml
  format: yaml
  label: ClickUp Spaces API
  slug: spaces-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-spaces-openapi.yml
- filename: clickup-lists-openapi.yml
  format: yaml
  label: ClickUp Lists API
  slug: lists-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-lists-openapi.yml
- filename: clickup-folders-openapi.yml
  format: yaml
  label: ClickUp Folders API
  slug: folders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-folders-openapi.yml
- filename: clickup-goals-openapi.yml
  format: yaml
  label: ClickUp Goals API
  slug: goals-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-goals-openapi.yml
- filename: clickup-comments-openapi.yml
  format: yaml
  label: ClickUp Comments API
  slug: comments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-comments-openapi.yml
- filename: clickup-teams-openapi.yml
  format: yaml
  label: ClickUp Teams (Workspaces) API
  slug: teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-teams-openapi.yml
- filename: clickup-webhooks-openapi.yml
  format: yaml
  label: ClickUp Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-webhooks-openapi.yml
- filename: clickup-custom-fields-openapi.yml
  format: yaml
  label: ClickUp Custom Fields API
  slug: custom-fields-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-custom-fields-openapi.yml
- filename: clickup-time-tracking-openapi.yml
  format: yaml
  label: ClickUp Time Tracking API
  slug: time-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-time-tracking-openapi.yml
- filename: clickup-views-openapi.yml
  format: yaml
  label: ClickUp Views API
  slug: views-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-views-openapi.yml
- filename: clickup-oauth-openapi.yml
  format: yaml
  label: ClickUp OAuth API
  slug: oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/openapi/clickup-oauth-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for ClickUp.
focus_columns:
  BillingCurrency: USD
  ProviderName: ClickUp
  PublisherName: ClickUp
  ServiceCategory: Project Management
  ServiceName: ClickUp
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: automations
  unit: automation-run
- aggregation: max
  name: storage
  unit: GB-month
name: Clickup Finops
provider_name: clickup
provider_slug: clickup
publisher_name: ClickUp
service_category: Project Management
slug: clickup-finops
source_filename: clickup-finops.yml
source_heading: FinOps Profile
source_url: https://clickup.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ClickUp\nproviderId: clickup\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Project Management\ndescription: FOCUS-aligned FinOps for ClickUp.\nsources:\n  - https://clickup.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: ClickUp\nserviceCategory: Project Management\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: ClickUp\n  ServiceCategory: Project Management\n  ProviderName: ClickUp\n  PublisherName: ClickUp\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n\
  \      - plan\n  - name: automations\n    unit: automation-run\n    aggregation: sum\n  - name: storage\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track ClickUp consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clickup/refs/heads/main/finops/clickup-finops.yml
sources:
- https://clickup.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Project Management
---
