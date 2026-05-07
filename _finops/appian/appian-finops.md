---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps view for Appian: per-user / per-app / per-month subscription priced by named edition (Standard / Advanced / Premium). Primary cost drivers are user seats, app count, and AI Actions consumption (200K/500K/1M monthly cap by edition). RPA bot count and data-source row counts are tier-included rather than separately metered.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Appian Corporation
  PricingCategory: Tiered Subscription
  ProviderName: Appian
  PublisherName: Appian Corporation
  ServiceCategory: Low-Code / Process Automation
  ServiceName: Appian Platform
layout: finops
meters:
- aggregation: max
  description: Active named users on the Appian platform per month
  dimensions:
  - edition
  - app
  name: user_seats
  unit: seat
- aggregation: max
  description: Distinct apps in scope of the per-user-per-app subscription
  dimensions:
  - edition
  - environment
  name: applications
  unit: app
- aggregation: sum
  description: AI Actions consumed against the monthly tier allotment (Copilot, Agent Studio, DocCenter)
  dimensions:
  - edition
  - feature
  name: ai_actions
  unit: action
- aggregation: sum
  description: RPA bot executions against the bot allotment
  dimensions:
  - bot
  - environment
  name: rpa_bot_runs
  unit: bot-run
- aggregation: sum
  description: Portal end-user sessions for cost attribution where portals are the primary surface
  dimensions:
  - portal
  - app
  name: portal_traffic
  unit: session
name: Appian Finops
provider_name: Appian
provider_slug: appian
publisher_name: Appian Corporation
service_category: Low-Code / Process Automation
slug: appian-finops
source_filename: appian-finops.yml
source_heading: FinOps Profile
source_url: https://appian.com/products/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Appian\nproviderId: appian\npublisherName: Appian Corporation\nserviceCategory: Low-Code / Process Automation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Low Code\n  - Process Automation\n  - RPA\ndescription: 'FOCUS-aligned FinOps view for Appian: per-user / per-app / per-month subscription priced\n  by named edition (Standard / Advanced / Premium). Primary cost drivers are user seats, app count, and\n  AI Actions consumption (200K/500K/1M monthly cap by edition). RPA bot count and data-source row counts\n  are tier-included rather than separately metered.'\nsources:\n  - https://appian.com/products/pricing\n\
  billingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Appian Platform\n  ServiceCategory: Low-Code / Process Automation\n  ProviderName: Appian\n  PublisherName: Appian Corporation\n  InvoiceIssuerName: Appian Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Tiered Subscription\nmeters:\n  - name: user_seats\n    description: Active named users on the Appian platform per month\n    unit: seat\n    aggregation: max\n    dimensions:\n      - edition\n      - app\n  - name: applications\n    description: Distinct apps in scope of the per-user-per-app subscription\n    unit: app\n    aggregation: max\n    dimensions:\n      - edition\n      - environment\n  - name: ai_actions\n    description: AI Actions consumed against the monthly tier allotment (Copilot, Agent Studio, DocCenter)\n    unit: action\n    aggregation:\
  \ sum\n    dimensions:\n      - edition\n      - feature\n  - name: rpa_bot_runs\n    description: RPA bot executions against the bot allotment\n    unit: bot-run\n    aggregation: sum\n    dimensions:\n      - bot\n      - environment\n  - name: portal_traffic\n    description: Portal end-user sessions for cost attribution where portals are the primary surface\n    unit: session\n    aggregation: sum\n    dimensions:\n      - portal\n      - app\nprinciples:\n  - name: Visibility\n    description: Use Appian's License Center, Process HQ, and AI usage dashboards to track seat utilization,\n      AI Action burn-rate, and RPA bot runs.\n  - name: Allocation\n    description: Tag apps and processes with business-unit metadata; allocate per-user-per-app cost back\n      to consuming product owners.\n  - name: Optimization\n    description: Right-size editions per app (Standard for transactional apps without AI; Advanced/Premium\n      where AI features are exercised); reclaim inactive seats;\
  \ sample AI Actions during prototyping;\n      consolidate small apps to share data sources.\n  - name: Accountability\n    description: Center of Excellence (COE) owns the Appian contract; product owners accountable for app-level\n      seat count, AI Action consumption, and RPA bot ROI.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appian/refs/heads/main/finops/appian-finops.yml
sources:
- https://appian.com/products/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Low Code
- Process Automation
- RPA
---
