---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Usage
description: FOCUS-aligned FinOps mapping for Ford's Developer Marketplace — partner-licensed connected-vehicle APIs typically billed on a per-vehicle subscription plus per-call usage basis under a partnership agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ford Motor Company
  ProviderName: Ford Motor Company
  PublisherName: Ford Motor Company
  ServiceCategory: Connected Vehicle / Mobility
  ServiceName: Ford Developer Marketplace
layout: finops
meters:
- aggregation: max
  description: Active connected-vehicle (VIN) subscriptions enrolled with the partner application
  dimensions:
  - region
  - vehicle_model
  - data_package
  name: vehicle_subscriptions
  unit: vehicle-month
- aggregation: sum
  description: API requests against vehicle, location, telemetry, or dealer endpoints
  dimensions:
  - api
  - endpoint
  - data_class
  name: api_calls
  unit: request
- aggregation: sum
  description: Webhook / streaming events delivered (telemetry, status changes, alerts)
  dimensions:
  - event_type
  - vehicle_model
  name: streaming_events
  unit: event
- aggregation: sum
  description: Premium-data add-ons (high-resolution telemetry, historical replay, OBD-II extended PIDs)
  dimensions:
  - data_class
  name: premium_data
  unit: request
name: Ford Finops
provider_name: Ford
provider_slug: ford
publisher_name: Ford Motor Company
service_category: Connected Vehicle / Mobility
slug: ford-finops
source_filename: ford-finops.yml
source_heading: FinOps Profile
source_url: https://developer.ford.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ford\nproviderId: ford\npublisherName: Ford Motor Company\nserviceCategory: Connected Vehicle / Mobility\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automobiles\n  - Connected Vehicle\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for Ford's Developer Marketplace — partner-licensed connected-vehicle APIs typically billed on a per-vehicle subscription plus per-call usage basis under a partnership agreement.\nnotes: No public pricing. Meters reflect typical connected-vehicle/OEM API invoicing patterns (per-VIN subscription, per-call fees, premium-data add-ons).\nsources:\n  - https://developer.ford.com/\n\
  \  - https://developer.ford.com/apis\nbillingModel:\n  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Ford Developer Marketplace\n  ServiceCategory: Connected Vehicle / Mobility\n  ProviderName: Ford Motor Company\n  PublisherName: Ford Motor Company\n  InvoiceIssuerName: Ford Motor Company\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: vehicle_subscriptions\n    description: Active connected-vehicle (VIN) subscriptions enrolled with the partner application\n    unit: vehicle-month\n    aggregation: max\n    dimensions:\n      - region\n      - vehicle_model\n      - data_package\n  - name: api_calls\n    description: API requests against vehicle, location, telemetry, or dealer endpoints\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - data_class\n  -\
  \ name: streaming_events\n    description: Webhook / streaming events delivered (telemetry, status changes, alerts)\n    unit: event\n    aggregation: sum\n    dimensions:\n      - event_type\n      - vehicle_model\n  - name: premium_data\n    description: Premium-data add-ons (high-resolution telemetry, historical replay, OBD-II extended PIDs)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - data_class\nprinciples:\n  - name: Visibility\n    description: Pull partner-portal usage reports daily and reconcile against your own request logs to catch billable polling against vehicles whose owners have revoked consent.\n  - name: Allocation\n    description: Tag every request with end-customer/account, VIN, and use-case so spend is allocable to the downstream product feature.\n  - name: Optimization\n    description: Replace polling with webhooks/streaming where Ford supports it; respect minimum poll intervals to avoid wasted billable calls and TCU wake-ups; cache static data\
  \ (VIN-decode, model trims).\n  - name: Accountability\n    description: Connected-vehicle product owner owns the partnership agreement; finance audits per-VIN subscription counts against active consent records monthly.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ford/refs/heads/main/finops/ford-finops.yml
sources:
- https://developer.ford.com/
- https://developer.ford.com/apis
specification: FinOps Framework
tags:
- Automobiles
- Connected Vehicle
- FinOps
- FOCUS
---
