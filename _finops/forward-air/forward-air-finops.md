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
  - Tax
  - Adjustment
  pricingCategory: Contracted Rate Card
description: Forward Air bills freight services on a contracted-rate basis (LTL, truckload, intermodal, brokerage) rather than via a published API/SaaS pricing surface. FinOps treatment focuses on freight spend allocation and rate-card optimization.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Forward Air Corporation
  ProviderName: Forward Air
  PublisherName: Forward Air Corporation
  ServiceCategory: Freight & Logistics
  ServiceName: Forward Air
layout: finops
meters:
- aggregation: count
  dimensions:
  - service_type
  - origin
  - destination
  name: shipments
  unit: shipment
- aggregation: sum
  dimensions:
  - service_type
  - lane
  name: billable_weight
  unit: lb
- aggregation: sum
  dimensions:
  - charge_type
  name: accessorial_charges
  unit: charge
name: Forward Air Finops
provider_name: Forward Air
provider_slug: forward-air
publisher_name: Forward Air Corporation
service_category: Freight & Logistics
slug: forward-air-finops
source_filename: forward-air-finops.yml
source_heading: FinOps Profile
source_url: https://www.forwardair.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Forward Air\nproviderId: forward-air\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Freight\n  - Logistics\ndescription: Forward Air bills freight services on a contracted-rate basis (LTL, truckload, intermodal,\n  brokerage) rather than via a published API/SaaS pricing surface. FinOps treatment focuses on freight\n  spend allocation and rate-card optimization.\nnotes: No public API; FinOps shape inferred from a freight-carrier billing model. Reconcile against\n  a customer's master service agreement / rate card when available.\nsources:\n  - https://www.forwardair.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Forward\
  \ Air Corporation\nserviceCategory: Freight & Logistics\nbillingModel:\n  pricingCategory: Contracted Rate Card\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Forward Air\n  ServiceCategory: Freight & Logistics\n  ProviderName: Forward Air\n  PublisherName: Forward Air Corporation\n  InvoiceIssuerName: Forward Air Corporation\n  BillingCurrency: USD\nmeters:\n  - name: shipments\n    unit: shipment\n    aggregation: count\n    dimensions:\n      - service_type\n      - origin\n      - destination\n  - name: billable_weight\n    unit: lb\n    aggregation: sum\n    dimensions:\n      - service_type\n      - lane\n  - name: accessorial_charges\n    unit: charge\n    aggregation: sum\n    dimensions:\n      - charge_type\nprinciples:\n  - name: Visibility\n    description: Reconcile Forward Air invoices against shipment manifests and tracking records;\n      no public usage API is available.\n\
  \  - name: Allocation\n    description: Tag shipments with cost-center / project codes at booking time for downstream\n      chargeback.\n  - name: Optimization\n    description: Negotiate lane-specific and volume-tier rate cards; consolidate LTL where possible\n      to reduce accessorial fees.\n  - name: Accountability\n    description: Assign a freight-spend owner; review carrier mix and accessorial-fee variance\n      monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/forward-air/refs/heads/main/finops/forward-air-finops.yml
sources:
- https://www.forwardair.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Freight
- Logistics
---
