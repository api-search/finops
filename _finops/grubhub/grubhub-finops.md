---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: grubhub-menu-openapi.yml
  format: yaml
  label: Grubhub Menu API
  slug: menu-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/openapi/grubhub-menu-openapi.yml
- filename: grubhub-orders-openapi.yml
  format: yaml
  label: Grubhub Orders API
  slug: orders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/openapi/grubhub-orders-openapi.yml
- filename: grubhub-merchant-data-openapi.yml
  format: yaml
  label: Grubhub Merchant Data API
  slug: merchant-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/openapi/grubhub-merchant-data-openapi.yml
- filename: grubhub-merchant-schedules-openapi.yml
  format: yaml
  label: Grubhub Merchant Schedules API
  slug: merchant-schedules-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/openapi/grubhub-merchant-schedules-openapi.yml
- filename: grubhub-deliveries-openapi.yml
  format: yaml
  label: Grubhub Deliveries API
  slug: deliveries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/openapi/grubhub-deliveries-openapi.yml
- filename: grubhub-onboarding-openapi.yml
  format: yaml
  label: Grubhub Onboarding API
  slug: onboarding-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/openapi/grubhub-onboarding-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Take Rate
description: 'FOCUS-aligned FinOps for Grubhub: revenue model is marketplace commission per restaurant order plus optional Grubhub Connect delivery fees, not per-API-call billing. Partner integration APIs (Menu, Orders, Deliveries, Merchant Data, Schedules, Onboarding) are included with the merchant marketplace agreement. Treat this document as a placeholder pending direct reconciliation with a Grubhub merchant or partner contract.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Grubhub Holdings Inc.
  ProviderName: Grubhub
  PublisherName: Grubhub Holdings Inc.
  ServiceCategory: Food Delivery / Marketplaces
  ServiceName: Grubhub
layout: finops
meters:
- aggregation: sum
  description: Orders routed through the Grubhub Marketplace
  dimensions:
  - restaurant
  - market
  - order_type
  name: marketplace_orders
  unit: order
- aggregation: sum
  description: Gross merchandise value of marketplace orders
  dimensions:
  - restaurant
  - market
  name: marketplace_gmv
  unit: USD
- aggregation: sum
  description: Deliveries fulfilled by the Grubhub courier network (Grubhub Connect)
  dimensions:
  - restaurant
  - market
  name: connect_deliveries
  unit: delivery
- aggregation: sum
  description: Partner integration API calls (operational metric, not directly billed)
  dimensions:
  - api
  - partner
  - restaurant
  name: api_requests
  unit: request
- aggregation: sum
  description: Outbound order / delivery / merchant webhook events
  dimensions:
  - event_type
  - restaurant
  name: webhook_events
  unit: event
name: Grubhub Finops
provider_name: grubhub
provider_slug: grubhub
publisher_name: Grubhub Holdings Inc.
service_category: Food Delivery / Marketplaces
slug: grubhub-finops
source_filename: grubhub-finops.yml
source_heading: FinOps Profile
source_url: https://developer.grubhub.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Grubhub\nproviderId: grubhub\npublisherName: Grubhub Holdings Inc.\nserviceCategory: Food Delivery / Marketplaces\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Food Delivery\n  - Marketplaces\n  - Restaurants\ndescription: 'FOCUS-aligned FinOps for Grubhub: revenue model is marketplace commission per\n  restaurant order plus optional Grubhub Connect delivery fees, not per-API-call billing. Partner\n  integration APIs (Menu, Orders, Deliveries, Merchant Data, Schedules, Onboarding) are included\n  with the merchant marketplace agreement. Treat this document as a placeholder pending direct\n  reconciliation\
  \ with a Grubhub merchant or partner contract.'\nnotes: No public per-call API price book. Cost flows through restaurant-marketplace commissions\n  and optional service fees. Reconcile against signed merchant or partner contract.\nsources:\n  - https://developer.grubhub.com\n  - https://www.grubhub.com/restaurant\nbillingModel:\n  pricingCategory: Take Rate\n  billingFrequency: Continuous Settlement\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Grubhub\n  ServiceCategory: Food Delivery / Marketplaces\n  ProviderName: Grubhub\n  PublisherName: Grubhub Holdings Inc.\n  InvoiceIssuerName: Grubhub Holdings Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: marketplace_orders\n    description: Orders routed through the Grubhub Marketplace\n    unit: order\n    aggregation: sum\n    dimensions:\n      - restaurant\n      - market\n      - order_type\n  - name: marketplace_gmv\n \
  \   description: Gross merchandise value of marketplace orders\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - restaurant\n      - market\n  - name: connect_deliveries\n    description: Deliveries fulfilled by the Grubhub courier network (Grubhub Connect)\n    unit: delivery\n    aggregation: sum\n    dimensions:\n      - restaurant\n      - market\n  - name: api_requests\n    description: Partner integration API calls (operational metric, not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - partner\n      - restaurant\n  - name: webhook_events\n    description: Outbound order / delivery / merchant webhook events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - event_type\n      - restaurant\nprinciples:\n  - name: Visibility\n    description: Use the Grubhub merchant portal / payouts reporting and partner dashboards to\n      reconcile commission, delivery, and refund line items per restaurant.\n  - name: Allocation\n\
  \    description: Tag restaurants / locations with brand / region / franchisee so commission and\n      Connect-delivery costs allocate to the correct P&L.\n  - name: Optimization\n    description: Negotiate commission rates at scale; tune which markets use Connect vs\n      restaurant-fulfilled delivery; use the Schedules API to avoid orders during overload.\n  - name: Accountability\n    description: Designate a partnerships / merchant-ops owner accountable for the Grubhub\n      contract, monthly payout reconciliation, and dispute / refund handling.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/grubhub/refs/heads/main/finops/grubhub-finops.yml
sources:
- https://developer.grubhub.com
- https://www.grubhub.com/restaurant
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Food Delivery
- Marketplaces
- Restaurants
---
