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
  - Refund
  pricingCategory: Negotiated
description: 'FOCUS-aligned FinOps for Green Dot Corporation: no public price book is published for the Arc / BaaS APIs. Cost shape is presumed to be a partner-program contract combining program fees, per-account / per-card fees, transaction interchange share, and movement-of-money fees. Treat this document as a placeholder pending direct reconciliation with a Green Dot program agreement.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Green Dot Corporation
  ProviderName: Green Dot Corporation
  PublisherName: Green Dot Corporation
  ServiceCategory: Banking-as-a-Service / Embedded Finance
  ServiceName: Green Dot Corporation API
layout: finops
meters:
- aggregation: sum
  description: Monthly program / sponsorship fee per partner
  dimensions:
  - program
  name: program_fee
  unit: month
- aggregation: max
  description: Active card accounts under the program
  dimensions:
  - program
  name: active_accounts
  unit: account
- aggregation: sum
  description: Card authorization and clearing transactions
  dimensions:
  - program
  - card_brand
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: ACH / push-to-card / wire transfers initiated through the API
  dimensions:
  - program
  - rail
  name: ach_transfers
  unit: transaction
- aggregation: sum
  description: API calls into Green Dot endpoints (operational metric, not directly billed)
  dimensions:
  - program
  - endpoint
  name: api_requests
  unit: request
name: Green Dot Finops
provider_name: Green Dot Corporation
provider_slug: green-dot
publisher_name: Green Dot Corporation
service_category: Banking-as-a-Service / Embedded Finance
slug: green-dot-finops
source_filename: green-dot-finops.yml
source_heading: FinOps Profile
source_url: https://www.greendot.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Green Dot Corporation\nproviderId: green-dot\npublisherName: Green Dot Corporation\nserviceCategory: Banking-as-a-Service / Embedded Finance\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking-as-a-Service\n  - Fintech\n  - Prepaid Cards\ndescription: 'FOCUS-aligned FinOps for Green Dot Corporation: no public price book is published for\n  the Arc / BaaS APIs. Cost shape is presumed to be a partner-program contract combining program\n  fees, per-account / per-card fees, transaction interchange share, and movement-of-money fees.\n  Treat this document as a placeholder pending direct reconciliation\
  \ with a Green Dot program\n  agreement.'\nnotes: No public pricing or billing documentation. Reconcile against signed partner program\n  agreement when available.\nsources:\n  - https://www.greendot.com\nbillingModel:\n  pricingCategory: Negotiated\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Green Dot Corporation API\n  ServiceCategory: Banking-as-a-Service / Embedded Finance\n  ProviderName: Green Dot Corporation\n  PublisherName: Green Dot Corporation\n  InvoiceIssuerName: Green Dot Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: program_fee\n    description: Monthly program / sponsorship fee per partner\n    unit: month\n    aggregation: sum\n    dimensions:\n      - program\n  - name: active_accounts\n    description: Active card accounts under the program\n    unit: account\n    aggregation: max\n    dimensions:\n      - program\n\
  \  - name: card_transactions\n    description: Card authorization and clearing transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - program\n      - card_brand\n  - name: ach_transfers\n    description: ACH / push-to-card / wire transfers initiated through the API\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - program\n      - rail\n  - name: api_requests\n    description: API calls into Green Dot endpoints (operational metric, not directly billed)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - program\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Track program telemetry — accounts, transactions, ACH movement — through Green\n      Dot's partner reporting and reconcile against monthly program invoices.\n  - name: Allocation\n    description: Tag accounts / cards / transactions with consuming product / sub-program so\n      program-fee and interchange splits roll up to the right business\
  \ owner.\n  - name: Optimization\n    description: Negotiate interchange share at scale; consolidate program-fee SKUs; route\n      transactions through the lower-cost rail (ACH vs card) when possible.\n  - name: Accountability\n    description: Designate a fintech / BaaS owner accountable for the Green Dot program contract,\n      monthly reconciliation, and chargeback / dispute handling.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/green-dot/refs/heads/main/finops/green-dot-finops.yml
sources:
- https://www.greendot.com
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking-as-a-Service
- Fintech
- Prepaid Cards
---
