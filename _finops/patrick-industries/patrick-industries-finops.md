---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Shipment / Net Terms
  chargeCategories:
  - Purchase
  pricingCategory: Purchase Order
description: Structural FinOps placeholder for Patrick Industries. Component supplier billed through purchase orders and EDI to OEM customers; no public per-API pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Patrick Industries, Inc.
  ProviderName: Patrick Industries
  PublisherName: Patrick Industries, Inc.
  ServiceCategory: Manufacturing
  ServiceName: Patrick Industries Components
layout: finops
meters:
- aggregation: sum
  description: Components / SKUs shipped to OEM customer
  dimensions:
  - sku
  - customer
  - market
  name: parts_shipped
  unit: unit
- aggregation: sum
  description: Purchase-order line value
  dimensions:
  - customer
  - po
  name: po_value
  unit: USD
name: Patrick Industries Finops
provider_name: Patrick Industries
provider_slug: patrick-industries
publisher_name: Patrick Industries, Inc.
service_category: Manufacturing
slug: patrick-industries-finops
source_filename: patrick-industries-finops.yml
source_heading: FinOps Profile
source_url: https://www.patrickind.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Patrick Industries\nproviderId: patrick-industries\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: No public pricing or APIs — manufacturer/distributor billed via PO / EDI to OEM customers.\ntags:\n  - FinOps\n  - FOCUS\n  - RV\n  - Marine\n  - Manufacturing\ndescription: Structural FinOps placeholder for Patrick Industries. Component supplier billed\n  through purchase orders and EDI to OEM customers; no public per-API pricing.\nsources:\n  - https://www.patrickind.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Patrick Industries, Inc.\nserviceCategory: Manufacturing\nbillingModel:\n  pricingCategory:\
  \ Purchase Order\n  billingFrequency: Per Shipment / Net Terms\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Patrick Industries Components\n  ServiceCategory: Manufacturing\n  ProviderName: Patrick Industries\n  PublisherName: Patrick Industries, Inc.\n  InvoiceIssuerName: Patrick Industries, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: parts_shipped\n    description: Components / SKUs shipped to OEM customer\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - sku\n      - customer\n      - market\n  - name: po_value\n    description: Purchase-order line value\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - customer\n      - po\nprinciples:\n  - name: Visibility\n    description: Visibility comes from customer ERP / EDI receipts; no Patrick-published consumer\n      API.\n  - name: Allocation\n    description: Allocate by SKU, customer, and end market (RV / Marine / Powersports / Housing).\n\
  \  - name: Optimization\n    description: Optimization is on the OEM side via vendor consolidation, lead-time planning,\n      and SKU rationalization.\n  - name: Accountability\n    description: OEM procurement owner accountable for spend; supplier scorecard reviews quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/patrick-industries/refs/heads/main/finops/patrick-industries-finops.yml
sources:
- https://www.patrickind.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- RV
- Marine
- Manufacturing
---
