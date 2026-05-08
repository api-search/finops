---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: Local (ARS, BRL, MXN, CLP, COP, USD)
  billingFrequency: Per-Transaction
  chargeCategories:
  - Usage
  - Adjustment
  pricingCategory: Transaction Fee
description: FOCUS-aligned FinOps profile for Mercado Libre. The marketplace REST APIs are free to use; cost is incurred via marketplace listing/sale fees, Mercado Pago transaction fees, shipping costs (Mercado Envios), and advertising spend (Mercado Ads).
focus_columns:
  BillingCurrency: Local Currency
  ChargeCategory: Usage
  InvoiceIssuerName: Mercado Libre (country entity)
  ProviderName: Mercado Libre
  PublisherName: Mercado Libre
  ServiceCategory: E-Commerce
  ServiceName: Mercado Libre Marketplace
layout: finops
meters:
- aggregation: sum
  description: Commission charged on completed marketplace sales.
  dimensions:
  - country
  - category
  - listing_type
  name: marketplace_sale_fee
  unit: percent_of_sale
- aggregation: sum
  description: Mercado Pago processing fee per payment.
  dimensions:
  - country
  - payment_method
  name: payment_processing_fee
  unit: percent_plus_fixed
- aggregation: sum
  description: Mercado Envios shipping label cost.
  dimensions:
  - country
  - service_level
  name: shipping_fee
  unit: per_shipment
- aggregation: sum
  description: Mercado Ads (Product Ads, Brand Ads) spend.
  dimensions:
  - country
  - campaign
  name: ads_spend
  unit: currency
name: Mercado Libre Finops
provider_name: Mercado Libre
provider_slug: mercado-libre
publisher_name: Mercado Libre
service_category: E-Commerce
slug: mercado-libre-finops
source_filename: mercado-libre-finops.yml
source_heading: FinOps Profile
source_url: https://www.mercadolibre.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Mercado Libre\nproviderId: mercado-libre\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- E-Commerce\n- Marketplace\n- Latin America\n- Payments\n- Mercado Pago\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Mercado Libre. The marketplace REST APIs are free to use; cost is incurred via marketplace listing/sale fees, Mercado Pago transaction fees, shipping costs (Mercado Envios), and advertising spend (Mercado Ads).\nnotes: Cost lever is at the commerce layer (fees and ads), not the API layer. Negotiate seller terms by country and category.\nsources:\n- https://www.mercadolibre.com/\n- https://developers.mercadolibre.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec:\
  \ FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Mercado Libre\nserviceCategory: E-Commerce\nbillingModel:\n  pricingCategory: Transaction Fee\n  billingFrequency: Per-Transaction\n  billingCurrency: Local (ARS, BRL, MXN, CLP, COP, USD)\n  chargeCategories:\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Mercado Libre Marketplace\n  ServiceCategory: E-Commerce\n  ProviderName: Mercado Libre\n  PublisherName: Mercado Libre\n  InvoiceIssuerName: Mercado Libre (country entity)\n  BillingCurrency: Local Currency\n  ChargeCategory: Usage\nmeters:\n- name: marketplace_sale_fee\n  description: Commission charged on completed marketplace sales.\n  unit: percent_of_sale\n  aggregation: sum\n  dimensions:\n  - country\n  - category\n  - listing_type\n- name: payment_processing_fee\n  description: Mercado Pago processing fee per payment.\n  unit: percent_plus_fixed\n  aggregation: sum\n  dimensions:\n  - country\n  - payment_method\n\
  - name: shipping_fee\n  description: Mercado Envios shipping label cost.\n  unit: per_shipment\n  aggregation: sum\n  dimensions:\n  - country\n  - service_level\n- name: ads_spend\n  description: Mercado Ads (Product Ads, Brand Ads) spend.\n  unit: currency\n  aggregation: sum\n  dimensions:\n  - country\n  - campaign\nprinciples:\n- name: Visibility\n  description: Pull seller billing reports by country entity; reconcile with Mercado Pago dashboards and Ads invoicing.\n- name: Allocation\n  description: Tag listings by SKU and brand to attribute fees to product lines.\n- name: Optimization\n  description: Tune listing type (free vs. classic vs. premium), shipping mode, and ad bidding to reduce blended take rate.\n- name: Accountability\n  description: Assign country-level commerce owners to track fee structures and renegotiate at scale.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mercado-libre/refs/heads/main/finops/mercado-libre-finops.yml
sources:
- https://www.mercadolibre.com/
- https://developers.mercadolibre.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- E-Commerce
- Marketplace
- Latin America
- Payments
- Mercado Pago
- FinOps
- Cost Management
- FOCUS
---
