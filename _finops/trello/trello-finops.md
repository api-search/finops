---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: trello-rest-api-openapi.yml
  format: yaml
  label: Trello REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trello/refs/heads/main/openapi/trello-rest-api-openapi.yml
- filename: trello-webhooks-asyncapi.yml
  format: yaml
  label: Trello Webhooks API
  slug: webhooks-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/trello/refs/heads/main/asyncapi/trello-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription
description: FOCUS-aligned FinOps for Trello.
focus_columns:
  BillingCurrency: USD
  ProviderName: Trello
  PublisherName: Trello
  ServiceCategory: Kanban / Project Management
  ServiceName: Trello
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: max
  name: boards
  unit: board-month
- aggregation: sum
  name: automation_runs
  unit: run
name: Trello Finops
provider_name: trello
provider_slug: trello
publisher_name: Trello
service_category: Kanban / Project Management
slug: trello-finops
source_filename: trello-finops.yml
source_heading: FinOps Profile
source_url: https://trello.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trello\nproviderId: trello\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Kanban / Project Management\ndescription: FOCUS-aligned FinOps for Trello.\nsources:\n  - https://trello.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Trello\nserviceCategory: Kanban / Project Management\nbillingModel:\n  pricingCategory: Per-User Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Trello\n  ServiceCategory: Kanban / Project Management\n  ProviderName: Trello\n  PublisherName: Trello\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n\
  \    dimensions:\n      - plan\n  - name: boards\n    unit: board-month\n    aggregation: max\n  - name: automation_runs\n    unit: run\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Trello consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trello/refs/heads/main/finops/trello-finops.yml
sources:
- https://trello.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Kanban / Project Management
---
