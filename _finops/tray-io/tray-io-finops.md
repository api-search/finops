---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tray-io-platform-api-openapi.yml
  format: yaml
  label: Tray.io Platform API
  slug: tray-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tray-io/refs/heads/main/openapi/tray-io-platform-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Custom Per-Workspace + Tasks (Quarterly Billing)
description: FOCUS-aligned FinOps for Tray.io.
focus_columns:
  BillingCurrency: USD
  ProviderName: Tray.io
  PublisherName: Tray.io
  ServiceCategory: iPaaS
  ServiceName: Tray.io
layout: finops
meters:
- aggregation: sum
  dimensions:
  - workflow
  - connector
  name: tasks_consumed
  unit: task
- aggregation: max
  name: workflows_active
  unit: workflow-month
- aggregation: max
  name: user_seats
  unit: seat-month
name: Tray Io Finops
provider_name: Tray.io
provider_slug: tray-io
publisher_name: Tray.io
service_category: iPaaS
slug: tray-io-finops
source_filename: tray-io-finops.yml
source_heading: FinOps Profile
source_url: https://tray.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tray.io\nproviderId: tray-io\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - iPaaS\ndescription: FOCUS-aligned FinOps for Tray.io.\nsources:\n  - https://tray.ai/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tray.io\nserviceCategory: iPaaS\nbillingModel:\n  pricingCategory: Custom Per-Workspace + Tasks (Quarterly Billing)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Tray.io\n  ServiceCategory: iPaaS\n  ProviderName: Tray.io\n  PublisherName: Tray.io\n  BillingCurrency: USD\nmeters:\n  - name: tasks_consumed\n    unit: task\n    aggregation: sum\n    dimensions:\n      - workflow\n\
  \      - connector\n  - name: workflows_active\n    unit: workflow-month\n    aggregation: max\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Tray.io consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tray-io/refs/heads/main/finops/tray-io-finops.yml
sources:
- https://tray.ai/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- iPaaS
---
