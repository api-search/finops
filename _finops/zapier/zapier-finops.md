---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: zapier-partner-api.yml
  format: yaml
  label: Zapier Partner API
  slug: partner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zapier/refs/heads/main/openapi/zapier-partner-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Task-Based
description: FOCUS-aligned FinOps for Zapier.
focus_columns:
  BillingCurrency: USD
  ProviderName: Zapier
  PublisherName: Zapier
  ServiceCategory: Workflow Automation
  ServiceName: Zapier
layout: finops
meters:
- aggregation: sum
  dimensions:
  - zap
  name: tasks_consumed
  unit: task
- aggregation: max
  name: user_seats
  unit: seat-month
- aggregation: max
  name: active_zaps
  unit: zap-month
- aggregation: sum
  name: ai_actions
  unit: action
name: Zapier Finops
provider_name: Zapier
provider_slug: zapier
publisher_name: Zapier
service_category: Workflow Automation
slug: zapier-finops
source_filename: zapier-finops.yml
source_heading: FinOps Profile
source_url: https://zapier.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Zapier\nproviderId: zapier\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Workflow Automation\ndescription: FOCUS-aligned FinOps for Zapier.\nsources:\n  - https://zapier.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Zapier\nserviceCategory: Workflow Automation\nbillingModel:\n  pricingCategory: Subscription + Task-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Zapier\n  ServiceCategory: Workflow Automation\n  ProviderName: Zapier\n  PublisherName: Zapier\n  BillingCurrency: USD\nmeters:\n  - name: tasks_consumed\n    unit: task\n    aggregation: sum\n    dimensions:\n\
  \      - zap\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n  - name: active_zaps\n    unit: zap-month\n    aggregation: max\n  - name: ai_actions\n    unit: action\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Zapier consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zapier/refs/heads/main/finops/zapier-finops.yml
sources:
- https://zapier.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Workflow Automation
---
