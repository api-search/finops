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
  pricingCategory: Custom Session-Based Annual Contract
description: FOCUS-aligned FinOps for Heap.
focus_columns:
  BillingCurrency: USD
  ProviderName: Heap
  PublisherName: Heap
  ServiceCategory: Product Analytics
  ServiceName: Heap
layout: finops
meters:
- aggregation: sum
  name: monthly_sessions
  unit: session
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: max
  name: active_users
  unit: user
- aggregation: max
  name: subscription
  unit: month
name: Heap Finops
provider_name: Heap
provider_slug: heap
publisher_name: Heap
service_category: Product Analytics
slug: heap-finops
source_filename: heap-finops.yml
source_heading: FinOps Profile
source_url: https://heap.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Heap\nproviderId: heap\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Product Analytics\ndescription: FOCUS-aligned FinOps for Heap.\nsources:\n  - https://heap.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Heap\nserviceCategory: Product Analytics\nbillingModel:\n  pricingCategory: Custom Session-Based Annual Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Heap\n  ServiceCategory: Product Analytics\n  ProviderName: Heap\n  PublisherName: Heap\n  BillingCurrency: USD\nmeters:\n  - name: monthly_sessions\n    unit: session\n    aggregation: sum\n  - name: session_replays\n\
  \    unit: replay\n    aggregation: sum\n  - name: active_users\n    unit: user\n    aggregation: max\n  - name: subscription\n    unit: month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Heap consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/heap/refs/heads/main/finops/heap-finops.yml
sources:
- https://heap.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Product Analytics
---
