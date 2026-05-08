---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: v1
  format: yaml
  label: Power Apps API
  slug: ''
  spec_type: OpenAPI
  url: https://api.powerapps.com/openapi/v1
- filename: v1
  format: yaml
  label: Power Automate API
  slug: ''
  spec_type: OpenAPI
  url: https://api.flow.microsoft.com/openapi/v1
- filename: swagger.json
  format: json
  label: Power BI REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.powerbi.com/v1.0/myorg/swagger.json
- filename: power-platform-api-openapi.json
  format: json
  label: Power Platform Unified API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/power-platform/refs/heads/main/openapi/power-platform-api-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Annual (per-user/per-bot) and Monthly (PAYG and Copilot Credits)
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Per-Bot + Pay-As-You-Go + Tenant Add-Ons
description: 'FOCUS-aligned FinOps for Microsoft Power Platform: layered model combining per-user subscriptions (Power Apps Premium $20, Power Automate Premium $15), per-bot subscriptions (Process $150, Hosted Process $215), tenant-level add-ons (Process Mining $5,000, Dataverse storage $40/GB/month), pre-paid Copilot Credits ($200 per 25,000), and pay-as-you-go overage for Power Apps. The unifying meter is Power Platform Requests (PPR), entitled per license on a 24-hour sliding window. Add-on capacity packs raise target identities by 50k PPR/day each and are stackable.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  PricingUnit: seat-month / bot-month / GB-month / 25k-credits
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Business Applications
  ServiceName: Microsoft Power Platform
  ServiceSubcategory: Low-Code Platform
layout: finops
meters:
- aggregation: max
  description: Per-user Power Apps Premium subscriptions.
  dimensions:
  - tenant
  - department
  name: power_apps_premium_seats
  unit: seat-month
- aggregation: max
  description: Per-user Power Automate Premium subscriptions.
  dimensions:
  - tenant
  - department
  name: power_automate_premium_seats
  unit: seat-month
- aggregation: max
  description: Per-bot Process and Hosted Process subscriptions for unattended desktop flows.
  dimensions:
  - flow_id
  - environment
  - hosted
  name: process_bots
  unit: bot-month
- aggregation: sum
  description: Daily request entitlement consumed per user (Premium) or per flow (Process), evaluated on a 24-hour sliding window.
  dimensions:
  - environment
  - caller_id
  - caller_type
  - resource_type
  - license
  name: power_platform_requests
  unit: request
- aggregation: sum
  description: Microsoft Copilot Studio Credits consumed by custom copilots.
  dimensions:
  - copilot
  - tenant
  - environment
  name: copilot_credits
  unit: credit
- aggregation: max
  description: Dataverse database, file, and log storage at the tenant level.
  dimensions:
  - environment
  - storage_type
  name: dataverse_storage
  unit: GB-month
- aggregation: max
  description: Process Mining add-on storage capacity.
  dimensions:
  - tenant
  name: process_mining_storage
  unit: GB-month
- aggregation: sum
  description: Pay-as-you-go cloud-flow actions billed when daily PPR limits are exceeded.
  dimensions:
  - environment
  - flow_id
  name: payg_actions
  unit: action
name: Power Platform Finops
provider_name: Microsoft Power Platform APIs
provider_slug: power-platform
publisher_name: Microsoft Corporation
service_category: Business Applications
slug: power-platform-finops
source_filename: power-platform-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/power-platform/products/power-apps/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Power Platform APIs\nproviderId: power-platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Business Applications\n  - Copilot Studio\n  - Dataverse\n  - Low-Code\n  - Microsoft\n  - Power Apps\n  - Power Automate\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Microsoft Power Platform: layered model combining\n  per-user subscriptions (Power Apps Premium $20, Power Automate Premium $15),\n  per-bot subscriptions (Process $150, Hosted Process $215), tenant-level\n  add-ons (Process Mining $5,000, Dataverse storage $40/GB/month), pre-paid\n  Copilot Credits ($200 per 25,000), and pay-as-you-go overage for Power Apps.\n  The unifying meter is Power Platform Requests (PPR), entitled per license\n  on a 24-hour sliding window. Add-on capacity packs raise target identities\n  by 50k PPR/day each and are\
  \ stackable.\nsources:\n  - https://www.microsoft.com/en-us/power-platform/products/power-apps/pricing\n  - https://www.microsoft.com/en-us/power-platform/products/power-automate/pricing\n  - https://learn.microsoft.com/en-us/power-platform/admin/api-request-limits-allocations\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Business Applications\nbillingModel:\n  pricingCategory: Subscription + Per-Bot + Pay-As-You-Go + Tenant Add-Ons\n  billingFrequency: Annual (per-user/per-bot) and Monthly (PAYG and Copilot Credits)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Power Platform\n  ServiceCategory: Business Applications\n  ServiceSubcategory: Low-Code Platform\n\
  \  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: seat-month / bot-month / GB-month / 25k-credits\nmeters:\n  - name: power_apps_premium_seats\n    description: Per-user Power Apps Premium subscriptions.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - department\n  - name: power_automate_premium_seats\n    description: Per-user Power Automate Premium subscriptions.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - tenant\n      - department\n  - name: process_bots\n    description: Per-bot Process and Hosted Process subscriptions for unattended desktop flows.\n    unit: bot-month\n    aggregation: max\n    dimensions:\n      - flow_id\n      - environment\n      - hosted\n  - name: power_platform_requests\n    description: Daily request entitlement consumed per user (Premium) or per flow (Process), evaluated\
  \ on a 24-hour sliding window.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - environment\n      - caller_id\n      - caller_type\n      - resource_type\n      - license\n  - name: copilot_credits\n    description: Microsoft Copilot Studio Credits consumed by custom copilots.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - copilot\n      - tenant\n      - environment\n  - name: dataverse_storage\n    description: Dataverse database, file, and log storage at the tenant level.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - environment\n      - storage_type\n  - name: process_mining_storage\n    description: Process Mining add-on storage capacity.\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - tenant\n  - name: payg_actions\n    description: Pay-as-you-go cloud-flow actions billed when daily PPR limits are exceeded.\n    unit: action\n    aggregation: sum\n    dimensions:\n      - environment\n      - flow_id\n\
  principles:\n  - name: Visibility\n    description: Use the Power Platform admin center capacity reports (Licensed user, Non-licensed user, Per-flow) to track Power Platform Requests against entitlement; Microsoft 365 admin center surfaces seat consumption.\n  - name: Allocation\n    description: Tag environments by business unit and assign capacity reports per-environment; the per-flow report attributes Process-license consumption to a specific flow_id for chargeback to the flow's owning team.\n  - name: Optimization\n    description: Right-size license mix between Premium (per-user) and Process (per-flow); stack Process licenses on a single high-volume flow rather than over-licensing users; switch to Power Apps pay-as-you-go for spiky workloads to avoid throttling; cache and de-duplicate connector calls inside flows.\n  - name: Accountability\n    description: Environment admins are accountable for PPR consumption in their environments; Power Automate flow owners are accountable for\
  \ the 24-hour and 5-minute (100k) ceilings; tenant admins purchase capacity add-ons and review per-flow reports before transition-period enforcement begins.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/power-platform/refs/heads/main/finops/power-platform-finops.yml
sources:
- https://www.microsoft.com/en-us/power-platform/products/power-apps/pricing
- https://www.microsoft.com/en-us/power-platform/products/power-automate/pricing
- https://learn.microsoft.com/en-us/power-platform/admin/api-request-limits-allocations
specification: FinOps Framework
tags:
- Business Applications
- Copilot Studio
- Dataverse
- Low-Code
- Microsoft
- Power Apps
- Power Automate
- FinOps
- FOCUS
---
