---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Contract
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Contract / Partner
description: FinOps framing for Kroger Developer APIs. Public APIs are free-to-register; Partner APIs carry no published per-call pricing and are governed by a partner contract. FOCUS columns reflect Kroger as the publisher and merchant of record for any negotiated commercial terms.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Kroger Co.
  ProviderName: Kroger
  PublisherName: The Kroger Co.
  ServiceCategory: Retail / Grocery
  ServiceName: Kroger Developer APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - api
  - environment
  - application
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - store_id
  - fulfillment_type
  name: order_transactions
  unit: order
- aggregation: sum
  dimensions:
  - location_id
  name: product_lookups
  unit: request
- aggregation: sum
  name: cart_operations
  unit: request
name: Kroger Finops
provider_name: Kroger
provider_slug: kroger
publisher_name: The Kroger Co.
service_category: Retail / Grocery APIs
slug: kroger-finops
source_filename: kroger-finops.yml
source_heading: FinOps Profile
source_url: https://developer.kroger.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kroger\nproviderId: kroger\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Groceries\n  - Retail\n  - Partner API\ndescription: FinOps framing for Kroger Developer APIs. Public APIs are free-to-register; Partner APIs\n  carry no published per-call pricing and are governed by a partner contract. FOCUS columns reflect Kroger\n  as the publisher and merchant of record for any negotiated commercial terms.\nsources:\n  - https://developer.kroger.com/\n  - https://developer.kroger.com/manage/documentation/policies\nnotes: No public unit pricing exists; FinOps shape is contract-driven. Meters describe what an integrator\n  should track internally rather than what Kroger invoices.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Kroger Co.\nserviceCategory: Retail / Grocery APIs\nbillingModel:\n  pricingCategory: Contract / Partner\n  billingFrequency: Per-Contract\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Kroger Developer APIs\n  ServiceCategory: Retail / Grocery\n  ProviderName: Kroger\n  PublisherName: The Kroger Co.\n  InvoiceIssuerName: The Kroger Co.\n  BillingCurrency: USD\nmeters:\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - environment\n      - application\n  - name: order_transactions\n    unit: order\n    aggregation: sum\n    dimensions:\n      - store_id\n      - fulfillment_type\n  - name: product_lookups\n    unit: request\n    aggregation: sum\n    dimensions:\n      - location_id\n  - name: cart_operations\n    unit: request\n    aggregation: sum\nprinciples:\n \
  \ - name: Visibility\n    description: Capture Kroger API call volumes per application and per endpoint; the platform does\n      not expose a usage API, so client-side telemetry is required.\n  - name: Allocation\n    description: Tag outbound API requests with the consuming product line (digital cart, locker, fulfillment)\n      so internal chargeback can be performed against the partner contract.\n  - name: Optimization\n    description: Cache static catalog and location data; batch product lookups; refresh OAuth tokens\n      rather than re-issuing them per call.\n  - name: Accountability\n    description: Partnership owner reviews API call volumes against the partner agreement quarterly to\n      anticipate any renegotiation triggers.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kroger/refs/heads/main/finops/kroger-finops.yml
sources:
- https://developer.kroger.com/
- https://developer.kroger.com/manage/documentation/policies
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Groceries
- Retail
- Partner API
---
