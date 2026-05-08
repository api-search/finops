---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ably-platform-api-openapi.yml
  format: yaml
  label: Ably Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ably/refs/heads/main/openapi/ably-platform-api-openapi.yml
- filename: ably-control-api-openapi.yml
  format: yaml
  label: Ably Control API
  slug: control-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ably/refs/heads/main/openapi/ably-control-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Subscription + Usage
description: FinOps view of Ably. Subscription plus usage-based billing. Cost lines are flat-fee plan tier, per-million messages, per-million connection / channel minutes, and any push-notification add-on. Volume discounts apply at higher commitment levels.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Ably
  ProviderName: Ably
  PublisherName: Ably Realtime
  ServiceCategory: Realtime Infrastructure
  ServiceName: Ably Platform API
layout: finops
meters:
- aggregation: sum
  description: Monthly plan-tier subscription.
  dimensions:
  - account
  name: subscription
  unit: month
- aggregation: sum
  description: Messages above included allowance, $2.50 per million.
  dimensions:
  - account
  - app
  name: messages
  unit: million_messages
- aggregation: sum
  description: Connection or channel minutes above allowance, $1.00 per million.
  dimensions:
  - account
  - app
  name: connection_minutes
  unit: million_minutes
name: Ably Finops
provider_name: Ably
provider_slug: ably
publisher_name: Ably Realtime
service_category: Realtime Infrastructure
slug: ably-finops
source_filename: ably-finops.yml
source_heading: FinOps Profile
source_url: https://ably.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Ably\nproviderId: ably\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Realtime\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Ably. Subscription plus usage-based billing. Cost lines are flat-fee plan tier,\n  per-million messages, per-million connection / channel minutes, and any push-notification\n  add-on. Volume discounts apply at higher commitment levels.\nsources:\n  - https://ably.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Ably Realtime\nserviceCategory: Realtime Infrastructure\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Ably Platform API\n  ServiceCategory: Realtime Infrastructure\n  ProviderName: Ably\n  PublisherName: Ably Realtime\n  InvoiceIssuerName: Ably\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly plan-tier subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account\n  - name: messages\n    description: Messages above included allowance, $2.50 per million.\n    unit: million_messages\n    aggregation: sum\n    dimensions:\n      - account\n      - app\n  - name: connection_minutes\n    description: Connection or channel minutes above allowance, $1.00 per million.\n    unit: million_minutes\n    aggregation: sum\n    dimensions:\n      - account\n      - app\nprinciples:\n  - name: Visibility\n    description: Pull Ably stats by app and namespace daily into FinOps store.\n  -\
  \ name: Allocation\n    description: Allocate by app or namespace, mapping to consuming product or feature.\n  - name: Optimization\n    description: Use channel rewinds; batch publishes; close idle connections to reduce minute usage.\n  - name: Accountability\n    description: Assign a billing owner per account; review monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ably/refs/heads/main/finops/ably-finops.yml
sources:
- https://ably.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Realtime
- FinOps
- FOCUS
---
