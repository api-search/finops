---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: linear-graphql-openapi.yml
  format: yaml
  label: Linear GraphQL API
  slug: linear-graphql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/linear/refs/heads/main/openapi/linear-graphql-openapi.yml
- filename: linear-webhooks-asyncapi.yml
  format: yaml
  label: Linear Webhooks API
  slug: linear-webhooks-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/linear/refs/heads/main/asyncapi/linear-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Linear.
focus_columns:
  BillingCurrency: USD
  ProviderName: Linear
  PublisherName: Linear
  ServiceCategory: Issue Tracking
  ServiceName: Linear
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  - team
  name: user_seats
  unit: seat-month
- aggregation: max
  name: guest_accounts
  unit: guest-month
name: Linear Finops
provider_name: linear
provider_slug: linear
publisher_name: Linear
service_category: Issue Tracking
slug: linear-finops
source_filename: linear-finops.yml
source_heading: FinOps Profile
source_url: https://linear.app/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Linear\nproviderId: linear\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Issue Tracking\ndescription: FOCUS-aligned FinOps for Linear.\nsources:\n  - https://linear.app/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Linear\nserviceCategory: Issue Tracking\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Linear\n  ServiceCategory: Issue Tracking\n  ProviderName: Linear\n  PublisherName: Linear\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n   \
  \   - team\n  - name: guest_accounts\n    unit: guest-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Linear consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linear/refs/heads/main/finops/linear-finops.yml
sources:
- https://linear.app/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Issue Tracking
---
