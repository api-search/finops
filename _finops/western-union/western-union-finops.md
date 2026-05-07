---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: western-union-mass-payments-openapi.yml
  format: yaml
  label: Western Union Mass Payments API
  slug: mass-payments
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/western-union/refs/heads/main/openapi/western-union-mass-payments-openapi.yml
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Adjustment
  - Refund
  pricingCategory: Per-Transaction Fee + FX Margin
description: FinOps shape for Western Union is partner-contract-driven - per-payment fees plus FX margin by corridor, no public price list, settled through the partner agreement.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: The Western Union Company
  ProviderName: Western Union
  PublisherName: The Western Union Company
  ServiceCategory: Payments
  ServiceName: Western Union Partner APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - send_country
  - receive_country
  - send_currency
  - receive_currency
  - payout_method
  name: payments_initiated
  unit: transaction
- aggregation: sum
  dimensions:
  - send_currency
  - receive_currency
  - corridor
  name: fx_converted_volume
  unit: send_currency_amount
- aggregation: count
  dimensions:
  - partner
  name: batches_submitted
  unit: batch
name: Western Union Finops
provider_name: western-union
provider_slug: western-union
publisher_name: The Western Union Company
service_category: Payments
slug: western-union-finops
source_filename: western-union-finops.yml
source_heading: FinOps Profile
source_url: https://www.westernunion.com/us/en/business/payments-api.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Western Union\nproviderId: western-union\npublisherName: The Western Union Company\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Money Transfer\n  - Payments\n  - Cross-Border\n  - FinOps\n  - FOCUS\n  - Contact Sales\ndescription: FinOps shape for Western Union is partner-contract-driven - per-payment fees plus FX margin by corridor, no public price list, settled through the partner agreement.\nsources:\n  - https://www.westernunion.com/us/en/business/payments-api.html\nnotes: No public per-call or per-corridor price list. Meters reflect the actual billable shape (payments and FX-converted\
  \ volume) but unit prices live in the partner contract.\nbillingModel:\n  pricingCategory: Per-Transaction Fee + FX Margin\n  billingFrequency: Per-Invoice\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Usage\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Western Union Partner APIs\n  ServiceCategory: Payments\n  ProviderName: Western Union\n  PublisherName: The Western Union Company\n  InvoiceIssuerName: The Western Union Company\n  BillingCurrency: USD\nmeters:\n  - name: payments_initiated\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - send_country\n      - receive_country\n      - send_currency\n      - receive_currency\n      - payout_method\n  - name: fx_converted_volume\n    unit: send_currency_amount\n    aggregation: sum\n    dimensions:\n      - send_currency\n      - receive_currency\n      - corridor\n  - name: batches_submitted\n    unit: batch\n    aggregation: count\n    dimensions:\n      - partner\nprinciples:\n\
  \  - name: Visibility\n    description: Reconcile against the Mass Payments batch responses and partner settlement reports; there is no public billing API.\n  - name: Allocation\n    description: Allocate by corridor (send/receive country pair) and partner account, since fees and FX margins differ per corridor.\n  - name: Optimization\n    description: Optimization levers are corridor selection, payout method (bank vs cash vs wallet), batching, and renegotiating partner FX margins.\n  - name: Accountability\n    description: Treasury / payment-ops owns FX and corridor mix; engineering owns batch reliability and reconciliation accuracy.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/western-union/refs/heads/main/finops/western-union-finops.yml
sources:
- https://www.westernunion.com/us/en/business/payments-api.html
specification: FinOps Framework
tags:
- Money Transfer
- Payments
- Cross-Border
- FinOps
- FOCUS
- Contact Sales
---
