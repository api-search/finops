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
  - Tax
  - Credit
  pricingCategory: Per-Verification (Custom-Quoted) + Add-Ons
description: FOCUS-aligned FinOps for Jumio. The dominant cost is per-verification consumption against the contracted KYX Platform plan, with optional add-on lines per AML screening lookup, ongoing-monitoring identity-month, risk-signals lookup, and extended-retention or retrieval. The SDKs (web, iOS, Android, React Native, Flutter, Cordova, Java, .NET) are free; cost begins when a backend transaction is created. Most contracts include a minimum monthly commit. Specific per-verification rates and the commit floor are negotiated and not published, so this artifact stays reconciled:false until paired with a real customer contract.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Jumio Corporation
  ProviderName: Jumio
  PublisherName: Jumio Corporation
  ServiceCategory: Identity Verification
  ServiceName: Jumio KYX Platform
layout: finops
meters:
- aggregation: sum
  description: Per-completed ID Verification transaction. Drives the bulk of usage cost.
  dimensions:
  - account_id
  - product_workflow
  - country
  name: id_verification
  unit: verification
- aggregation: sum
  description: Per Document Verification (proof-of-address, supporting documents) transaction.
  dimensions:
  - account_id
  - document_type
  name: document_verification
  unit: verification
- aggregation: sum
  description: Per biometric authentication / selfie reverification (selfie.DONE, Authentication product).
  dimensions:
  - account_id
  - product_workflow
  name: authentication
  unit: authentication
- aggregation: sum
  description: Per AML / sanctions / PEP / adverse-media screening lookup.
  dimensions:
  - account_id
  - watchlist_set
  name: screening
  unit: screening
- aggregation: sum
  description: Per-identity-per-month subscription for ongoing AML monitoring.
  dimensions:
  - account_id
  name: ongoing_monitoring
  unit: monitored_identity_month
- aggregation: sum
  description: Per Risk Signals lookup against the Identity Graph / device / behavioural data.
  dimensions:
  - account_id
  name: risk_signals
  unit: lookup
- aggregation: sum
  description: Subscription line for extended Retrieval / data-retention windows beyond the default term.
  dimensions:
  - account_id
  name: retention_extended
  unit: month
- aggregation: max
  description: Monthly minimum commit; whichever is greater (commit or actual usage) is billed.
  dimensions:
  - account_id
  name: minimum_commit
  unit: month
name: Jumio Finops
provider_name: Jumio
provider_slug: jumio
publisher_name: Jumio Corporation
service_category: Identity Verification
slug: jumio-finops
source_filename: jumio-finops.yml
source_heading: FinOps Profile
source_url: https://www.jumio.com/products/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Jumio\nproviderId: jumio\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n  - KYC\n  - Identity Verification\n  - Biometrics\n  - AML\n  - Fraud Prevention\n  - KYX\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Jumio. The dominant cost is per-verification consumption\n  against the contracted KYX Platform plan, with optional add-on lines per AML\n  screening lookup, ongoing-monitoring identity-month, risk-signals lookup, and\n  extended-retention or retrieval. The SDKs (web, iOS, Android, React Native, Flutter,\n  Cordova, Java, .NET) are free; cost begins when a backend transaction is created.\n  Most contracts include a minimum monthly commit. Specific per-verification rates and\n  the commit floor are negotiated and not published, so this artifact stays\n  reconciled:false until paired with a real customer contract.\n\
  sources:\n  - https://www.jumio.com/products/\n  - https://documentation.jumio.ai/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jumio Corporation\nserviceCategory: Identity Verification\nbillingModel:\n  pricingCategory: Per-Verification (Custom-Quoted) + Add-Ons\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Tax\n    - Credit\nfocusColumns:\n  ServiceName: Jumio KYX Platform\n  ServiceCategory: Identity Verification\n  ProviderName: Jumio\n  PublisherName: Jumio Corporation\n  InvoiceIssuerName: Jumio Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: id_verification\n    description: >-\n      Per-completed ID Verification transaction. Drives the bulk of usage cost.\n    unit: verification\n\
  \    aggregation: sum\n    dimensions:\n      - account_id\n      - product_workflow\n      - country\n  - name: document_verification\n    description: >-\n      Per Document Verification (proof-of-address, supporting documents) transaction.\n    unit: verification\n    aggregation: sum\n    dimensions:\n      - account_id\n      - document_type\n  - name: authentication\n    description: >-\n      Per biometric authentication / selfie reverification (selfie.DONE, Authentication\n      product).\n    unit: authentication\n    aggregation: sum\n    dimensions:\n      - account_id\n      - product_workflow\n  - name: screening\n    description: >-\n      Per AML / sanctions / PEP / adverse-media screening lookup.\n    unit: screening\n    aggregation: sum\n    dimensions:\n      - account_id\n      - watchlist_set\n  - name: ongoing_monitoring\n    description: >-\n      Per-identity-per-month subscription for ongoing AML monitoring.\n    unit: monitored_identity_month\n    aggregation:\
  \ sum\n    dimensions:\n      - account_id\n  - name: risk_signals\n    description: >-\n      Per Risk Signals lookup against the Identity Graph / device / behavioural data.\n    unit: lookup\n    aggregation: sum\n    dimensions:\n      - account_id\n  - name: retention_extended\n    description: >-\n      Subscription line for extended Retrieval / data-retention windows beyond the\n      default term.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - account_id\n  - name: minimum_commit\n    description: >-\n      Monthly minimum commit; whichever is greater (commit or actual usage) is billed.\n    unit: month\n    aggregation: max\n    dimensions:\n      - account_id\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull the Jumio dashboard usage report and reconcile against the per-product\n      meters. Use callback events and the Retrieval API to confirm verification\n      lifecycle counts and avoid double-counting incomplete sessions.\n  - name: Allocation\n\
  \    description: >-\n      Use a customerInternalReference per product or business unit so line-of-business\n      attribution flows through the Jumio invoice. Separate test and production\n      accounts to avoid mixing development volume with billable verifications.\n  - name: Optimization\n    description: >-\n      Move returning users to selfie.DONE / Authentication to skip a full ID\n      Verification cycle. Use Risk Signals as a pre-screen so low-risk customers skip\n      full verification. Avoid creating verification transactions in test or canary\n      flows that would consume the production meter. Negotiate the monthly minimum\n      commit to match steady-state demand.\n  - name: Accountability\n    description: >-\n      Assign a compliance / risk owner per Jumio account. Monitor against the monthly\n      minimum commit and renegotiate add-on inclusion (Screening, Risk Signals,\n      Retention) at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jumio/refs/heads/main/finops/jumio-finops.yml
sources:
- https://www.jumio.com/products/
- https://documentation.jumio.ai/
specification: FinOps Framework
tags:
- KYC
- Identity Verification
- Biometrics
- AML
- Fraud Prevention
- KYX
- FinOps
- FOCUS
---
