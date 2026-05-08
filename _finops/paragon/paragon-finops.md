---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: paragon-proxy-api-openapi.yml
  format: yaml
  label: Proxy API
  slug: proxy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/openapi/paragon-proxy-api-openapi.yml
- filename: paragon-users-api-openapi.yml
  format: yaml
  label: Users API
  slug: users-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/openapi/paragon-users-api-openapi.yml
- filename: paragon-task-history-api-openapi.yml
  format: yaml
  label: Task History API
  slug: task-history-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/openapi/paragon-task-history-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom by Connected Users
description: FOCUS-aligned FinOps for Paragon.
focus_columns:
  BillingCurrency: USD
  ProviderName: Paragon
  PublisherName: Paragon
  ServiceCategory: Embedded Integrations
  ServiceName: Paragon
layout: finops
meters:
- aggregation: max
  name: connected_users
  unit: user-month
- aggregation: sum
  name: workflow_executions
  unit: execution
- aggregation: max
  name: active_integrations
  unit: integration-month
- aggregation: sum
  name: actionkit_calls
  unit: call
name: Paragon Finops
provider_name: Paragon
provider_slug: paragon
publisher_name: Paragon
service_category: Embedded Integrations
slug: paragon-finops
source_filename: paragon-finops.yml
source_heading: FinOps Profile
source_url: https://www.useparagon.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Paragon\nproviderId: paragon\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Embedded Integrations\ndescription: FOCUS-aligned FinOps for Paragon.\nsources:\n  - https://www.useparagon.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Paragon\nserviceCategory: Embedded Integrations\nbillingModel:\n  pricingCategory: Custom by Connected Users\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Paragon\n  ServiceCategory: Embedded Integrations\n  ProviderName: Paragon\n  PublisherName: Paragon\n  BillingCurrency: USD\nmeters:\n  - name: connected_users\n    unit: user-month\n    aggregation:\
  \ max\n  - name: workflow_executions\n    unit: execution\n    aggregation: sum\n  - name: active_integrations\n    unit: integration-month\n    aggregation: max\n  - name: actionkit_calls\n    unit: call\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Paragon consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/paragon/refs/heads/main/finops/paragon-finops.yml
sources:
- https://www.useparagon.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Embedded Integrations
---
