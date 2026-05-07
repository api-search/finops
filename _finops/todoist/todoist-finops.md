---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: todoist-openapi.yml
  format: yaml
  label: Todoist API
  slug: todoist-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/todoist/refs/heads/main/openapi/todoist-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Todoist: per-seat tiered SaaS subscription (Beginner free, Pro individual, Business team) billed monthly or annually. API access is bundled into the subscription, so cost allocation in this artifact tracks seats and team membership rather than per-request usage.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Doist Inc.
  PricingCategory: Subscription
  PricingUnit: seat-month
  ProviderName: Todoist
  PublisherName: Doist Inc.
  ServiceCategory: Productivity SaaS
  ServiceName: Todoist
layout: finops
meters:
- aggregation: sum
  description: One Pro-tier user seat for one month. Annual billing applies a 20% discount.
  dimensions:
  - billing_cycle
  - currency
  name: pro_seat_month
  unit: seat-month
- aggregation: sum
  description: One Business-tier user seat (team member or guest) for one month.
  dimensions:
  - billing_cycle
  - team
  - role
  name: business_seat_month
  unit: seat-month
- aggregation: max
  description: Count of active team projects (capped at 500 per Business team) for capacity tracking.
  dimensions:
  - team
  name: team_projects_active
  unit: project
- aggregation: sum
  description: Local tax applied to Business seats per the customer's jurisdiction.
  dimensions:
  - jurisdiction
  name: tax
  unit: month
name: Todoist Finops
provider_name: Todoist
provider_slug: todoist
publisher_name: Doist Inc.
service_category: Productivity SaaS
slug: todoist-finops
source_filename: todoist-finops.yml
source_heading: FinOps Profile
source_url: https://todoist.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Todoist\nproviderId: todoist\npublisherName: Doist Inc.\nserviceCategory: Productivity SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Productivity\n  - Tasks\n  - Task Management\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Todoist: per-seat tiered SaaS subscription (Beginner free, Pro\n  individual, Business team) billed monthly or annually. API access is bundled into the subscription,\n  so cost allocation in this artifact tracks seats and team membership rather than per-request usage.'\nsources:\n  - https://todoist.com/pricing\n  - https://developer.todoist.com/api/v1\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Todoist\n  ServiceCategory: Productivity SaaS\n  ProviderName: Todoist\n  PublisherName: Doist Inc.\n  InvoiceIssuerName: Doist Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\n  PricingUnit: seat-month\nmeters:\n  - name: pro_seat_month\n    description: One Pro-tier user seat for one month. Annual billing applies a 20% discount.\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - billing_cycle\n      - currency\n  - name: business_seat_month\n    description: One Business-tier user seat (team member or guest) for one month.\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - billing_cycle\n      - team\n      - role\n  - name: team_projects_active\n    description: Count of active team projects (capped\
  \ at 500 per Business team) for capacity tracking.\n    unit: project\n    aggregation: max\n    dimensions:\n      - team\n  - name: tax\n    description: Local tax applied to Business seats per the customer's jurisdiction.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - jurisdiction\nprinciples:\n  - name: Visibility\n    description: Pull invoices and seat counts from the Todoist Business admin console; reconcile against\n      the Pro/Business seat counts your team actually uses each month.\n  - name: Allocation\n    description: Use Business team workspaces and team folders to group seats by department or product;\n      Todoist supports centralized billing per team so chargeback can be done team-by-team.\n  - name: Optimization\n    description: Move heavy users from Pro to Business when team collaboration features are needed; convert\n      monthly subscriptions to annual on the Pro plan to capture the documented 20% discount; downgrade\n      idle Pro accounts\
  \ to Beginner.\n  - name: Accountability\n    description: Designate a workspace admin per Business team to own seat additions, role assignments,\n      and the activity log review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/todoist/refs/heads/main/finops/todoist-finops.yml
sources:
- https://todoist.com/pricing
- https://developer.todoist.com/api/v1
specification: FinOps Framework
tags:
- Productivity
- Tasks
- Task Management
- SaaS
- FinOps
- FOCUS
---
