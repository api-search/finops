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
  - Adjustment
  pricingCategory: Per Purchase Order (Negotiated Discount)
description: 'FinOps shape for Knoll Inc: B2B furniture manufacturer billing per purchase order under dealer-channel agreements. No public API tariff; product prices follow the Knoll Price Book and dealer discount tiers.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Knoll, Inc.
  ProviderName: Knoll Inc
  PublisherName: Knoll, Inc.
  ServiceCategory: Furniture
  ServiceName: Knoll Inc
layout: finops
meters:
- aggregation: sum
  dimensions:
  - dealer
  - product_line
  name: purchase_orders
  unit: order
- aggregation: sum
  dimensions:
  - product_line
  - sku
  name: line_items
  unit: line
- aggregation: sum
  dimensions:
  - dealer
  - product_line
  name: order_value
  unit: USD
- aggregation: sum
  dimensions:
  - endpoint
  name: api_calls
  unit: request
name: Knoll Finops
provider_name: Knoll Inc
provider_slug: knoll
publisher_name: Knoll, Inc. (a MillerKnoll company)
service_category: Furniture & Manufacturing
slug: knoll-finops
source_filename: knoll-finops.yml
source_heading: FinOps Profile
source_url: https://www.knoll.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Knoll Inc\nproviderId: knoll\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Furniture\n  - Manufacturing\ndescription: 'FinOps shape for Knoll Inc: B2B furniture manufacturer billing per purchase order under\n  dealer-channel agreements. No public API tariff; product prices follow the Knoll Price Book and dealer\n  discount tiers.'\nsources:\n  - https://www.knoll.com\n  - https://developer.knoll.com\nnotes: No public API pricing. Reconcile cost models from actual purchase orders and dealer-discount\n  schedules.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Knoll, Inc. (a MillerKnoll company)\nserviceCategory: Furniture &\
  \ Manufacturing\nbillingModel:\n  pricingCategory: Per Purchase Order (Negotiated Discount)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Knoll Inc\n  ServiceCategory: Furniture\n  ProviderName: Knoll Inc\n  PublisherName: Knoll, Inc.\n  InvoiceIssuerName: Knoll, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: purchase_orders\n    unit: order\n    aggregation: sum\n    dimensions:\n      - dealer\n      - product_line\n  - name: line_items\n    unit: line\n    aggregation: sum\n    dimensions:\n      - product_line\n      - sku\n  - name: order_value\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - dealer\n      - product_line\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Use Knoll API order and invoice endpoints (where available) plus dealer EDI feeds to\n     \
  \ track price-book vs net-of-discount per project.\n  - name: Allocation\n    description: Tag purchase orders by project / floor / business unit so furniture spend rolls up to\n      the right cost center.\n  - name: Optimization\n    description: Negotiate dealer-discount tiers and product-line bundling; use Knoll configurator data\n      to compare alternates and consolidate to higher-discount product lines.\n  - name: Accountability\n    description: Procurement reviews dealer invoices against the Knoll Price Book and contract discount\n      tier; disputes mismatches and re-negotiates at the next contract cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/knoll/refs/heads/main/finops/knoll-finops.yml
sources:
- https://www.knoll.com
- https://developer.knoll.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Furniture
- Manufacturing
---
