---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: wrike-openapi.yml
  format: yaml
  label: Wrike API
  slug: wrike
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/wrike/refs/heads/main/openapi/wrike-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Wrike: per-seat tiered SaaS subscription with paid add-ons. No per-API meter; spend is driven by seat count and add-on subscriptions invoiced in USD.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Wrike, Inc.
  ProviderName: Wrike
  PublisherName: Wrike, Inc.
  ServiceCategory: Work Management SaaS
  ServiceName: Wrike
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  - account
  name: seats
  unit: seat
- aggregation: sum
  dimensions:
  - addon
  - account
  name: addon_subscription
  unit: month
- aggregation: sum
  dimensions:
  - account
  - plan
  name: ai_elite_actions
  unit: action
name: Wrike Finops
provider_name: Wrike
provider_slug: wrike
publisher_name: Wrike, Inc.
service_category: Work Management SaaS
slug: wrike-finops
source_filename: wrike-finops.yml
source_heading: FinOps Profile
source_url: https://www.wrike.com/price/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Wrike\nproviderId: wrike\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Work Management\n  - Project Management\n  - SaaS\ndescription: 'FOCUS-aligned FinOps for Wrike: per-seat tiered SaaS subscription with paid add-ons.\n  No per-API meter; spend is driven by seat count and add-on subscriptions invoiced in USD.'\nsources:\n  - https://www.wrike.com/price/\n  - https://developers.wrike.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Wrike, Inc.\nserviceCategory: Work Management SaaS\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n\
  \    - Adjustment\nfocusColumns:\n  ServiceName: Wrike\n  ServiceCategory: Work Management SaaS\n  ProviderName: Wrike\n  PublisherName: Wrike, Inc.\n  InvoiceIssuerName: Wrike, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - plan\n      - account\n  - name: addon_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - addon\n      - account\n  - name: ai_elite_actions\n    unit: action\n    aggregation: sum\n    dimensions:\n      - account\n      - plan\nprinciples:\n  - name: Visibility\n    description: Wrike spend is visible at the account level via the Wrike admin billing page and\n      monthly invoices; API consumption is not separately metered, so usage telemetry comes from\n      Wrike Analyze / Datahub rather than a billing export.\n  - name: Allocation\n    description: Allocate by Wrike account and plan tier; multi-team customers split cost by\n      department via Wrike's account-group\
  \ structure or by exporting seat-assignment reports.\n  - name: Optimization\n    description: Levers are seat right-sizing (Team vs. Business vs. Pinnacle), pruning inactive\n      collaborators, and consolidating add-ons (Whiteboard / Integrate / Datahub) onto Apex when\n      AI Elite usage is heavy.\n  - name: Accountability\n    description: PMO or Operations typically owns the Wrike subscription; integration teams own\n      Wrike Integrate / Sync add-on consumption and AI Elite action budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/wrike/refs/heads/main/finops/wrike-finops.yml
sources:
- https://www.wrike.com/price/
- https://developers.wrike.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Work Management
- Project Management
- SaaS
---
