---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cardtonic-openapi.yml
  format: yaml
  label: Cardtonic Gift Card Developer API
  slug: gift-card-developer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cardtonic/refs/heads/main/openapi/cardtonic-openapi.yml
billing_model:
  billingCurrency: NGN / GHS / USD
  billingFrequency: Continuous Settlement
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Take Rate + Custom Merchant Agreement
description: 'FOCUS-aligned FinOps for Cardtonic: per-transaction take rates on gift cards, bill payments, eSIMs, and virtual dollar cards; merchant API access via waitlist with bilateral pricing.'
focus_columns:
  BillingCurrency: NGN
  InvoiceIssuerName: Cardtonic Limited
  ProviderName: Cardtonic
  PublisherName: Cardtonic Limited
  ServiceCategory: Fintech / Gift Cards
  ServiceName: Cardtonic
layout: finops
meters:
- aggregation: sum
  dimensions:
  - direction
  - card_brand
  - country
  name: gift_card_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - biller
  - country
  name: bill_payments
  unit: transaction
- aggregation: sum
  dimensions:
  - currency
  name: virtual_card_issuance
  unit: card
- aggregation: sum
  dimensions:
  - country
  name: esim_purchases
  unit: purchase
name: Cardtonic Finops
provider_name: Cardtonic
provider_slug: cardtonic
publisher_name: Cardtonic Limited
service_category: Fintech / Gift Cards
slug: cardtonic-finops
source_filename: cardtonic-finops.yml
source_heading: FinOps Profile
source_url: https://www.cardtonic.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cardtonic\nproviderId: cardtonic\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Fintech\n  - Gift Cards\n  - Payments\n  - Africa\ndescription: 'FOCUS-aligned FinOps for Cardtonic: per-transaction take rates on gift cards, bill payments,\n  eSIMs, and virtual dollar cards; merchant API access via waitlist with bilateral pricing.'\nnotes: Cardtonic does not publish public API or transaction tariffs. Take rates are quoted in-app at\n  point of sale; reconcile against merchant-onboarding terms when available.\nsources:\n  - https://www.cardtonic.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Cardtonic Limited\nserviceCategory:\
  \ Fintech / Gift Cards\nbillingModel:\n  pricingCategory: Take Rate + Custom Merchant Agreement\n  billingFrequency: Continuous Settlement\n  billingCurrency: NGN / GHS / USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Cardtonic\n  ServiceCategory: Fintech / Gift Cards\n  ProviderName: Cardtonic\n  PublisherName: Cardtonic Limited\n  InvoiceIssuerName: Cardtonic Limited\n  BillingCurrency: NGN\nmeters:\n  - name: gift_card_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - direction\n      - card_brand\n      - country\n  - name: bill_payments\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - biller\n      - country\n  - name: virtual_card_issuance\n    unit: card\n    aggregation: sum\n    dimensions:\n      - currency\n  - name: esim_purchases\n    unit: purchase\n    aggregation: sum\n    dimensions:\n      - country\nprinciples:\n  - name: Visibility\n    description:\
  \ Visibility into per-transaction take rates is via the in-app quote and merchant settlement\n      reports; the consumer app displays NGN/GHS settlement.\n  - name: Allocation\n    description: Allocate by merchant, country, and product family (gift cards vs bills vs eSIMs).\n  - name: Optimization\n    description: Bulk gift-card ordering and merchant-tier negotiation reduce effective take rates; cache\n      catalog data to avoid redundant inventory calls.\n  - name: Accountability\n    description: Merchant operations team owns the relationship; reconcile NGN/GHS settlement against\n      USD card economics monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cardtonic/refs/heads/main/finops/cardtonic-finops.yml
sources:
- https://www.cardtonic.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Fintech
- Gift Cards
- Payments
- Africa
---
