---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: jpmorgan-chase-jpmorgan-api-openapi.yml
  format: yaml
  label: JPMorgan Chase API
  slug: jpmorgan-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/jpmorgan-chase/refs/heads/main/openapi/jpmorgan-chase-jpmorgan-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  - Refund
  pricingCategory: Per-Transaction + Negotiated
description: FOCUS-aligned FinOps scaffold for JPMorgan Chase Payments / Treasury / Embedded Banking APIs. Treated as a per-transaction banking model with negotiated client pricing.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: JPMorgan Chase Bank, N.A.
  ProviderName: JPMorgan Chase
  PublisherName: JPMorgan Chase Bank, N.A.
  ServiceCategory: Banking / Payments
  ServiceName: JPMorgan Chase Payments APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  - direction
  - sec_code
  name: ach_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - account
  - currency
  - direction
  name: wire_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - account
  - direction
  name: rtp_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - account
  - card_brand
  - mcc
  name: card_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - product
  - account
  name: api_requests
  unit: request
name: Jpmorgan Chase Finops
provider_name: JPMorgan Chase
provider_slug: jpmorgan-chase
publisher_name: JPMorgan Chase Bank, N.A.
service_category: Banking / Payments
slug: jpmorgan-chase-finops
source_filename: jpmorgan-chase-finops.yml
source_heading: FinOps Profile
source_url: https://www.jpmorgan.com/payments
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: JPMorgan Chase\nproviderId: jpmorgan-chase\npublisherName: JPMorgan Chase Bank, N.A.\nserviceCategory: Banking / Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: JPMorgan Chase does not expose a public usage-billing API for its developer /\n  Payments surface. FinOps shape inferred from a per-transaction banking model. Meters\n  list common payment-class billable units; replace with the contract-specific invoice\n  line items.\ntags:\n  - Banking\n  - Embedded Finance\n  - Financial Services\n  - Payments\n  - Treasury\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps scaffold for JPMorgan Chase Payments\
  \ / Treasury / Embedded\n  Banking APIs. Treated as a per-transaction banking model with negotiated client pricing.\nsources:\n  - https://www.jpmorgan.com/payments\n  - https://developer.payments.jpmorgan.com/\n  - https://www.finops.org/framework/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Per-Transaction + Negotiated\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: JPMorgan Chase Payments APIs\n  ServiceCategory: Banking / Payments\n  ProviderName: JPMorgan Chase\n  PublisherName: JPMorgan Chase Bank, N.A.\n  InvoiceIssuerName: JPMorgan Chase Bank, N.A.\n  BillingCurrency: USD\nmeters:\n  - name: ach_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n      - direction\n      - sec_code\n  - name: wire_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n  \
  \    - account\n      - currency\n      - direction\n  - name: rtp_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n      - direction\n  - name: card_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n      - card_brand\n      - mcc\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - product\n      - account\nprinciples:\n  - name: Visibility\n    description: Reconcile usage against the monthly J.P. Morgan account analysis statement;\n      developer portal also exposes per-call telemetry for some products.\n  - name: Allocation\n    description: Allocate by account number and product (ACH, Wires, RTP, Card, FX) to\n      mirror account-analysis line items.\n  - name: Optimization\n    description: Right-size between rails (RTP vs ACH vs Wire) for cost-per-payment;\n      reconcile FX margin against quoted rates.\n  - name: Accountability\n    description: Pair\
  \ the J.P. Morgan implementation manager with an internal treasurer /\n      payments product owner; review quarterly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jpmorgan-chase/refs/heads/main/finops/jpmorgan-chase-finops.yml
sources:
- https://www.jpmorgan.com/payments
- https://developer.payments.jpmorgan.com/
- https://www.finops.org/framework/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Banking
- Embedded Finance
- Financial Services
- Payments
- Treasury
- FinOps
- FOCUS
---
