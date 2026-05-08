---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: basecamp-api-openapi.yml
  format: yaml
  label: Basecamp API
  slug: basecamp-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/basecamp/refs/heads/main/openapi/basecamp-api-openapi.yml
- filename: basecamp-webhooks-asyncapi.yml
  format: yaml
  label: Basecamp Webhooks
  slug: basecamp-webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/basecamp/refs/heads/main/asyncapi/basecamp-webhooks-asyncapi.yml
- filename: basecamp-oauth-openapi.yml
  format: yaml
  label: Basecamp OAuth
  slug: basecamp-oauth
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/basecamp/refs/heads/main/openapi/basecamp-oauth-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Basecamp: tiered SaaS subscription with two billing shapes — per-user (Plus) and flat unlimited-seat (Pro Unlimited) — plus storage overage and add-on subscriptions. No per-API-call billing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: 37signals, LLC
  PricingCategory: Subscription
  PricingUnit: seat-month
  ProviderName: Basecamp
  PublisherName: 37signals, LLC
  ServiceCategory: Collaboration / Project Management SaaS
  ServiceName: Basecamp
layout: finops
meters:
- aggregation: sum
  description: Per-user monthly subscription on the Plus plan (employees only; guests free)
  dimensions:
  - account
  - plan
  - billing_period
  name: seat_subscription
  unit: seat-month
- aggregation: sum
  description: Flat monthly subscription on the Pro Unlimited plan
  dimensions:
  - account
  - billing_cycle
  name: flat_subscription
  unit: month
- aggregation: max
  description: Storage included in the plan ceiling (Plus 500 GB, Pro Unlimited 5 TB)
  dimensions:
  - account
  - plan
  name: storage_included
  unit: GB-month
- aggregation: sum
  description: Additional storage purchased above the plan ceiling
  dimensions:
  - account
  name: storage_overage
  unit: TB-month
- aggregation: sum
  description: Timesheet add-on flat monthly fee (Plus only; included with Pro Unlimited)
  dimensions:
  - account
  name: addon_timesheet
  unit: month
- aggregation: sum
  description: Admin Pro Pack add-on flat monthly fee (Plus only; included with Pro Unlimited)
  dimensions:
  - account
  name: addon_admin_pro_pack
  unit: month
name: Basecamp Finops
provider_name: Basecamp
provider_slug: basecamp
publisher_name: 37signals, LLC
service_category: Collaboration / Project Management SaaS
slug: basecamp-finops
source_filename: basecamp-finops.yml
source_heading: FinOps Profile
source_url: https://basecamp.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Basecamp\nproviderId: basecamp\npublisherName: 37signals, LLC\nserviceCategory: Collaboration / Project Management SaaS\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Collaboration\n  - Project Management\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Basecamp: tiered SaaS subscription with two billing shapes —\n  per-user (Plus) and flat unlimited-seat (Pro Unlimited) — plus storage overage and add-on subscriptions.\n  No per-API-call billing.'\nsources:\n  - https://basecamp.com/pricing\n  - https://github.com/basecamp/bc3-api\nprinciples:\n  - name: Visibility\n    description: 37signals invoices and receipts surface seat counts,\
  \ storage usage, and add-on charges\n      in the Basecamp account billing portal. There is no usage API; reconciliation relies on the monthly\n      invoice line items.\n  - name: Allocation\n    description: Allocate spend by Basecamp account; cost can be split across teams via project-level\n      attribution outside Basecamp (the API exposes project membership for chargeback modeling).\n  - name: Optimization\n    description: Compare Plus per-user math vs Pro Unlimited flat fee — Pro Unlimited becomes cheaper\n      around 20+ active employee seats. Use annual billing on Pro Unlimited ($299/mo vs $349/mo monthly)\n      and prune storage to avoid $50/TB overage.\n  - name: Accountability\n    description: Account owner is the billing contact; assign an internal Basecamp budget owner to review\n      seat counts quarterly and remove inactive employees before each billing cycle.\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n\
  \  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Basecamp\n  ServiceCategory: Collaboration / Project Management SaaS\n  ProviderName: Basecamp\n  PublisherName: 37signals, LLC\n  InvoiceIssuerName: 37signals, LLC\n  PricingCategory: Subscription\n  PricingUnit: seat-month\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: seat_subscription\n    description: Per-user monthly subscription on the Plus plan (employees only; guests free)\n    unit: seat-month\n    aggregation: sum\n    dimensions:\n      - account\n      - plan\n      - billing_period\n  - name: flat_subscription\n    description: Flat monthly subscription on the Pro Unlimited plan\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n      - billing_cycle\n  - name: storage_included\n    description: Storage included in the plan ceiling (Plus 500 GB, Pro Unlimited\
  \ 5 TB)\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - account\n      - plan\n  - name: storage_overage\n    description: Additional storage purchased above the plan ceiling\n    unit: TB-month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: addon_timesheet\n    description: Timesheet add-on flat monthly fee (Plus only; included with Pro Unlimited)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: addon_admin_pro_pack\n    description: Admin Pro Pack add-on flat monthly fee (Plus only; included with Pro Unlimited)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\napis:\n  - name: Basecamp API\n    baseURL: https://3.basecampapi.com\n    tags:\n      - Collaboration\n      - Project Management\n      - REST\n      - Team Communication\n    serviceName: Basecamp API\n    serviceCategory: API\n  - name: Basecamp Webhooks\n    baseURL: https://3.basecampapi.com\n    tags:\n      - Events\n   \
  \   - Notifications\n      - Project Management\n      - Webhooks\n    serviceName: Basecamp Webhooks\n    serviceCategory: API\n  - name: Basecamp OAuth\n    baseURL: https://launchpad.37signals.com\n    tags:\n      - Authentication\n      - Authorization\n      - OAuth\n      - Security\n    serviceName: Basecamp OAuth\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Active Seat\n    metric: billed_cost / active_seats\n    target: '<= $15/seat/month on Plus; switch to Pro Unlimited above ~20 seats'\n  - name: Storage Cost Ratio\n    metric: storage_overage_cost / total_billed\n    target: minimize via retention policies\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/basecamp/refs/heads/main/finops/basecamp-finops.yml
sources:
- https://basecamp.com/pricing
- https://github.com/basecamp/bc3-api
specification: FinOps Framework
tags:
- Collaboration
- Project Management
- SaaS
- FinOps
- FOCUS
---
