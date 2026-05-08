---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per Purchase Order
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Industrial Goods (Quote-to-Cash)
description: 'FOCUS-aligned FinOps for CIRCOR International: industrial-goods commercial shape — product purchase orders, aftermarket parts, and service contracts. CIRCOR does not bill for API access and does not expose a metered usage surface. This artifact records the commercial cost shape that a buyer would see, not an API cost surface.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: CIRCOR International, Inc.
  PricingCategory: Industrial Goods
  ProviderName: CIRCOR International
  PublisherName: CIRCOR International, Inc.
  ServiceCategory: Industrial / Flow Control
  ServiceName: CIRCOR International
layout: finops
meters:
- aggregation: sum
  description: Industrial pumps, valves, and aerospace / defense flow-control products purchased
  dimensions:
  - business_group
  - product_family
  - region
  name: product_purchase
  unit: unit
- aggregation: sum
  description: Spare parts and consumables purchased post-installation
  dimensions:
  - product_family
  - asset_id
  name: aftermarket_parts
  unit: unit
- aggregation: sum
  description: Field service, maintenance, or extended warranty contracts
  dimensions:
  - tier
  - region
  name: service_contract
  unit: month
name: Circor International Finops
provider_name: CIRCOR International
provider_slug: circor-international
publisher_name: CIRCOR International, Inc.
service_category: Industrial / Flow Control
slug: circor-international-finops
source_filename: circor-international-finops.yml
source_heading: FinOps Profile
source_url: https://www.circor.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CIRCOR International\nproviderId: circor-international\ncreated: '2026-04-19'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Energy\n  - Flow Control\n  - Industrial\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for CIRCOR International: industrial-goods commercial shape —\n  product purchase orders, aftermarket parts, and service contracts. CIRCOR does not bill for API\n  access and does not expose a metered usage surface. This artifact records the commercial cost\n  shape that a buyer would see, not an API cost surface.'\nnotes: CIRCOR does not currently expose any API billing surface. The FinOps shape below describes\n  the industrial-product commercial relationship.\nsources:\n  - https://www.circor.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CIRCOR International, Inc.\nserviceCategory: Industrial / Flow Control\nbillingModel:\n  pricingCategory: Industrial Goods (Quote-to-Cash)\n  billingFrequency: Per Purchase Order\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: CIRCOR International\n  ServiceCategory: Industrial / Flow Control\n  ProviderName: CIRCOR International\n  PublisherName: CIRCOR International, Inc.\n  InvoiceIssuerName: CIRCOR International, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Industrial Goods\nmeters:\n  - name: product_purchase\n    description: Industrial pumps, valves, and aerospace / defense flow-control products purchased\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - business_group\n      - product_family\n      - region\n  - name: aftermarket_parts\n    description: Spare\
  \ parts and consumables purchased post-installation\n    unit: unit\n    aggregation: sum\n    dimensions:\n      - product_family\n      - asset_id\n  - name: service_contract\n    description: Field service, maintenance, or extended warranty contracts\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - region\nprinciples:\n  - name: Visibility\n    description: Track CIRCOR spend through purchase orders, asset / equipment registers, and\n      service-contract invoices.\n  - name: Allocation\n    description: Allocate flow-control assets to the operating site, plant, or platform that owns\n      them so industrial maintenance can be charged back accurately.\n  - name: Optimization\n    description: Standardize on common product families to simplify spares inventory; align service\n      contracts with planned outage cycles; retire end-of-life assets before excessive aftermarket\n      cost accrues.\n  - name: Accountability\n    description: Operations / engineering\
  \ owns the asset; procurement owns vendor terms; finance\n      reconciles purchase orders, parts spend, and service invoices.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circor-international/refs/heads/main/finops/circor-international-finops.yml
sources:
- https://www.circor.com/
specification: FinOps Framework
tags:
- Energy
- Flow Control
- Industrial
- FinOps
- FOCUS
---
