---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Transaction
  chargeCategories:
  - Adjustment
  pricingCategory: Revenue Share
description: FOCUS-aligned FinOps profile for Bandcamp. The APIs are free; the cost lever is the seller share Bandcamp deducts from artist sales (digital and merch). For API consumers (labels, fulfillment partners) the integration cost is essentially zero on the platform side.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Adjustment
  InvoiceIssuerName: Bandcamp
  ProviderName: Bandcamp
  PublisherName: Bandcamp
  ServiceCategory: Music Marketplace
  ServiceName: Bandcamp Partner API
layout: finops
meters:
- aggregation: sum
  description: Bandcamp's percentage of artist digital sales.
  dimensions:
  - band
  - release
  name: digital_sales_share
  unit: percent_of_sale
- aggregation: sum
  description: Bandcamp's percentage of merch sales.
  dimensions:
  - band
  - product
  name: merch_sales_share
  unit: percent_of_sale
name: Bandcamp Finops
provider_name: Bandcamp
provider_slug: bandcamp
publisher_name: Bandcamp
service_category: Music Marketplace
slug: bandcamp-finops
source_filename: bandcamp-finops.yml
source_heading: FinOps Profile
source_url: https://bandcamp.com/developer
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bandcamp\nproviderId: bandcamp\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Music\n- Marketplace\n- Indie\n- Audio\n- Sales\n- Merch\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Bandcamp. The APIs are free; the cost lever is the seller share\n  Bandcamp deducts from artist sales (digital and merch). For API consumers (labels, fulfillment\n  partners) the integration cost is essentially zero on the platform side.\nnotes: API is free; cost concentration is on artist sales share, billed implicitly via reduced payouts.\nsources:\n- https://bandcamp.com/developer\n- https://bandcamp.com/help/seller_help\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Bandcamp\nserviceCategory: Music Marketplace\nbillingModel:\n  pricingCategory: Revenue Share\n  billingFrequency: Per-Transaction\n  billingCurrency: USD\n  chargeCategories:\n  - Adjustment\nfocusColumns:\n  ServiceName: Bandcamp Partner API\n  ServiceCategory: Music Marketplace\n  ProviderName: Bandcamp\n  PublisherName: Bandcamp\n  InvoiceIssuerName: Bandcamp\n  BillingCurrency: USD\n  ChargeCategory: Adjustment\nmeters:\n- name: digital_sales_share\n  description: Bandcamp's percentage of artist digital sales.\n  unit: percent_of_sale\n  aggregation: sum\n  dimensions:\n  - band\n  - release\n- name: merch_sales_share\n  description: Bandcamp's percentage of merch sales.\n  unit: percent_of_sale\n  aggregation: sum\n  dimensions:\n  - band\n  - product\nprinciples:\n- name: Visibility\n  description: Pull Sales Report API regularly to reconcile gross sales against Bandcamp payouts.\n- name: Allocation\n  description: Allocate sales-share cost to the artist or release\
  \ that generated it.\n- name: Optimization\n  description: Lever is product mix and Bandcamp Friday participation; not API-side.\n- name: Accountability\n  description: Label or fulfillment partner owns the API credentials and reconciliation.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bandcamp/refs/heads/main/finops/bandcamp-finops.yml
sources:
- https://bandcamp.com/developer
- https://bandcamp.com/help/seller_help
specification: FinOps Framework
tags:
- Music
- Marketplace
- Indie
- Audio
- Sales
- Merch
- FinOps
- Cost Management
- FOCUS
---
