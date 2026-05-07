---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: ford-motor-ford-api-openapi.yml
  format: yaml
  label: Ford Developer API
  slug: ford-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/ford-motor/refs/heads/main/openapi/ford-motor-ford-api-openapi.yml
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
description: FOCUS-aligned FinOps mapping for Ford Motor Company's developer/partner APIs — partner-licensed connected-vehicle access, billed per-VIN subscription plus per-call/event usage.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Ford Motor Company
  ProviderName: Ford Motor Company
  PublisherName: Ford Motor Company
  ServiceCategory: Connected Vehicle / Mobility
  ServiceName: Ford Motor Company Connected Vehicle APIs
layout: finops
meters:
- aggregation: max
  description: Active VIN subscriptions enrolled with the partner application
  dimensions:
  - region
  - vehicle_model
  - data_package
  name: vehicle_subscriptions
  unit: vehicle-month
- aggregation: sum
  description: API requests against connected-vehicle, dealer, and fleet endpoints
  dimensions:
  - api
  - endpoint
  - data_class
  name: api_calls
  unit: request
- aggregation: sum
  description: Webhook/streaming events delivered (telemetry, status, alerts)
  dimensions:
  - event_type
  name: streaming_events
  unit: event
- aggregation: sum
  description: Premium-data add-ons (high-resolution telemetry, historical replay)
  dimensions:
  - data_class
  name: premium_data
  unit: request
name: Ford Motor Finops
provider_name: ford-motor
provider_slug: ford-motor
publisher_name: Ford Motor Company
service_category: Connected Vehicle / Mobility
slug: ford-motor-finops
source_filename: ford-motor-finops.yml
source_heading: FinOps Profile
source_url: https://developer.ford.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Ford Motor Company\nproviderId: ford-motor\npublisherName: Ford Motor Company\nserviceCategory: Connected Vehicle / Mobility\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automobiles\n  - Connected Vehicle\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps mapping for Ford Motor Company's developer/partner APIs — partner-licensed connected-vehicle access, billed per-VIN subscription plus per-call/event usage.\nnotes: No public pricing. Mirrors the ford finops; meters reflect typical OEM connected-vehicle billing patterns.\nsources:\n  - https://developer.ford.com/\n  - https://developer.ford.com/apis\nbillingModel:\n\
  \  pricingCategory: Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Ford Motor Company Connected Vehicle APIs\n  ServiceCategory: Connected Vehicle / Mobility\n  ProviderName: Ford Motor Company\n  PublisherName: Ford Motor Company\n  InvoiceIssuerName: Ford Motor Company\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: vehicle_subscriptions\n    description: Active VIN subscriptions enrolled with the partner application\n    unit: vehicle-month\n    aggregation: max\n    dimensions:\n      - region\n      - vehicle_model\n      - data_package\n  - name: api_calls\n    description: API requests against connected-vehicle, dealer, and fleet endpoints\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - data_class\n  - name: streaming_events\n    description: Webhook/streaming\
  \ events delivered (telemetry, status, alerts)\n    unit: event\n    aggregation: sum\n    dimensions:\n      - event_type\n  - name: premium_data\n    description: Premium-data add-ons (high-resolution telemetry, historical replay)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - data_class\nprinciples:\n  - name: Visibility\n    description: Pull partner-portal usage daily and reconcile against your own logs; track per-VIN consent status to avoid billing for orphaned subscriptions.\n  - name: Allocation\n    description: Tag every request with end-customer, VIN, and use-case for chargeback to downstream product features.\n  - name: Optimization\n    description: Use webhooks/streaming over polling; respect minimum poll intervals; cache static reference data; archive historical data into your own warehouse rather than re-fetching.\n  - name: Accountability\n    description: Connected-vehicle product owner owns the partnership agreement; finance audits VIN subscription\
  \ counts against active consent monthly.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/ford-motor/refs/heads/main/finops/ford-motor-finops.yml
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
