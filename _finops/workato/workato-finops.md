---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: workato-developer-api-openapi.yml
  format: yaml
  label: Workato
  slug: workato
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workato/refs/heads/main/openapi/workato-developer-api-openapi.yml
- filename: workato-event-streams-openapi.yml
  format: yaml
  label: Workato Event Streams Public API
  slug: event-streams-public-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workato/refs/heads/main/openapi/workato-event-streams-openapi.yml
- filename: workato-mcp-server-openapi.yml
  format: yaml
  label: Workato MCP Server API
  slug: mcp-server-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workato/refs/heads/main/openapi/workato-mcp-server-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Annual (Recipes + Tasks + Connectors)
description: FOCUS-aligned FinOps for Workato.
focus_columns:
  BillingCurrency: USD
  ProviderName: Workato
  PublisherName: Workato
  ServiceCategory: iPaaS
  ServiceName: Workato
layout: finops
meters:
- aggregation: sum
  dimensions:
  - recipe
  - connector
  name: tasks_consumed
  unit: task
- aggregation: max
  name: recipes_active
  unit: recipe-month
- aggregation: max
  name: high_volume_recipes
  unit: hvr-month
- aggregation: max
  name: user_seats
  unit: seat-month
- aggregation: max
  name: premium_connectors
  unit: connector-month
name: Workato Finops
provider_name: Workato
provider_slug: workato
publisher_name: Workato
service_category: iPaaS
slug: workato-finops
source_filename: workato-finops.yml
source_heading: FinOps Profile
source_url: https://www.workato.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Workato\nproviderId: workato\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - iPaaS\ndescription: FOCUS-aligned FinOps for Workato.\nsources:\n  - https://www.workato.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Workato\nserviceCategory: iPaaS\nbillingModel:\n  pricingCategory: Custom Annual (Recipes + Tasks + Connectors)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Workato\n  ServiceCategory: iPaaS\n  ProviderName: Workato\n  PublisherName: Workato\n  BillingCurrency: USD\nmeters:\n  - name: tasks_consumed\n    unit: task\n    aggregation: sum\n    dimensions:\n      - recipe\n\
  \      - connector\n  - name: recipes_active\n    unit: recipe-month\n    aggregation: max\n  - name: high_volume_recipes\n    unit: hvr-month\n    aggregation: max\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n  - name: premium_connectors\n    unit: connector-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Workato consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workato/refs/heads/main/finops/workato-finops.yml
sources:
- https://www.workato.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- iPaaS
---
