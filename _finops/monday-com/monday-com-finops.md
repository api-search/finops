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
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for monday.com.
focus_columns:
  BillingCurrency: USD
  ProviderName: monday.com
  PublisherName: monday.com
  ServiceCategory: Work Management
  ServiceName: monday.com
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: automation_actions
  unit: action
- aggregation: sum
  name: integration_actions
  unit: action
- aggregation: sum
  name: ai_credits
  unit: credit
name: Monday Com Finops
provider_name: Monday.com
provider_slug: monday-com
publisher_name: monday.com
service_category: Work Management
slug: monday-com-finops
source_filename: monday-com-finops.yml
source_heading: FinOps Profile
source_url: https://monday.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: monday.com\nproviderId: monday-com\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Work Management\ndescription: FOCUS-aligned FinOps for monday.com.\nsources:\n  - https://monday.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: monday.com\nserviceCategory: Work Management\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: monday.com\n  ServiceCategory: Work Management\n  ProviderName: monday.com\n  PublisherName: monday.com\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n   \
  \ dimensions:\n      - plan\n  - name: automation_actions\n    unit: action\n    aggregation: sum\n  - name: integration_actions\n    unit: action\n    aggregation: sum\n  - name: ai_credits\n    unit: credit\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track monday.com consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/monday-com/refs/heads/main/finops/monday-com-finops.yml
sources:
- https://monday.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Work Management
---
