---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: norfolk-southern-shipment-status-api.yml
  format: yaml
  label: Norfolk Southern Shipment Status API
  slug: shipment-status
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/norfolk-southern/refs/heads/main/openapi/norfolk-southern-shipment-status-api.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None (bundled)
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: Bundled with Freight Relationship
description: 'FOCUS-aligned FinOps for Norfolk Southern: API access is bundled with the underlying freight-rail customer relationship and not invoiced separately. Cost dimensions are operational (integration build, shipment volume) rather than per-call.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Norfolk Southern Corporation (freight invoice; API not separately billed)
  PricingCategory: Bundled
  PricingUnit: request
  ProviderName: Norfolk Southern
  PublisherName: Norfolk Southern Corporation
  ServiceCategory: Freight Rail / Logistics
  ServiceName: Norfolk Southern ApiHub
layout: finops
meters:
- aggregation: sum
  description: Operationally tracked API request count per key (not invoiced)
  dimensions:
  - api
  - api_key
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Shipment Status polls (track to optimize polling cadence)
  dimensions:
  - shipment_id
  name: shipment_status_polls
  unit: poll
- aggregation: sum
  description: Trip Plan lookups
  name: trip_plan_lookups
  unit: lookup
- aggregation: sum
  description: Gate Receipts retrieved
  name: gate_receipts_pulled
  unit: receipt
name: Norfolk Southern Finops
provider_name: Norfolk Southern
provider_slug: norfolk-southern
publisher_name: Norfolk Southern Corporation
service_category: Freight Rail / Logistics
slug: norfolk-southern-finops
source_filename: norfolk-southern-finops.yml
source_heading: FinOps Profile
source_url: https://developer.nscorp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Norfolk Southern\nproviderId: norfolk-southern\npublisherName: Norfolk Southern Corporation\nserviceCategory: Freight Rail / Logistics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Freight\n  - Logistics\n  - Railroad\n  - Shipping\n  - Transportation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Norfolk Southern: API access is bundled with the underlying freight-rail\n  customer relationship and not invoiced separately. Cost dimensions are operational (integration build,\n  shipment volume) rather than per-call.'\nnotes: Norfolk Southern does not invoice API consumers separately\
  \ from their freight relationship.\nsources:\n  - https://developer.nscorp.com/\n  - https://www.nscorp.com/site/customers/\nprinciples:\n  - name: Visibility\n    description: NS does not bill per-call. Track per-API-key request volume and shipment status polling\n      rates internally to ensure the integration scales with shipment volume.\n  - name: Allocation\n    description: Allocate integration cost (engineering time, monitoring) to the consuming logistics\n      app or business unit. Tag NS API keys per-app for usage attribution.\n  - name: Optimization\n    description: Cache shipment status responses; use webhooks where available rather than polling. Batch\n      Trip Plan and Gate Receipts queries by waybill rather than per-shipment to reduce request count.\n  - name: Accountability\n    description: Designate a logistics-IT owner for the NS ApiHub credential and integration health.\n      Reconcile shipment-tracking data quality with NS Customer Service quarterly.\nbillingModel:\n\
  \  pricingCategory: Bundled with Freight Relationship\n  billingFrequency: None (bundled)\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: Norfolk Southern ApiHub\n  ServiceCategory: Freight Rail / Logistics\n  ProviderName: Norfolk Southern\n  PublisherName: Norfolk Southern Corporation\n  InvoiceIssuerName: Norfolk Southern Corporation (freight invoice; API not separately billed)\n  PricingCategory: Bundled\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Operationally tracked API request count per key (not invoiced)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - api_key\n      - endpoint\n  - name: shipment_status_polls\n    description: Shipment Status polls (track to optimize polling cadence)\n    unit: poll\n    aggregation: sum\n    dimensions:\n      - shipment_id\n  - name: trip_plan_lookups\n    description:\
  \ Trip Plan lookups\n    unit: lookup\n    aggregation: sum\n  - name: gate_receipts_pulled\n    description: Gate Receipts retrieved\n    unit: receipt\n    aggregation: sum\napis:\n  - name: Norfolk Southern Shipment Status API\n    baseURL: https://api.nscorp.com\n    tags:\n      - Freight\n      - Railroad\n      - Shipment\n      - Tracking\n    serviceName: Norfolk Southern Shipment Status API\n    serviceCategory: Freight Rail\n  - name: Norfolk Southern Trip Plan API\n    baseURL: https://api.nscorp.com\n    tags:\n      - ETA\n      - Railroad\n      - Route\n      - Trip Plan\n    serviceName: Norfolk Southern Trip Plan API\n    serviceCategory: Freight Rail\n  - name: Norfolk Southern Gate Receipts API\n    baseURL: https://api.nscorp.com\n    tags:\n      - Gate Receipts\n      - Intermodal\n      - Terminal\n    serviceName: Norfolk Southern Gate Receipts API\n    serviceCategory: Freight Rail\nunitEconomics:\n  - name: Polls per shipment\n    metric: shipment_status_polls\
  \ / active_shipments\n    target: minimize via webhooks where available\n  - name: Integration cost per shipment\n    metric: integration_engineering_cost / shipments_tracked\n    target: declining over time via reuse\nmaintainers:\n  - FN: API Evangelist\n    url: https://apievangelist.com\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/norfolk-southern/refs/heads/main/finops/norfolk-southern-finops.yml
sources:
- https://developer.nscorp.com/
- https://www.nscorp.com/site/customers/
specification: FinOps Framework
tags:
- Freight
- Logistics
- Railroad
- Shipping
- Transportation
- FinOps
- Cost Management
- FOCUS
---
