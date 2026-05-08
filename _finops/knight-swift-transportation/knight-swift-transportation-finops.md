---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Adjustment
  pricingCategory: Negotiated Per-Load
description: 'FinOps shape for Knight-Swift: per-load freight billing under a negotiated carrier-services agreement; API access bundled into the contract. No public tariff.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Knight-Swift Transportation Holdings Inc.
  ProviderName: Knight-Swift Transportation
  PublisherName: Knight-Swift Transportation Holdings Inc.
  ServiceCategory: Transportation
  ServiceName: Knight-Swift Transportation
layout: finops
meters:
- aggregation: sum
  dimensions:
  - mode
  - lane
  - shipper
  name: loads_tendered
  unit: load
- aggregation: sum
  dimensions:
  - mode
  - lane
  name: linehaul_charges
  unit: USD
- aggregation: sum
  dimensions:
  - accessorial_type
  name: accessorials
  unit: USD
- aggregation: sum
  dimensions:
  - lane
  name: fuel_surcharge
  unit: USD
- aggregation: sum
  dimensions:
  - endpoint
  - shipper
  name: api_calls
  unit: request
name: Knight Swift Transportation Finops
provider_name: Knight-Swift Transportation
provider_slug: knight-swift-transportation
publisher_name: Knight-Swift Transportation Holdings Inc.
service_category: Transportation & Logistics
slug: knight-swift-transportation-finops
source_filename: knight-swift-transportation-finops.yml
source_heading: FinOps Profile
source_url: https://developer.knight-swift.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Knight-Swift Transportation\nproviderId: knight-swift-transportation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Transportation\n  - Logistics\n  - Freight\ndescription: 'FinOps shape for Knight-Swift: per-load freight billing under a negotiated carrier-services\n  agreement; API access bundled into the contract. No public tariff.'\nsources:\n  - https://developer.knight-swift.com\n  - https://www.knight-swift.com\nnotes: Knight-Swift's freight invoicing is per-shipment under negotiated lane rates; API access fees\n  (if any) are bundled. Reconcile from actual customer invoices and contract terms.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Knight-Swift Transportation Holdings Inc.\nserviceCategory: Transportation & Logistics\nbillingModel:\n  pricingCategory: Negotiated Per-Load\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Knight-Swift Transportation\n  ServiceCategory: Transportation\n  ProviderName: Knight-Swift Transportation\n  PublisherName: Knight-Swift Transportation Holdings Inc.\n  InvoiceIssuerName: Knight-Swift Transportation Holdings Inc.\n  BillingCurrency: USD\nmeters:\n  - name: loads_tendered\n    unit: load\n    aggregation: sum\n    dimensions:\n      - mode\n      - lane\n      - shipper\n  - name: linehaul_charges\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - mode\n      - lane\n  - name: accessorials\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - accessorial_type\n  - name: fuel_surcharge\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - lane\n  -\
  \ name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - shipper\nprinciples:\n  - name: Visibility\n    description: Pull load and billing data from the Knight-Swift API (status, tender response, invoice)\n      and reconcile against EDI 210 freight invoices to match expected vs actual lane rates.\n  - name: Allocation\n    description: Tag tendered loads with internal cost-center metadata (plant, BU, customer order) so\n      freight spend can be attributed by business unit.\n  - name: Optimization\n    description: Use Knight-Swift Logistics' multi-carrier visibility to compare modes (TL/LTL/Intermodal),\n      consolidate loads, and shift commodities to lower-cost lanes; review accessorial charges (detention,\n      layover) for process fixes.\n  - name: Accountability\n    description: Logistics owners reconcile per-shipment invoices weekly, dispute incorrect accessorials,\n      and feed lane performance back into the next contract negotiation.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/knight-swift-transportation/refs/heads/main/finops/knight-swift-transportation-finops.yml
sources:
- https://developer.knight-swift.com
- https://www.knight-swift.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Transportation
- Logistics
- Freight
---
