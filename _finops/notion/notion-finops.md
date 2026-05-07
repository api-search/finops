---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: notion-openapi.yml
  format: yaml
  label: Notion API
  slug: notion
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/notion/refs/heads/main/openapi/notion-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Seat Subscription
description: FOCUS-aligned FinOps for Notion.
focus_columns:
  BillingCurrency: USD
  ProviderName: Notion
  PublisherName: Notion
  ServiceCategory: Productivity
  ServiceName: Notion
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: member_seats
  unit: seat-month
- aggregation: sum
  name: ai_credits
  unit: credit
- aggregation: max
  name: external_guests
  unit: guest-month
name: Notion Finops
provider_name: Notion
provider_slug: notion
publisher_name: Notion
service_category: Productivity
slug: notion-finops
source_filename: notion-finops.yml
source_heading: FinOps Profile
source_url: https://www.notion.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Notion\nproviderId: notion\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Productivity\ndescription: FOCUS-aligned FinOps for Notion.\nsources:\n  - https://www.notion.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Notion\nserviceCategory: Productivity\nbillingModel:\n  pricingCategory: Per-Seat Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Notion\n  ServiceCategory: Productivity\n  ProviderName: Notion\n  PublisherName: Notion\n  BillingCurrency: USD\nmeters:\n  - name: member_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  -\
  \ name: ai_credits\n    unit: credit\n    aggregation: sum\n  - name: external_guests\n    unit: guest-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Notion consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/notion/refs/heads/main/finops/notion-finops.yml
sources:
- https://www.notion.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Productivity
---
