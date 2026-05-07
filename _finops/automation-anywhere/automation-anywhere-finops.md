---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: automation-anywhere-control-room-openapi.yml
  format: yaml
  label: Automation Anywhere Control Room API
  slug: control-room-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-control-room-openapi.yml
- filename: automation-anywhere-bot-deploy-openapi.yml
  format: yaml
  label: Automation Anywhere Bot Deploy API
  slug: bot-deploy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-bot-deploy-openapi.yml
- filename: automation-anywhere-workload-management-openapi.yml
  format: yaml
  label: Automation Anywhere Workload Management API
  slug: workload-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-workload-management-openapi.yml
- filename: automation-anywhere-bot-insight-openapi.yml
  format: yaml
  label: Automation Anywhere Bot Insight API
  slug: bot-insight-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-bot-insight-openapi.yml
- filename: automation-anywhere-api-task-execution-openapi.yml
  format: yaml
  label: Automation Anywhere API Task Execution API
  slug: api-task-execution-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-api-task-execution-openapi.yml
- filename: automation-anywhere-credential-vault-openapi.yml
  format: yaml
  label: Automation Anywhere Credential Vault API
  slug: credential-vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-credential-vault-openapi.yml
- filename: automation-anywhere-repository-management-openapi.yml
  format: yaml
  label: Automation Anywhere Repository Management API
  slug: repository-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/openapi/automation-anywhere-repository-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  - Credit
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Automation Anywhere: subscription-based platform license sized by edition and licensed bot count, with separately licensed AI Agent Studio and Document Automation add-ons.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Automation Anywhere, Inc.
  ProviderName: Automation Anywhere
  PublisherName: Automation Anywhere, Inc.
  ServiceCategory: RPA / Intelligent Automation
  ServiceName: Automation Anywhere
layout: finops
meters:
- aggregation: max
  dimensions:
  - bot_type
  - edition
  name: licensed_bots
  unit: bot
- aggregation: sum
  dimensions:
  - edition
  - region
  name: control_room_subscription
  unit: month
- aggregation: sum
  dimensions:
  - model
  - bot
  name: ai_agent_studio_usage
  unit: invocation
- aggregation: sum
  dimensions:
  - document_type
  name: document_automation_pages
  unit: page
- aggregation: max
  name: copilot_seats
  unit: seat
name: Automation Anywhere Finops
provider_name: automation-anywhere
provider_slug: automation-anywhere
publisher_name: Automation Anywhere, Inc.
service_category: RPA / Intelligent Automation
slug: automation-anywhere-finops
source_filename: automation-anywhere-finops.yml
source_heading: FinOps Profile
source_url: https://www.automationanywhere.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Automation Anywhere\nproviderId: automation-anywhere\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Automation Anywhere pricing is not publicly posted; this artifact models the FinOps shape of an\n  Automation 360 deployment. Per-edition prices and bot counts come from the customer's signed order\n  form.\ntags:\n  - FinOps\n  - FOCUS\n  - RPA\n  - Intelligent Automation\ndescription: 'FOCUS-aligned FinOps for Automation Anywhere: subscription-based platform license sized\n  by edition and licensed bot count, with separately licensed AI Agent Studio and Document Automation\n  add-ons.'\nsources:\n  - https://www.automationanywhere.com/\n  - https://www.automationanywhere.com/products/automation-360\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Automation Anywhere, Inc.\nserviceCategory: RPA / Intelligent Automation\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Automation Anywhere\n  ServiceCategory: RPA / Intelligent Automation\n  ProviderName: Automation Anywhere\n  PublisherName: Automation Anywhere, Inc.\n  InvoiceIssuerName: Automation Anywhere, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: licensed_bots\n    unit: bot\n    aggregation: max\n    dimensions:\n      - bot_type\n      - edition\n  - name: control_room_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - edition\n      - region\n  - name: ai_agent_studio_usage\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - model\n      - bot\n  - name: document_automation_pages\n\
  \    unit: page\n    aggregation: sum\n    dimensions:\n      - document_type\n  - name: copilot_seats\n    unit: seat\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Use the Control Room's Bot Insight dashboards and the Activity API to see bot run\n      counts, durations, and queue throughput. Match against the order-form bot allocation to detect\n      under-utilization.\n  - name: Allocation\n    description: Tag bots and queues by business unit / process owner; chargeback by attributing bot\n      run minutes to the requesting team.\n  - name: Optimization\n    description: Right-size by retiring idle bots, consolidating attended licenses where the same user\n      uses multiple, and using AI Agent Studio for long-tail processes instead of dedicated bots.\n  - name: Accountability\n    description: Center of Excellence (CoE) typically owns Automation Anywhere spend; bot owners are\n      named on each automation and review utilization quarterly.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/automation-anywhere/refs/heads/main/finops/automation-anywhere-finops.yml
sources:
- https://www.automationanywhere.com/
- https://www.automationanywhere.com/products/automation-360
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- RPA
- Intelligent Automation
---
