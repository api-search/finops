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
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Per-Transaction + Subscription (Contract)
description: 'FOCUS-aligned FinOps framing for Change Healthcare (Optum): per-transaction EDI/clearinghouse fees plus contracted clinical interoperability subscriptions.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Optum, Inc.
  ProviderName: Change Healthcare
  PublisherName: Optum, Inc.
  ServiceCategory: Healthcare Data Exchange
  ServiceName: Change Healthcare
layout: finops
meters:
- aggregation: sum
  dimensions:
  - payer
  - tradingPartner
  name: eligibility_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - payer
  name: claim_status_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - payer
  - claimType
  name: claims_submitted
  unit: claim
- aggregation: sum
  name: era_remittances
  unit: remittance
- aggregation: sum
  name: prior_auth_transactions
  unit: transaction
- aggregation: sum
  name: clinical_api_subscription
  unit: month
name: Change Healthcare Finops
provider_name: Change Healthcare
provider_slug: change-healthcare
publisher_name: Optum, Inc. (UnitedHealth Group)
service_category: Healthcare / Data Exchange
slug: change-healthcare-finops
source_filename: change-healthcare-finops.yml
source_heading: FinOps Profile
source_url: https://www.changehealthcare.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Change Healthcare\nproviderId: change-healthcare\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Healthcare\n  - EDI\ndescription: 'FOCUS-aligned FinOps framing for Change Healthcare (Optum): per-transaction EDI/clearinghouse\n  fees plus contracted clinical interoperability subscriptions.'\nnotes: Pricing is contract-based per-transaction; meters reflect typical EDI billing lines.\nsources:\n  - https://www.changehealthcare.com\n  - https://www.optum.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Optum, Inc. (UnitedHealth Group)\nserviceCategory: Healthcare / Data Exchange\nbillingModel:\n  pricingCategory: Per-Transaction\
  \ + Subscription (Contract)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Change Healthcare\n  ServiceCategory: Healthcare Data Exchange\n  ProviderName: Change Healthcare\n  PublisherName: Optum, Inc.\n  InvoiceIssuerName: Optum, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: eligibility_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - payer\n      - tradingPartner\n  - name: claim_status_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - payer\n  - name: claims_submitted\n    unit: claim\n    aggregation: sum\n    dimensions:\n      - payer\n      - claimType\n  - name: era_remittances\n    unit: remittance\n    aggregation: sum\n  - name: prior_auth_transactions\n    unit: transaction\n    aggregation: sum\n  - name: clinical_api_subscription\n    unit: month\n    aggregation: sum\nprinciples:\n\
  \  - name: Visibility\n    description: Use Change Healthcare reporting and EDI 999/277 acknowledgements to track transaction\n      volume; reconcile monthly invoices against transaction counts.\n  - name: Allocation\n    description: Allocate by payer, line of business, and trading partner using EDI metadata.\n  - name: Optimization\n    description: Reduce duplicate eligibility checks via caching, batch claims where supported, and audit\n      rejection rates to lower retransmissions.\n  - name: Accountability\n    description: Revenue cycle / clearinghouse manager owns Change Healthcare invoices; review monthly\n      against payer mix and rejection trends.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/change-healthcare/refs/heads/main/finops/change-healthcare-finops.yml
sources:
- https://www.changehealthcare.com
- https://www.optum.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Healthcare
- EDI
---
