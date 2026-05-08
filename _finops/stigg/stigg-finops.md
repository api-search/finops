---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stigg-openapi.yml
  format: yaml
  label: Stigg GraphQL API
  slug: stigg-graphql
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stigg/refs/heads/main/openapi/stigg-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Usage-Based Add-Ons
description: FOCUS-aligned FinOps definition for Stigg. Stigg is itself a pricing/entitlement platform billed as a tiered SaaS subscription (Sandbox / Growth / Scale) plus per-seat and per-subscription metered charges and per-GB event metering.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Stigg Ltd.
  ProviderName: Stigg
  PublisherName: Stigg Ltd.
  ServiceCategory: Pricing & Entitlements Platform
  ServiceName: Stigg
layout: finops
meters:
- aggregation: sum
  description: Monthly or annual base platform fee for the Growth or Scale plan
  dimensions:
  - plan
  name: base_subscription
  unit: month
- aggregation: max
  description: Active team-member seats charged per month
  dimensions:
  - role
  name: seats
  unit: seat
- aggregation: count
  description: Self-service subscriptions managed in Stigg billed at $0.32 each
  dimensions:
  - plan
  - product
  name: self_service_subscriptions
  unit: subscription
- aggregation: count
  description: Custom (wire/ACH) subscriptions billed at $4.70 each
  dimensions:
  - plan
  - product
  name: custom_subscriptions
  unit: subscription
- aggregation: sum
  description: Advanced event metering data processed/stored, billed per GB per month
  dimensions:
  - feature
  - environment
  name: event_metering_volume
  unit: GB
- aggregation: sum
  description: Optional per-integration add-on charges (Slack support, AWS Marketplace, Snowflake, BigQuery, Salesforce native)
  dimensions:
  - integration
  name: integration_addons
  unit: month
name: Stigg Finops
provider_name: Stigg
provider_slug: stigg
publisher_name: Stigg Ltd.
service_category: Pricing & Entitlements Platform
slug: stigg-finops
source_filename: stigg-finops.yml
source_heading: FinOps Profile
source_url: https://www.stigg.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Stigg\nproviderId: stigg\npublisherName: Stigg Ltd.\nserviceCategory: Pricing & Entitlements Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Pricing\n  - Billing\n  - Entitlements\n  - Usage-Based Billing\n  - SaaS\ndescription: FOCUS-aligned FinOps definition for Stigg. Stigg is itself a pricing/entitlement platform\n  billed as a tiered SaaS subscription (Sandbox / Growth / Scale) plus per-seat and per-subscription metered\n  charges and per-GB event metering.\nsources:\n  - https://www.stigg.io/pricing\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage-Based Add-Ons\n  billingFrequency:\
  \ Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Stigg\n  ServiceCategory: Pricing & Entitlements Platform\n  ProviderName: Stigg\n  PublisherName: Stigg Ltd.\n  InvoiceIssuerName: Stigg Ltd.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: base_subscription\n    description: Monthly or annual base platform fee for the Growth or Scale plan\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n  - name: seats\n    description: Active team-member seats charged per month\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n  - name: self_service_subscriptions\n    description: Self-service subscriptions managed in Stigg billed at $0.32 each\n    unit: subscription\n    aggregation: count\n    dimensions:\n      - plan\n      - product\n  - name: custom_subscriptions\n    description: Custom (wire/ACH) subscriptions billed\
  \ at $4.70 each\n    unit: subscription\n    aggregation: count\n    dimensions:\n      - plan\n      - product\n  - name: event_metering_volume\n    description: Advanced event metering data processed/stored, billed per GB per month\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - feature\n      - environment\n  - name: integration_addons\n    description: Optional per-integration add-on charges (Slack support, AWS Marketplace, Snowflake,\n      BigQuery, Salesforce native)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - integration\nprinciples:\n  - name: Visibility\n    description: Use the Stigg admin console and customer-portal usage views, plus the Stripe/Zuora\n      integration export, to surface subscription counts, seats, and event-metering GB to product/finance.\n  - name: Allocation\n    description: Tag subscriptions with environment (Sandbox vs Production) and product to attribute\n      Stigg cost to the customer-facing product line that drives\
  \ subscription volume.\n  - name: Optimization\n    description: Levers include consolidating non-production environments under Sandbox, choosing annual\n      billing for the 20% discount, batching event ingestion to reduce GB-month, and avoiding wire/ACH\n      subscription type ($4.70) where self-service ($0.32) is acceptable.\n  - name: Accountability\n    description: Designate a Stigg admin per workspace; route invoices to the platform-engineering or\n      monetization owner; review subscription growth and event GB monthly against the Growth plan budget.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stigg/refs/heads/main/finops/stigg-finops.yml
sources:
- https://www.stigg.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Pricing
- Billing
- Entitlements
- Usage-Based Billing
- SaaS
---
