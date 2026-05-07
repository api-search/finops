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
  - Purchase
  - Tax
  - Refund
  pricingCategory: Product Purchase
description: Fox Factory Holding Corp sells performance components via e-commerce and dealer channels. No SaaS or API billing surface; FinOps treatment is product-procurement-style for consuming organizations.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Fox Factory Holding Corp.
  ProviderName: Fox Factory
  PublisherName: Fox Factory Holding Corp.
  ServiceCategory: Manufacturing & Components
  ServiceName: Fox Factory Holding
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product_line
  - sku
  name: units_purchased
  unit: unit
- aggregation: sum
  dimensions:
  - product_line
  name: order_value
  unit: USD
name: Fox Factory Holding Finops
provider_name: Fox Factory Holding
provider_slug: fox-factory-holding
publisher_name: Fox Factory Holding Corp.
service_category: Manufacturing & Components
slug: fox-factory-holding-finops
source_filename: fox-factory-holding-finops.yml
source_heading: FinOps Profile
source_url: https://www.ridefox.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Fox Factory Holding\nproviderId: fox-factory-holding\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Manufacturing\n  - Powersports\ndescription: Fox Factory Holding Corp sells performance components via e-commerce and dealer\n  channels. No SaaS or API billing surface; FinOps treatment is product-procurement-style for\n  consuming organizations.\nnotes: No public API or pricing surface; FinOps shape inferred from a consumer-products procurement\n  model.\nsources:\n  - https://www.ridefox.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Fox Factory Holding Corp.\nserviceCategory: Manufacturing & Components\nbillingModel:\n\
  \  pricingCategory: Product Purchase\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Refund\nfocusColumns:\n  ServiceName: Fox Factory Holding\n  ServiceCategory: Manufacturing & Components\n  ProviderName: Fox Factory\n  PublisherName: Fox Factory Holding Corp.\n  InvoiceIssuerName: Fox Factory Holding Corp.\n  BillingCurrency: USD\nmeters:\n  - name: units_purchased\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - product_line\n      - sku\n  - name: order_value\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - product_line\nprinciples:\n  - name: Visibility\n    description: Reconcile Fox Factory invoices against purchase orders; no usage telemetry API\n      exists.\n  - name: Allocation\n    description: Allocate purchases to bills-of-materials or project codes at PO time.\n  - name: Optimization\n    description: Negotiate dealer-volume terms; consolidate orders to reduce shipping and\n  \
  \    handling.\n  - name: Accountability\n    description: Procurement function owns spend; review BOM cost variance against forecast.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fox-factory-holding/refs/heads/main/finops/fox-factory-holding-finops.yml
sources:
- https://www.ridefox.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Manufacturing
- Powersports
---
