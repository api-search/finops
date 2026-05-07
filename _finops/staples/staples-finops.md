---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: staples-advantage-eprocurement-api-openapi.yml
  format: yaml
  label: Staples Advantage eProcurement API
  slug: staples-advantage-eprocurement-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/staples/refs/heads/main/openapi/staples-advantage-eprocurement-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Procurement (Per-Order)
description: Staples Advantage eProcurement is a B2B procurement contract, not a per-call API product. Cost surfaces as the line items on the Staples Business Advantage invoice (purchased goods, shipping, applicable taxes), not as an API-usage meter. FinOps shape is procurement-spend tracking against the negotiated agreement; per-call API metering does not apply.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Staples, Inc.
  ProviderName: Staples
  PublisherName: Staples, Inc.
  ServiceCategory: B2B Procurement
  ServiceName: Staples Advantage eProcurement
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cost_center
  - department
  - punchout_session
  name: purchase_order_value
  unit: USD
- aggregation: count
  dimensions:
  - sku_category
  - cost_center
  name: purchase_order_lines
  unit: line
name: Staples Finops
provider_name: Staples
provider_slug: staples
publisher_name: Staples, Inc. (Staples Business Advantage)
service_category: B2B Procurement
slug: staples-finops
source_filename: staples-finops.yml
source_heading: FinOps Profile
source_url: https://www.staplesadvantage.com/learn/eprocurement-integrations
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Staples\nproviderId: staples\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Office Supplies\n  - Procurement\n  - eProcurement\n  - B2B\n  - FinOps\n  - FOCUS\ndescription: Staples Advantage eProcurement is a B2B procurement contract, not a per-call API product. Cost surfaces as the line items on the Staples Business Advantage invoice (purchased goods, shipping, applicable taxes), not as an API-usage meter. FinOps shape is procurement-spend tracking against the negotiated agreement; per-call API metering does not apply.\nsources:\n  - https://www.staplesadvantage.com/learn/eprocurement-integrations\nnotes: No API usage meter. FOCUS-style modeling here describes procurement spend (purchase orders, line items) rather than per-call API charges, since access is bundled into the procurement agreement.\nalignedWith:\n  framework: FinOps\
  \ Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Staples, Inc. (Staples Business Advantage)\nserviceCategory: B2B Procurement\nbillingModel:\n  pricingCategory: Procurement (Per-Order)\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Staples Advantage eProcurement\n  ServiceCategory: B2B Procurement\n  ProviderName: Staples\n  PublisherName: Staples, Inc.\n  InvoiceIssuerName: Staples, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: purchase_order_value\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - cost_center\n      - department\n      - punchout_session\n  - name: purchase_order_lines\n    unit: line\n    aggregation: count\n    dimensions:\n      - sku_category\n      - cost_center\nprinciples:\n \
  \ - name: Visibility\n    description: Spend is visible through the Staples Business Advantage account dashboard and through the integrated procurement system (Ariba, Coupa, Jaggaer, Oracle, NetSuite). Pull cXML order responses or EDI 810 invoices into the procurement-analytics layer for line-level visibility.\n  - name: Allocation\n    description: Allocate spend by cost center / department through the procurement system's chart-of-accounts mapping. PunchOut sessions carry the requisitioner identity into Staples for downstream reporting.\n  - name: Optimization\n    description: Cost levers are catalog-side - enforce contract-priced SKU lists in the punch-out catalog, set per-requester approval thresholds, and consolidate orders to qualify for shipping / volume discounts negotiated in the master agreement.\n  - name: Accountability\n    description: Procurement / sourcing team owns the Staples Business Advantage agreement; department managers own their cost-center spend through the procurement\
  \ system's approval flow.\nmaintainers:\n  - name: Staples Business Advantage\n    url: https://www.staplesadvantage.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/staples/refs/heads/main/finops/staples-finops.yml
sources:
- https://www.staplesadvantage.com/learn/eprocurement-integrations
specification: FinOps Framework
tags:
- Office Supplies
- Procurement
- eProcurement
- B2B
- FinOps
- FOCUS
---
