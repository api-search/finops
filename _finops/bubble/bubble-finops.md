---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bubble-data-api-openapi.yml
  format: yaml
  label: Bubble Data API
  slug: bubble-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bubble/refs/heads/main/openapi/bubble-data-api-openapi.yml
- filename: bubble-workflow-api-openapi.yml
  format: yaml
  label: Bubble Workflow API
  slug: bubble-workflow-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bubble/refs/heads/main/openapi/bubble-workflow-api-openapi.yml
- filename: bubble-plugin-api-openapi.yml
  format: yaml
  label: Bubble Plugin API
  slug: bubble-plugin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bubble/refs/heads/main/openapi/bubble-plugin-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Tiered Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Bubble: tiered subscription with bundled Workload

  Units, plus pay-as-you-go meters for additional WU, file storage, and

  bandwidth overages.

  '
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bubble Group, Inc.
  ProviderName: Bubble
  PublisherName: Bubble Group, Inc.
  ServiceCategory: Application Platform
  ServiceName: Bubble
  ServiceSubcategory: No-Code Application Builder
layout: finops
meters:
- aggregation: sum
  dimensions:
  - activity_type
  - app
  - environment
  name: workload_units
  unit: wu
- aggregation: sum
  dimensions:
  - plan_tier
  - billing_frequency
  - bundle_type
  name: subscription_fees
  unit: month
- aggregation: sum
  dimensions:
  - app
  - region
  name: bandwidth
  unit: GB-month
- aggregation: sum
  dimensions:
  - app
  name: file_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - app
  - month
  name: extra_workload_addon
  unit: wu
- aggregation: max
  dimensions:
  - plan_tier
  name: app_editors
  unit: seat-month
- aggregation: sum
  dimensions:
  - api
  - environment
  - workflow
  - data_type
  name: api_requests
  unit: request
name: Bubble Finops
provider_name: Bubble
provider_slug: bubble
publisher_name: Bubble Group, Inc.
service_category: Application Platform
slug: bubble-finops
source_filename: bubble-finops.yml
source_heading: FinOps Profile
source_url: https://bubble.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bubble\nproviderId: bubble\ncreated: '2026-05-06'\nmodified: '2026-05-06'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - No-Code\n  - Application Platform\n  - Cost Management\ndescription: |\n  FOCUS-aligned FinOps for Bubble: tiered subscription with bundled Workload\n  Units, plus pay-as-you-go meters for additional WU, file storage, and\n  bandwidth overages.\nsources:\n  - https://bubble.io/pricing\n  - https://manual.bubble.io/account-and-marketplace/account-and-billing/pricing-plans.md\n  - https://manual.bubble.io/help-guides/workload/understanding-workload.md\n  - https://manual.bubble.io/help-guides/workload/understanding-workload/activity-types.md\n  - https://manual.bubble.io/help-guides/workload/understanding-workload/the-workload-calculation.md\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n\
  \  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bubble Group, Inc.\nserviceCategory: Application Platform\nbillingModel:\n  pricingCategory: Tiered Subscription + Pay-As-You-Go\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Bubble\n  ServiceCategory: Application Platform\n  ServiceSubcategory: No-Code Application Builder\n  ProviderName: Bubble\n  PublisherName: Bubble Group, Inc.\n  InvoiceIssuerName: Bubble Group, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: workload_units\n    unit: wu\n    aggregation: sum\n    dimensions:\n      - activity_type\n      - app\n      - environment\n  - name: subscription_fees\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan_tier\n      - billing_frequency\n      - bundle_type\n  - name: bandwidth\n\
  \    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - app\n      - region\n  - name: file_storage\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - app\n  - name: extra_workload_addon\n    unit: wu\n    aggregation: sum\n    dimensions:\n      - app\n      - month\n  - name: app_editors\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan_tier\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - workflow\n      - data_type\nprinciples:\n  - name: Visibility\n    description: |\n      Use the in-app Workload dashboard (Logs > Workload) to see WU consumption\n      by activity type, page, scheduled workflow, plugin, and database\n      operation. The Server Logs and App Metrics dashboards expose request\n      counts and per-page render costs. Export usage data for chargeback to\n      external BI tools.\n  - name: Allocation\n    description: |\n      Allocate cost\
  \ by tagging Bubble apps to teams or products (one app per\n      product is the cleanest mapping; sub-apps with white-label allow\n      product-level allocation within Growth/Team plans). Use scheduled\n      workflow names and plugin labels to attribute WU to features.\n  - name: Optimization\n    description: |\n      Reduce server-side WU by indexing fields used in searches, paginating\n      large result sets, replacing repeated server-side actions with\n      client-side equivalents, batching writes via the Data API /bulk\n      endpoint, and consolidating chained scheduled workflows. Use Bubble's\n      Workload optimization guide and the Performance & Capacity dashboard\n      to identify hot spots.\n  - name: Accountability\n    description: |\n      Set WU usage alerts in Settings > Workload before crossing plan\n      thresholds; assign an app owner per Bubble app. Reconcile monthly\n      Bubble invoices against the Workload dashboard and review per-feature\n      WU costs\
  \ in product roadmap reviews.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bubble/refs/heads/main/finops/bubble-finops.yml
sources:
- https://bubble.io/pricing
- https://manual.bubble.io/account-and-marketplace/account-and-billing/pricing-plans.md
- https://manual.bubble.io/help-guides/workload/understanding-workload.md
- https://manual.bubble.io/help-guides/workload/understanding-workload/activity-types.md
- https://manual.bubble.io/help-guides/workload/understanding-workload/the-workload-calculation.md
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- No-Code
- Application Platform
- Cost Management
---
