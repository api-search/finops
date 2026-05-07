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
  pricingCategory: Per-MAU + Per-Connection
description: FOCUS-aligned FinOps for WorkOS.
focus_columns:
  BillingCurrency: USD
  ProviderName: WorkOS
  PublisherName: WorkOS
  ServiceCategory: B2B Identity
  ServiceName: WorkOS
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: max
  name: sso_connections
  unit: connection-month
- aggregation: max
  name: directory_sync_connections
  unit: connection-month
- aggregation: sum
  name: audit_log_events
  unit: event
name: Workos Finops
provider_name: WorkOS
provider_slug: workos
publisher_name: WorkOS
service_category: B2B Identity
slug: workos-finops
source_filename: workos-finops.yml
source_heading: FinOps Profile
source_url: https://workos.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: WorkOS\nproviderId: workos\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - B2B Identity\ndescription: FOCUS-aligned FinOps for WorkOS.\nsources:\n  - https://workos.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: WorkOS\nserviceCategory: B2B Identity\nbillingModel:\n  pricingCategory: Per-MAU + Per-Connection\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: WorkOS\n  ServiceCategory: B2B Identity\n  ProviderName: WorkOS\n  PublisherName: WorkOS\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name: sso_connections\n    unit:\
  \ connection-month\n    aggregation: max\n  - name: directory_sync_connections\n    unit: connection-month\n    aggregation: max\n  - name: audit_log_events\n    unit: event\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track WorkOS consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workos/refs/heads/main/finops/workos-finops.yml
sources:
- https://workos.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- B2B Identity
---
