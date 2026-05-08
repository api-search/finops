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
  - Refund
  pricingCategory: Custom Contract
description: FinOps for Minerals Technologies does not map to a cloud / API consumption model; commercial spend is governed by negotiated B2B supply contracts denominated in shipped product units (tons, pounds, pallets) rather than API meters.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Minerals Technologies, Inc.
  ProviderName: Minerals Technologies
  PublisherName: Minerals Technologies, Inc.
  ServiceCategory: Industrial Materials
  ServiceName: Minerals Technologies
layout: finops
meters:
- aggregation: sum
  dimensions:
  - product
  - facility
  - customer
  name: shipped_tons
  unit: ton
- aggregation: sum
  dimensions:
  - product
  - sku
  name: shipped_units
  unit: varies
- aggregation: sum
  dimensions:
  - contract
  - customer
  name: contract_value
  unit: USD
name: Minerals Technologies Finops
provider_name: Minerals Technologies
provider_slug: minerals-technologies
publisher_name: Minerals Technologies, Inc.
service_category: Industrial Materials
slug: minerals-technologies-finops
source_filename: minerals-technologies-finops.yml
source_heading: FinOps Profile
source_url: https://www.mineralstech.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Minerals Technologies\nproviderId: minerals-technologies\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Industrial\ndescription: 'FinOps for Minerals Technologies does not map to a cloud / API consumption model;\n  commercial spend is governed by negotiated B2B supply contracts denominated in shipped product\n  units (tons, pounds, pallets) rather than API meters.'\nsources:\n  - https://www.mineralstech.com/\nnotes: Industrial supplier without a public API. FinOps mapping is structural only; meters reflect\n  procurement-style line items.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Minerals Technologies, Inc.\nserviceCategory:\
  \ Industrial Materials\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Minerals Technologies\n  ServiceCategory: Industrial Materials\n  ProviderName: Minerals Technologies\n  PublisherName: Minerals Technologies, Inc.\n  InvoiceIssuerName: Minerals Technologies, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: shipped_tons\n    unit: ton\n    aggregation: sum\n    dimensions:\n      - product\n      - facility\n      - customer\n  - name: shipped_units\n    unit: varies\n    aggregation: sum\n    dimensions:\n      - product\n      - sku\n  - name: contract_value\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - contract\n      - customer\nprinciples:\n  - name: Visibility\n    description: Procurement teams should track Minerals Technologies invoices and shipments through\n \
  \     the ERP / SAP receivables system; no programmatic usage feed is available.\n  - name: Allocation\n    description: Allocate invoiced cost to receiving plant / business unit using purchase-order line\n      metadata.\n  - name: Optimization\n    description: Negotiate volume tiers per contract; review supplier consolidation versus Imerys /\n      US Concrete alternatives.\n  - name: Accountability\n    description: Accountable to plant procurement / supply-chain leadership; reconcile shipped tonnage\n      against PO commitments.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/minerals-technologies/refs/heads/main/finops/minerals-technologies-finops.yml
sources:
- https://www.mineralstech.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Industrial
---
