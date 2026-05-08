---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Negotiated Contract (Bank Fees)
description: 'FinOps shape for KeyCorp/KeyBank: per-transaction banking fees plus monthly treasury / cash-management charges bundled into the commercial-banking contract. No public API tariff.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: KeyBank N.A.
  ProviderName: KeyCorp
  PublisherName: KeyBank N.A.
  ServiceCategory: Banking
  ServiceName: KeyBank
layout: finops
meters:
- aggregation: sum
  dimensions:
  - account
  - sec_code
  name: ach_originations
  unit: transaction
- aggregation: sum
  dimensions:
  - account
  - direction
  name: wire_transfers
  unit: transaction
- aggregation: sum
  dimensions:
  - account
  name: rtp_payments
  unit: transaction
- aggregation: sum
  dimensions:
  - api
  - account
  name: account_inquiries
  unit: request
- aggregation: sum
  name: account_validations
  unit: request
- aggregation: sum
  name: monthly_service_fee
  unit: month
name: Keycorp Finops
provider_name: KeyCorp
provider_slug: keycorp
publisher_name: KeyBank N.A.
service_category: Banking
slug: keycorp-finops
source_filename: keycorp-finops.yml
source_heading: FinOps Profile
source_url: https://developer.key.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: KeyCorp\nproviderId: keycorp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Commercial Banking\n  - Payments\ndescription: 'FinOps shape for KeyCorp/KeyBank: per-transaction banking fees plus monthly treasury / cash-management\n  charges bundled into the commercial-banking contract. No public API tariff.'\nsources:\n  - https://developer.key.com/\nnotes: KeyBank API consumption fees are not published; they roll up into the treasury-services bank-fee\n  analysis statement. Reconcile from actual customer bank statements when available.\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: KeyBank N.A.\nserviceCategory:\
  \ Banking\nbillingModel:\n  pricingCategory: Negotiated Contract (Bank Fees)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: KeyBank\n  ServiceCategory: Banking\n  ProviderName: KeyCorp\n  PublisherName: KeyBank N.A.\n  InvoiceIssuerName: KeyBank N.A.\n  BillingCurrency: USD\nmeters:\n  - name: ach_originations\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n      - sec_code\n  - name: wire_transfers\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n      - direction\n  - name: rtp_payments\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n  - name: account_inquiries\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - account\n  - name: account_validations\n    unit: request\n    aggregation: sum\n  - name: monthly_service_fee\n    unit: month\n    aggregation: sum\n\
  principles:\n  - name: Visibility\n    description: Pull KeyBank's monthly account-analysis statement (AFP service codes) and reconcile against\n      API-driven payment volume from your treasury-management system.\n  - name: Allocation\n    description: Tag originated payments with internal cost-center metadata so per-business-unit ACH/Wire/RTP\n      activity can be attributed.\n  - name: Optimization\n    description: Route low-urgency disbursements through ACH instead of Wire/RTP; use Account Validation\n      to reduce return/repair fees.\n  - name: Accountability\n    description: Treasury and AP owners review the monthly bank-fee analysis statement, dispute exceptions,\n      and negotiate the next contract cycle on actual API/transaction volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/keycorp/refs/heads/main/finops/keycorp-finops.yml
sources:
- https://developer.key.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Commercial Banking
- Payments
---
