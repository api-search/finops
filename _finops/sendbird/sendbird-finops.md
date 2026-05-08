---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sendbird-platform-openapi.yml
  format: yaml
  label: Sendbird Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sendbird/refs/heads/main/openapi/sendbird-platform-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps shape for Sendbird — MAU-tiered subscription with included message allowances and add-on products. The dominant cost driver is the MAU tier purchased; secondary drivers are peak concurrent connections (capped at 5% of MAU on Starter/Pro), Business Messaging volume, and Enterprise add-ons. Annual billing carries a discount over monthly.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Sendbird, Inc.
  ProviderName: Sendbird
  PublisherName: Sendbird, Inc.
  ServiceCategory: Communications PaaS
  ServiceName: Sendbird
layout: finops
meters:
- aggregation: max
  description: Monthly Active Users — primary tier-pricing meter
  dimensions:
  - application
  - plan
  name: mau
  unit: mau
- aggregation: max
  description: Peak concurrent WebSocket connections in the billing period (capped at 5% of MAU on Starter/Pro)
  dimensions:
  - application
  name: peak_connections
  unit: connection
- aggregation: sum
  description: In-app Business Messaging messages sent (30K included on Starter/Pro)
  dimensions:
  - application
  - channel
  name: business_messages
  unit: message
- aggregation: sum
  description: Recurring monthly plan fee (Starter, Pro at MAU tier; Enterprise custom)
  dimensions:
  - plan
  - billing_term
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Enterprise add-on products (e.g., dedicated server, advanced moderation)
  dimensions:
  - addon
  name: addon_fees
  unit: addon
name: Sendbird Finops
provider_name: Sendbird
provider_slug: sendbird
publisher_name: Sendbird, Inc.
service_category: Communications PaaS
slug: sendbird-finops
source_filename: sendbird-finops.yml
source_heading: FinOps Profile
source_url: https://sendbird.com/pricing/chat
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Sendbird\nproviderId: sendbird\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Chat\n  - Messaging\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Sendbird — MAU-tiered subscription with included message\n  allowances and add-on products. The dominant cost driver is the MAU tier purchased; secondary drivers\n  are peak concurrent connections (capped at 5% of MAU on Starter/Pro), Business Messaging volume, and\n  Enterprise add-ons. Annual billing carries a discount over monthly.\nsources:\n  - https://sendbird.com/pricing/chat\n  - https://sendbird.com/docs/chat/platform-api/v3/error-codes/rate-limits\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Sendbird, Inc.\nserviceCategory: Communications PaaS\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: Sendbird\n  ServiceCategory: Communications PaaS\n  ProviderName: Sendbird\n  PublisherName: Sendbird, Inc.\n  InvoiceIssuerName: Sendbird, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: mau\n    description: Monthly Active Users — primary tier-pricing meter\n    unit: mau\n    aggregation: max\n    dimensions:\n      - application\n      - plan\n  - name: peak_connections\n    description: Peak concurrent WebSocket connections in the billing period (capped at 5% of MAU on\n      Starter/Pro)\n    unit: connection\n    aggregation: max\n    dimensions:\n      - application\n  - name: business_messages\n    description: In-app Business Messaging messages sent (30K included on Starter/Pro)\n    unit: message\n    aggregation: sum\n \
  \   dimensions:\n      - application\n      - channel\n  - name: subscription_fee\n    description: Recurring monthly plan fee (Starter, Pro at MAU tier; Enterprise custom)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_term\n  - name: addon_fees\n    description: Enterprise add-on products (e.g., dedicated server, advanced moderation)\n    unit: addon\n    aggregation: sum\n    dimensions:\n      - addon\nprinciples:\n  - name: Visibility\n    description: Use the Sendbird Dashboard's MAU and peak-connection charts plus the Platform API's\n      usage endpoints to track tier headroom in real time. Watch for stricter-endpoint throttling (5/sec\n      cap) as a leading indicator of write-heavy workloads.\n  - name: Allocation\n    description: A Sendbird application is the natural allocation unit — split apps per product or environment\n      so MAU and message volume map cleanly to teams. Enterprise add-ons are line-item allocated to the\n      requesting\
  \ product.\n  - name: Optimization\n    description: Stay just under the next MAU tier (5K/10K/25K) to avoid step-function price jumps; prefer\n      annual billing for ~12% savings over monthly. Batch user updates and channel creation to respect\n      the 5/sec stricter-endpoint cap.\n  - name: Accountability\n    description: Product engineering owns MAU growth and Platform API hygiene; finance owns the annual\n      vs monthly billing decision and Enterprise renewal negotiation.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sendbird/refs/heads/main/finops/sendbird-finops.yml
sources:
- https://sendbird.com/pricing/chat
- https://sendbird.com/docs/chat/platform-api/v3/error-codes/rate-limits
specification: FinOps Framework
tags:
- Chat
- Messaging
- FinOps
- FOCUS
---
