---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: pipedream-openapi.yml
  format: yaml
  label: Pipedream REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pipedream/refs/heads/master/openapi/pipedream-openapi.yml
- filename: pipedream-openapi.yml
  format: yaml
  label: Pipedream Connect API
  slug: connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/pipedream/refs/heads/master/openapi/pipedream-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Credit-Based
description: FOCUS-aligned FinOps for Pipedream.
focus_columns:
  BillingCurrency: USD
  ProviderName: Pipedream
  PublisherName: Pipedream
  ServiceCategory: Workflow Automation
  ServiceName: Pipedream
layout: finops
meters:
- aggregation: sum
  name: credits_consumed
  unit: credit
- aggregation: sum
  name: workflow_executions
  unit: execution
- aggregation: sum
  name: events_received
  unit: event
- aggregation: max
  name: active_workflows
  unit: workflow-month
name: Pipedream Finops
provider_name: Pipedream
provider_slug: pipedream
publisher_name: Pipedream
service_category: Workflow Automation
slug: pipedream-finops
source_filename: pipedream-finops.yml
source_heading: FinOps Profile
source_url: https://pipedream.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Pipedream\nproviderId: pipedream\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Workflow Automation\ndescription: FOCUS-aligned FinOps for Pipedream.\nsources:\n  - https://pipedream.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Pipedream\nserviceCategory: Workflow Automation\nbillingModel:\n  pricingCategory: Subscription + Credit-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Pipedream\n  ServiceCategory: Workflow Automation\n  ProviderName: Pipedream\n  PublisherName: Pipedream\n  BillingCurrency: USD\nmeters:\n  - name: credits_consumed\n    unit: credit\n    aggregation:\
  \ sum\n  - name: workflow_executions\n    unit: execution\n    aggregation: sum\n  - name: events_received\n    unit: event\n    aggregation: sum\n  - name: active_workflows\n    unit: workflow-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Pipedream consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/pipedream/refs/heads/main/finops/pipedream-finops.yml
sources:
- https://pipedream.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Workflow Automation
---
