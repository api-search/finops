---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swetrix-events-api-openapi.yml
  format: yaml
  label: Swetrix Events API
  slug: swetrix-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/swetrix/refs/heads/main/openapi/swetrix-events-api-openapi.yml
- filename: swetrix-statistics-api-openapi.yml
  format: yaml
  label: Swetrix Statistics API
  slug: swetrix-statistics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/swetrix/refs/heads/main/openapi/swetrix-statistics-api-openapi.yml
- filename: swetrix-admin-api-openapi.yml
  format: yaml
  label: Swetrix Admin API
  slug: swetrix-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/swetrix/refs/heads/main/openapi/swetrix-admin-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps definition for Swetrix. Pricing is a pure tiered subscription differentiated by the included monthly event quota (10 published tiers from 100k to 20M events plus a Custom tier). All tiers ship the same feature set, so the only variable cost driver is monthly event volume.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Swetrix Ltd.
  ProviderName: Swetrix
  PublisherName: Swetrix Ltd.
  ServiceCategory: Web Analytics
  ServiceName: Swetrix
layout: finops
meters:
- aggregation: sum
  description: Monthly or annual base plan fee, tier determined by included monthly event quota
  dimensions:
  - plan
  name: base_subscription
  unit: month
- aggregation: sum
  description: Tracked analytics events ingested per month (counted against plan quota)
  dimensions:
  - project
  - event_type
  name: monthly_events
  unit: event
- aggregation: max
  description: Websites under one account, capped at 50 per account
  dimensions:
  - project
  name: tracked_websites
  unit: website
name: Swetrix Finops
provider_name: Swetrix
provider_slug: swetrix
publisher_name: Swetrix Ltd.
service_category: Web Analytics
slug: swetrix-finops
source_filename: swetrix-finops.yml
source_heading: FinOps Profile
source_url: https://swetrix.com/#pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Swetrix\nproviderId: swetrix\npublisherName: Swetrix Ltd.\nserviceCategory: Web Analytics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Web Analytics\ndescription: FOCUS-aligned FinOps definition for Swetrix. Pricing is a pure tiered subscription differentiated\n  by the included monthly event quota (10 published tiers from 100k to 20M events plus a Custom tier).\n  All tiers ship the same feature set, so the only variable cost driver is monthly event volume.\nsources:\n  - https://swetrix.com/#pricing\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\
  \ or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Swetrix\n  ServiceCategory: Web Analytics\n  ProviderName: Swetrix\n  PublisherName: Swetrix Ltd.\n  InvoiceIssuerName: Swetrix Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: base_subscription\n    description: Monthly or annual base plan fee, tier determined by included monthly event quota\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: monthly_events\n    description: Tracked analytics events ingested per month (counted against plan quota)\n    unit: event\n    aggregation: sum\n    dimensions:\n      - project\n      - event_type\n  - name: tracked_websites\n    description: Websites under one account, capped at 50 per account\n    unit: website\n    aggregation: max\n    dimensions:\n      - project\nprinciples:\n  - name: Visibility\n    description: Use the Swetrix dashboard project\
  \ usage view to track monthly event volume relative\n      to the subscribed plan quota; alert as you approach the next tier threshold.\n  - name: Allocation\n    description: Allocate Swetrix cost to the product or marketing site whose tracked events drive volume;\n      one Swetrix account aggregates up to 50 sites which can be split per business unit.\n  - name: Optimization\n    description: Reduce event volume by sampling high-volume events, disabling tracking on noisy paths,\n      and choosing annual billing for the ~17% discount; right-size to the smallest tier that covers\n      typical monthly volume rather than the peak.\n  - name: Accountability\n    description: Assign a Swetrix account owner per workspace; review monthly event consumption against\n      the subscribed tier and forecast tier upgrades 1-2 months ahead.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/swetrix/refs/heads/main/finops/swetrix-finops.yml
sources:
- https://swetrix.com/#pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Web Analytics
---
