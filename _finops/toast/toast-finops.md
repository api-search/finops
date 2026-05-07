---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: toast-orders-openapi.yaml
  format: yaml
  label: Toast Orders API
  slug: toast-orders
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-orders-openapi.yaml
- filename: toast-menus-openapi.yaml
  format: yaml
  label: Toast Menus API
  slug: toast-menus
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-menus-openapi.yaml
- filename: toast-labor-openapi.yaml
  format: yaml
  label: Toast Labor API
  slug: toast-labor
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-labor-openapi.yaml
- filename: toast-restaurants-openapi.yaml
  format: yaml
  label: Toast Restaurants API
  slug: toast-restaurants
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-restaurants-openapi.yaml
- filename: toast-stock-openapi.yaml
  format: yaml
  label: Toast Stock API
  slug: toast-stock
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-stock-openapi.yaml
- filename: toast-partners-openapi.yaml
  format: yaml
  label: Toast Partners API
  slug: toast-partners
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-partners-openapi.yaml
- filename: toast-authentication-openapi.yaml
  format: yaml
  label: Toast Authentication API
  slug: toast-authentication
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/openapi/toast-authentication-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Subscription + Take Rate + Hardware
description: 'FinOps shape for Toast: a hybrid POS subscription + payment processing take-rate + hardware purchase model, with API access bundled into the partner relationship. Specific dollar amounts and meter rates are sales-led and not exposed publicly, so this artifact captures the structure rather than reconciled rates.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Toast, Inc.
  ProviderName: Toast
  PublisherName: Toast, Inc.
  ServiceCategory: Restaurant POS & Payments
  ServiceName: Toast
layout: finops
meters:
- aggregation: sum
  description: Per-restaurant Toast POS software subscription billed monthly.
  dimensions:
  - location
  - package
  name: pos_software_subscription
  unit: location-month
- aggregation: sum
  description: Card-present and card-not-present transactions processed through Toast Payments. Take rate is configured per merchant.
  dimensions:
  - location
  - card_present
  - card_brand
  name: card_transactions
  unit: transaction
- aggregation: count
  description: One-time purchase of POS hardware (terminals, KDS, handhelds, peripherals).
  dimensions:
  - device_type
  - location
  name: hardware_purchase
  unit: device
name: Toast Finops
provider_name: Toast
provider_slug: toast
publisher_name: Toast, Inc.
service_category: Restaurant POS & Payments
slug: toast-finops
source_filename: toast-finops.yml
source_heading: FinOps Profile
source_url: https://pos.toasttab.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Toast\nproviderId: toast\npublisherName: Toast, Inc.\nserviceCategory: Restaurant POS & Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Food Service\n  - Point of Sale\n  - Restaurants\n  - Hospitality\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Toast: a hybrid POS subscription + payment processing take-rate + hardware\n  purchase model, with API access bundled into the partner relationship. Specific dollar amounts and meter\n  rates are sales-led and not exposed publicly, so this artifact captures the structure rather than reconciled\n  rates.'\nsources:\n  - https://pos.toasttab.com/\nnotes: Public\
  \ pricing pages returned 403 to WebFetch; rates and per-meter prices are not reconcilable\n  without a Toast quote. Meters described here are structural (what Toast bills on), not priced.\nbillingModel:\n  pricingCategory: Subscription + Take Rate + Hardware\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Toast\n  ServiceCategory: Restaurant POS & Payments\n  ProviderName: Toast\n  PublisherName: Toast, Inc.\n  InvoiceIssuerName: Toast, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: pos_software_subscription\n    description: Per-restaurant Toast POS software subscription billed monthly.\n    unit: location-month\n    aggregation: sum\n    dimensions:\n      - location\n      - package\n  - name: card_transactions\n    description: Card-present and card-not-present transactions processed through Toast Payments. Take\n      rate is configured per merchant.\n\
  \    unit: transaction\n    aggregation: sum\n    dimensions:\n      - location\n      - card_present\n      - card_brand\n  - name: hardware_purchase\n    description: One-time purchase of POS hardware (terminals, KDS, handhelds, peripherals).\n    unit: device\n    aggregation: count\n    dimensions:\n      - device_type\n      - location\nprinciples:\n  - name: Visibility\n    description: Pull the Toast invoice and Sales Summary reports per location; reconcile software fees,\n      processing fees, and hardware lines separately because they have different optimization levers.\n  - name: Allocation\n    description: Allocate fees to the operating restaurant location; multi-location operators can roll\n      up by brand or region using Toast's multi-location reporting.\n  - name: Optimization\n    description: Negotiate processing rates at scale, right-size hardware fleets per location, and audit\n      software add-ons (online ordering, marketing) against active usage at each renewal.\n\
  \  - name: Accountability\n    description: GM or operations director per location owns the Toast bill; corporate finance owns the\n      processing-rate negotiation for multi-location operators.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/toast/refs/heads/main/finops/toast-finops.yml
sources:
- https://pos.toasttab.com/
specification: FinOps Framework
tags:
- Food Service
- Point of Sale
- Restaurants
- Hospitality
- FinOps
- FOCUS
---
