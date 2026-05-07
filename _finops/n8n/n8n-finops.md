---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: n8n-openapi.yml
  format: yaml
  label: N8n REST API
  slug: n8n-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/n8n/refs/heads/main/openapi/n8n-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription with Execution Quota
description: FOCUS-aligned FinOps for n8n.
focus_columns:
  BillingCurrency: USD
  ProviderName: n8n
  PublisherName: n8n
  ServiceCategory: Workflow Automation
  ServiceName: n8n
layout: finops
meters:
- aggregation: sum
  name: workflow_executions
  unit: execution
- aggregation: max
  name: active_workflows
  unit: workflow-month
- aggregation: sum
  name: ai_credits
  unit: credit
- aggregation: max
  name: shared_projects
  unit: project-month
name: N8N Finops
provider_name: N8n
provider_slug: n8n
publisher_name: n8n
service_category: Workflow Automation
slug: n8n-finops
source_filename: n8n-finops.yml
source_heading: FinOps Profile
source_url: https://n8n.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: n8n\nproviderId: n8n\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Workflow Automation\ndescription: FOCUS-aligned FinOps for n8n.\nsources:\n  - https://n8n.io/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: n8n\nserviceCategory: Workflow Automation\nbillingModel:\n  pricingCategory: Subscription with Execution Quota\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: n8n\n  ServiceCategory: Workflow Automation\n  ProviderName: n8n\n  PublisherName: n8n\n  BillingCurrency: USD\nmeters:\n  - name: workflow_executions\n    unit: execution\n    aggregation: sum\n  - name: active_workflows\n\
  \    unit: workflow-month\n    aggregation: max\n  - name: ai_credits\n    unit: credit\n    aggregation: sum\n  - name: shared_projects\n    unit: project-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track n8n consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/n8n/refs/heads/main/finops/n8n-finops.yml
sources:
- https://n8n.io/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Workflow Automation
---
