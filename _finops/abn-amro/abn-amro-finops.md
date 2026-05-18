---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: EUR
  billingFrequency: Per-Invoice
  chargeCategories:
  - Purchase
  pricingCategory: Contract
description: ABN AMRO does not invoice per API call. PSD2 production access is free per the directive (TPPs bear their own licence and eIDAS-certificate cost). Tikkie and Business Account Payment usage is invoiced through the underlying ABN AMRO commercial banking product, not through a metered API surface.
focus_columns:
  BillingCurrency: EUR
  InvoiceIssuerName: ABN AMRO Bank N.V.
  ProviderName: ABN AMRO
  PublisherName: ABN AMRO Bank N.V.
  ServiceCategory: Financial Services / Open Banking
  ServiceName: ABN AMRO Developer APIs
layout: finops
meters:
- aggregation: count
  description: PSD2 production access — not a metered unit; cost is regulatory (TPP licence + eIDAS) rather than per-API-call.
  dimensions:
  - tpp
  name: psd2_production
  unit: licence
- aggregation: count
  description: Business-banking contract underlying Tikkie Business and Business Account Payment usage.
  dimensions:
  - customer
  name: business_contract
  unit: contract
name: Abn Amro Finops
provider_name: ABN AMRO
provider_slug: abn-amro
publisher_name: ABN AMRO Bank N.V.
service_category: Financial Services / Open Banking
slug: abn-amro-finops
source_filename: abn-amro-finops.yml
source_heading: FinOps Profile
source_url: https://developer.abnamro.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: ABN AMRO\nproviderId: abn-amro\ncreated: '2026-05-16'\nmodified: '2026-05-16'\nreconciled: false\ntags:\n  - Financial\n  - Open Banking\n  - PSD2\n  - FinOps\n  - FOCUS\ndescription: ABN AMRO does not invoice per API call. PSD2 production access is free per the directive (TPPs bear their own licence and eIDAS-certificate cost). Tikkie and Business Account Payment usage is invoiced through the underlying ABN AMRO commercial banking product, not through a metered API surface.\nnotes: No metered API invoice — costs flow through the regulator-mandated PSD2 framework or the underlying business-banking contract.\nsources:\n  - https://developer.abnamro.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: ABN AMRO Bank N.V.\nserviceCategory: Financial Services / Open Banking\nbillingModel:\n  pricingCategory: Contract\n  billingFrequency: Per-Invoice\n  billingCurrency: EUR\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: ABN AMRO Developer APIs\n  ServiceCategory: Financial Services / Open Banking\n  ProviderName: ABN AMRO\n  PublisherName: ABN AMRO Bank N.V.\n  InvoiceIssuerName: ABN AMRO Bank N.V.\n  BillingCurrency: EUR\nmeters:\n  - name: psd2_production\n    description: PSD2 production access — not a metered unit; cost is regulatory (TPP licence + eIDAS) rather than per-API-call.\n    unit: licence\n    aggregation: count\n    dimensions:\n      - tpp\n  - name: business_contract\n    description: Business-banking contract underlying Tikkie Business and Business Account Payment usage.\n    unit: contract\n    aggregation: count\n    dimensions:\n      - customer\nprinciples:\n  - name: Visibility\n    description: Track Tikkie and Business-API usage\
  \ against the linked commercial banking invoice and against any TPP-side eIDAS certificate spend.\n  - name: Allocation\n    description: Allocate Tikkie Business cost to the merchant / payment-collection cost centre and Business Account Payment cost to corporate treasury.\n  - name: Optimization\n    description: Optimize by consolidating PSD2 traffic within the 4-call/day unattended AIS limit and batching payments where the underlying SEPA rail allows.\n  - name: Accountability\n    description: Treasury / payments leadership owns the ABN AMRO relationship; integration teams own the developer-portal credentials and certificate lifecycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abn-amro/refs/heads/main/finops/abn-amro-finops.yml
sources:
- https://developer.abnamro.com/
specification: FinOps Framework
tags:
- Financial
- Open Banking
- PSD2
- FinOps
- FOCUS
---
