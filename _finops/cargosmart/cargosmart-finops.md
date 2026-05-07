---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Container Booking API
  slug: cargosmart-container-booking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Shipment Tracking API
  slug: cargosmart-shipment-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Vessel Schedule API
  slug: cargosmart-vessel-schedule-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
- filename: cargosmart-shipment-tracking-openapi.yml
  format: yaml
  label: CargoSmart Shipping Documentation API
  slug: cargosmart-shipping-documents-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/openapi/cargosmart-shipment-tracking-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Per-Container
description: 'FOCUS-aligned FinOps for CargoSmart/IQAX: enterprise license + per-tracked-container fees on the IQAX shipment-management platform; billing is contract-based.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: CargoSmart Limited (IQAX)
  ProviderName: CargoSmart
  PublisherName: CargoSmart Limited (IQAX)
  ServiceCategory: Shipment Management Platform
  ServiceName: CargoSmart / IQAX Platform
layout: finops
meters:
- aggregation: sum
  dimensions:
  - module
  name: enterprise_license
  unit: year
- aggregation: sum
  dimensions:
  - carrier
  - trade_lane
  name: tracked_containers
  unit: container
- aggregation: sum
  dimensions:
  - carrier
  name: bookings_created
  unit: booking
- aggregation: sum
  dimensions:
  - document_type
  name: documents_processed
  unit: document
- aggregation: max
  name: named_users
  unit: seat-month
name: Cargosmart Finops
provider_name: CargoSmart
provider_slug: cargosmart
publisher_name: CargoSmart Limited (IQAX)
service_category: Shipment Management Platform
slug: cargosmart-finops
source_filename: cargosmart-finops.yml
source_heading: FinOps Profile
source_url: https://www.cargosmart.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CargoSmart\nproviderId: cargosmart\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Logistics\n  - Ocean Freight\n  - Supply Chain\ndescription: 'FOCUS-aligned FinOps for CargoSmart/IQAX: enterprise license + per-tracked-container fees\n  on the IQAX shipment-management platform; billing is contract-based.'\nnotes: CargoSmart/IQAX does not publish public API or container-volume pricing. FinOps mapping is provisional\n  pending enterprise-contract reconciliation.\nsources:\n  - https://www.cargosmart.com/\n  - https://www.iqax.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CargoSmart Limited (IQAX)\nserviceCategory: Shipment\
  \ Management Platform\nbillingModel:\n  pricingCategory: Subscription + Per-Container\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: CargoSmart / IQAX Platform\n  ServiceCategory: Shipment Management Platform\n  ProviderName: CargoSmart\n  PublisherName: CargoSmart Limited (IQAX)\n  InvoiceIssuerName: CargoSmart Limited (IQAX)\n  BillingCurrency: USD\nmeters:\n  - name: enterprise_license\n    unit: year\n    aggregation: sum\n    dimensions:\n      - module\n  - name: tracked_containers\n    unit: container\n    aggregation: sum\n    dimensions:\n      - carrier\n      - trade_lane\n  - name: bookings_created\n    unit: booking\n    aggregation: sum\n    dimensions:\n      - carrier\n  - name: documents_processed\n    unit: document\n    aggregation: sum\n    dimensions:\n      - document_type\n  - name: named_users\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name:\
  \ Visibility\n    description: Use the IQAX platform reporting and audit logs to attribute container-volume cost to\n      trade lanes, carriers, and business units.\n  - name: Allocation\n    description: Allocate by carrier, trade lane, and originating business unit; multi-BU customers should\n      configure distinct organization tenants.\n  - name: Optimization\n    description: Right-size tracked-container quotas to actual fleet activity; consolidate carrier integrations\n      via GSBN where possible.\n  - name: Accountability\n    description: Logistics-operations / digital-supply-chain lead owns the relationship; quarterly volume\n      reviews with CargoSmart/IQAX are typical.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cargosmart/refs/heads/main/finops/cargosmart-finops.yml
sources:
- https://www.cargosmart.com/
- https://www.iqax.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Logistics
- Ocean Freight
- Supply Chain
---
