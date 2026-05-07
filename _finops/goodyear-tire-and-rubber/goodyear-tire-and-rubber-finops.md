---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sightline-api.yml
  format: yaml
  label: Goodyear SightLine API
  slug: sightline-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/goodyear-tire-and-rubber/refs/heads/main/openapi/sightline-api.yml
- filename: gaas-portal.yml
  format: yaml
  label: Goodyear API Management Portal
  slug: gaas-portal
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/goodyear-tire-and-rubber/refs/heads/main/openapi/gaas-portal.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Enterprise Contract
description: 'FOCUS-aligned FinOps for Goodyear''s SightLine + GaaS API portfolio: enterprise/partner-contracted access where commercial terms are not publicly disclosed. Meters reflect the consumption shape consumers should expect to track (vehicle/tire telematics ingest, catalog and work-order traffic).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: The Goodyear Tire & Rubber Company
  ProviderName: Goodyear Tire & Rubber
  PublisherName: The Goodyear Tire & Rubber Company
  ServiceCategory: Connected Vehicles / Tire Telematics
  ServiceName: Goodyear SightLine / GaaS APIs
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests across the SightLine + GaaS surface
  dimensions:
  - api
  - endpoint
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Telematics events ingested per vehicle/tire from SightLine
  dimensions:
  - vehicle
  - fleet
  - region
  name: tire_data_events
  unit: event
- aggregation: max
  description: Active connected vehicles or tires under contract
  dimensions:
  - fleet
  - region
  name: connected_vehicles
  unit: vehicle
- aggregation: sum
  description: Work orders / service tickets transacted via the truck tire APIs
  dimensions:
  - api
  - fleet
  name: work_orders
  unit: ticket
name: Goodyear Tire And Rubber Finops
provider_name: Goodyear Tire & Rubber
provider_slug: goodyear-tire-and-rubber
publisher_name: The Goodyear Tire & Rubber Company
service_category: Connected Vehicles / Tire Telematics
slug: goodyear-tire-and-rubber-finops
source_filename: goodyear-tire-and-rubber-finops.yml
source_heading: FinOps Profile
source_url: https://developer.goodyearsightline.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Goodyear Tire & Rubber\nproviderId: goodyear-tire-and-rubber\npublisherName: The Goodyear Tire & Rubber Company\nserviceCategory: Connected Vehicles / Tire Telematics\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Connected Vehicles\n  - Fleet Management\n  - IoT\n  - Telematics\n  - Tires\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Goodyear''s SightLine + GaaS API portfolio: enterprise/partner-contracted\n  access where commercial terms are not publicly disclosed. Meters reflect the consumption shape consumers\n  should expect to track (vehicle/tire telematics ingest, catalog and work-order traffic).'\n\
  notes: No public pricing or invoice surface was found at reconciliation time. Billing model assumes a contracted\n  recurring fee plus optional usage-based components negotiated through the GaaS portal; replace once the\n  partner agreement terms are known.\nsources:\n  - https://developer.goodyearsightline.com/\n  - https://gaas-portal.goodyear.com/\nbillingModel:\n  pricingCategory: Enterprise Contract\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Goodyear SightLine / GaaS APIs\n  ServiceCategory: Connected Vehicles / Tire Telematics\n  ProviderName: Goodyear Tire & Rubber\n  PublisherName: The Goodyear Tire & Rubber Company\n  InvoiceIssuerName: The Goodyear Tire & Rubber Company\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests across the SightLine + GaaS surface\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - consumer\n  - name: tire_data_events\n    description: Telematics events ingested per vehicle/tire from SightLine\n    unit: event\n    aggregation: sum\n    dimensions:\n      - vehicle\n      - fleet\n      - region\n  - name: connected_vehicles\n    description: Active connected vehicles or tires under contract\n    unit: vehicle\n    aggregation: max\n    dimensions:\n      - fleet\n      - region\n  - name: work_orders\n    description: Work orders / service tickets transacted via the truck tire APIs\n    unit: ticket\n    aggregation: sum\n    dimensions:\n      - api\n      - fleet\napis:\n  - name: Goodyear SightLine API\n    baseURL: https://developer.goodyearsightline.com\n    serviceName: Goodyear SightLine API\n    serviceCategory: Tire Telematics\n  - name: Goodyear API Management Portal\n    baseURL: https://gaas-portal.goodyear.com\n    serviceName: Goodyear API Management Portal\n    serviceCategory: API Management\n\
  \  - name: Goodyear Truck Tire Catalog API\n    baseURL: https://api.catalog.goodyeartrucktires.com\n    serviceName: Goodyear Truck Tire Catalog API\n    serviceCategory: Catalog\n  - name: Goodyear Work Order API\n    baseURL: https://api.workorder.goodyeartrucktires.com\n    serviceName: Goodyear Work Order API\n    serviceCategory: Fleet Management\n  - name: Goodyear Service Ticket API\n    baseURL: https://api.serviceticket.goodyeartrucktires.com\n    serviceName: Goodyear Service Ticket API\n    serviceCategory: Fleet Management\nprinciples:\n  - name: Visibility\n    description: Track SightLine telematics ingest volume and GaaS API request counts per fleet via the\n      partner portal usage views; export to your data warehouse for cross-charging.\n  - name: Allocation\n    description: Tag API consumers by fleet ID and vehicle ID so tire-telematics and work-order spend can\n      be attributed to the operating unit owning each fleet.\n  - name: Optimization\n    description:\
  \ Reduce SightLine event ingest cost by tuning sampling intervals on low-risk axles, batching\n      catalog lookups, and consolidating service-ticket polling.\n  - name: Accountability\n    description: Assign each fleet contract a budget owner; reconcile Goodyear invoices against the consumed\n      vehicles and ticket volume captured in your fleet system of record.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/goodyear-tire-and-rubber/refs/heads/main/finops/goodyear-tire-and-rubber-finops.yml
sources:
- https://developer.goodyearsightline.com/
- https://gaas-portal.goodyear.com/
specification: FinOps Framework
tags:
- Connected Vehicles
- Fleet Management
- IoT
- Telematics
- Tires
- FinOps
- FOCUS
---
