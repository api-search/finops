---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Mandate
  chargeCategories:
  - Purchase
  pricingCategory: Bilateral Contract
description: FOCUS-aligned FinOps placeholder for Piper Sandler. As an investment bank and institutional broker-dealer, Piper Sandler bills clients via brokerage commissions, advisory fees, and research / platform subscriptions rather than as a metered API SKU.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Piper Sandler Companies
  ProviderName: Piper Sandler
  PublisherName: Piper Sandler Companies
  ServiceCategory: Capital Markets
  ServiceName: Piper Sandler Institutional
  ServiceSubcategory: Investment Banking and Institutional Brokerage
layout: finops
meters:
- aggregation: count
  description: Bilateral institutional client mandate (research distribution, trading, advisory). Not metered per-call.
  dimensions:
  - product_line
  - region
  name: institutional_client_contract
  unit: contract
- aggregation: sum
  description: Per-trade or per-share commission billed at execution. Not API-metered.
  dimensions:
  - asset_class
  name: brokerage_commission
  unit: trade
name: Piper Sandler Finops
provider_name: Piper Sandler Companies
provider_slug: piper-sandler
publisher_name: Piper Sandler Companies
service_category: Capital Markets
slug: piper-sandler-finops
source_filename: piper-sandler-finops.yml
source_heading: FinOps Profile
source_url: https://www.pipersandler.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Piper Sandler Companies\nproviderId: piper-sandler\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Investment Banking\n  - Capital Markets\nnotes: Piper Sandler is an investment bank, not a software / API vendor. There is no public\n  metered API to model. This artifact captures the FinOps shape only at the institutional client\n  contract level.\ndescription: FOCUS-aligned FinOps placeholder for Piper Sandler. As an investment bank and\n  institutional broker-dealer, Piper Sandler bills clients via brokerage commissions, advisory\n  fees, and research / platform subscriptions rather than as a metered API SKU.\nsources:\n  - https://www.pipersandler.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl:\
  \ https://focus.finops.org/focus-specification/v1-3/\npublisherName: Piper Sandler Companies\nserviceCategory: Capital Markets\nbillingModel:\n  pricingCategory: Bilateral Contract\n  billingFrequency: Per-Mandate\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Piper Sandler Institutional\n  ServiceCategory: Capital Markets\n  ServiceSubcategory: Investment Banking and Institutional Brokerage\n  ProviderName: Piper Sandler\n  PublisherName: Piper Sandler Companies\n  InvoiceIssuerName: Piper Sandler Companies\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: institutional_client_contract\n    description: Bilateral institutional client mandate (research distribution, trading,\n      advisory). Not metered per-call.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - product_line\n      - region\n  - name: brokerage_commission\n    description: Per-trade or per-share commission billed at execution. Not API-metered.\n\
  \    unit: trade\n    aggregation: sum\n    dimensions:\n      - asset_class\nprinciples:\n  - name: Visibility\n    description: Visibility lives at the brokerage / advisory invoice level rather than at API\n      consumption.\n  - name: Allocation\n    description: Allocate institutional fees and brokerage commissions to the consuming desk /\n      strategy / fund.\n  - name: Optimization\n    description: Optimize via execution-quality reviews and renegotiation of advisory mandates;\n      this is not an API-cost-optimization problem.\n  - name: Accountability\n    description: Buy-side trading desk and finance team own the relationship and review fees per\n      mandate.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/piper-sandler/refs/heads/main/finops/piper-sandler-finops.yml
sources:
- https://www.pipersandler.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Investment Banking
- Capital Markets
---
