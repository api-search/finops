---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Connection + Usage
description: FOCUS-aligned FinOps for Nango.
focus_columns:
  BillingCurrency: USD
  ProviderName: Nango
  PublisherName: Nango
  ServiceCategory: Integrations Platform
  ServiceName: Nango
layout: finops
meters:
- aggregation: max
  name: active_connections
  unit: connection-month
- aggregation: sum
  name: proxy_requests
  unit: request
- aggregation: sum
  name: function_compute_hours
  unit: hour
- aggregation: sum
  name: function_runs
  unit: run
- aggregation: max
  name: sync_storage_records
  unit: record
- aggregation: sum
  name: webhooks_delivered
  unit: webhook
name: Nango Finops
provider_name: Nango
provider_slug: nango
publisher_name: Nango
service_category: Integrations Platform
slug: nango-finops
source_filename: nango-finops.yml
source_heading: FinOps Profile
source_url: https://www.nango.dev/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Nango\nproviderId: nango\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Integrations Platform\ndescription: FOCUS-aligned FinOps for Nango.\nsources:\n  - https://www.nango.dev/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Nango\nserviceCategory: Integrations Platform\nbillingModel:\n  pricingCategory: Per-Connection + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Nango\n  ServiceCategory: Integrations Platform\n  ProviderName: Nango\n  PublisherName: Nango\n  BillingCurrency: USD\nmeters:\n  - name: active_connections\n    unit: connection-month\n    aggregation: max\n  -\
  \ name: proxy_requests\n    unit: request\n    aggregation: sum\n  - name: function_compute_hours\n    unit: hour\n    aggregation: sum\n  - name: function_runs\n    unit: run\n    aggregation: sum\n  - name: sync_storage_records\n    unit: record\n    aggregation: max\n  - name: webhooks_delivered\n    unit: webhook\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Nango consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/nango/refs/heads/main/finops/nango-finops.yml
sources:
- https://www.nango.dev/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Integrations Platform
---
