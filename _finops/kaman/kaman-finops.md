---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Order
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Goods / Parts Distribution
description: FOCUS-aligned FinOps scaffold for Kaman Corporation B2B integration channels. Treated as goods / parts distribution, not as a metered API.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Kaman Aerospace Group, Inc.
  ProviderName: Kaman Corporation
  PublisherName: Kaman Aerospace Group, Inc.
  ServiceCategory: Aerospace / Industrial Distribution
  ServiceName: Kaman B2B Integration
layout: finops
meters:
- aggregation: count
  dimensions:
  - division
  - customer
  name: purchase_orders
  unit: order
- aggregation: sum
  dimensions:
  - partner
  - document_type
  name: edi_messages
  unit: message
- aggregation: sum
  dimensions:
  - division
  - customer
  name: line_items
  unit: line_item
name: Kaman Finops
provider_name: Kaman Corporation
provider_slug: kaman
publisher_name: Kaman Aerospace Group, Inc.
service_category: Aerospace / Industrial Distribution
slug: kaman-finops
source_filename: kaman-finops.yml
source_heading: FinOps Profile
source_url: https://www.kaman.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Kaman Corporation\nproviderId: kaman\npublisherName: Kaman Aerospace Group, Inc.\nserviceCategory: Aerospace / Industrial Distribution\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Kaman does not expose a public usage-billing surface. FinOps shape inferred from a\n  goods + parts-distribution model; meters reflect typical EDI / order-flow billable units.\ntags:\n  - Aerospace\n  - Distribution\n  - Industrial\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for Kaman Corporation B2B integration channels.\n  Treated as goods / parts distribution, not as a metered API.\nsources:\n  - https://www.kaman.com/\n\
  \  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Goods / Parts Distribution\n  billingFrequency: Per-Order\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Kaman B2B Integration\n  ServiceCategory: Aerospace / Industrial Distribution\n  ProviderName: Kaman Corporation\n  PublisherName: Kaman Aerospace Group, Inc.\n  InvoiceIssuerName: Kaman Aerospace Group, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: purchase_orders\n    unit: order\n    aggregation: count\n    dimensions:\n      - division\n      - customer\n  - name: edi_messages\n    unit: message\n    aggregation: sum\n    dimensions:\n      - partner\n      - document_type\n  - name: line_items\n    unit: line_item\n    aggregation: sum\n    dimensions:\n      - division\n      - customer\nprinciples:\n  - name: Visibility\n    description: Reconcile EDI message\
  \ counts and PO volumes against Kaman invoices since\n      no first-party usage API is exposed.\n  - name: Allocation\n    description: Allocate by Kaman division (Aerospace vs Distribution) and by program /\n      contract to mirror invoice line items.\n  - name: Optimization\n    description: Consolidate EDI partners and right-size order frequency to reduce\n      per-message overhead and expedite-fee exposure.\n  - name: Accountability\n    description: Procurement / supply-chain owns Kaman spend; pair with the Kaman account\n      manager for contract review.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kaman/refs/heads/main/finops/kaman-finops.yml
sources:
- https://www.kaman.com/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Aerospace
- Distribution
- Industrial
- FinOps
- FOCUS
---
