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
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Take Rate + Per-Transaction Fees
description: FOCUS-aligned FinOps shape for Citizens Financial Group's developer APIs. Cost is driven by Citizens' underlying commercial banking, payments, treasury, and consumer-data services - APIs themselves are not separately metered; charges flow from per-transaction wire / ACH / RTP fees and account-level service charges.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Citizens Bank, N.A.
  ProviderName: Citizens Financial Group
  PublisherName: Citizens Bank, N.A.
  ServiceCategory: Banking
  ServiceName: Citizens Financial Group
layout: finops
meters:
- aggregation: sum
  description: ACH / Wire / RTP payments initiated via Citizens APIs.
  dimensions:
  - rail
  - direction
  - geography
  name: payment_transactions
  unit: transaction
- aggregation: sum
  description: Buy Now Pay Later financed volume routed through Citizens partner APIs.
  dimensions:
  - merchant
  - product
  name: bnpl_volume
  unit: notional
- aggregation: max
  description: Monthly account-level service charges (statement reporting, balance reporting).
  dimensions:
  - account_type
  name: account_services
  unit: account-month
- aggregation: sum
  description: API call counts (informational; not directly billed).
  dimensions:
  - api_product
  - environment
  name: api_calls
  unit: request
name: Citizens Financial Group Finops
provider_name: Citizens Financial Group
provider_slug: citizens-financial-group
publisher_name: Citizens Bank, N.A.
service_category: Banking
slug: citizens-financial-group-finops
source_filename: citizens-financial-group-finops.yml
source_heading: FinOps Profile
source_url: https://www.citizensbank.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citizens Financial Group\nproviderId: citizens-financial-group\npublisherName: Citizens Bank, N.A.\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - Payments\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Citizens Financial Group's developer APIs. Cost is driven\n  by Citizens' underlying commercial banking, payments, treasury, and consumer-data services - APIs\n  themselves are not separately metered; charges flow from per-transaction wire / ACH / RTP fees and\n  account-level service charges.\nnotes: Per-API meters below are placeholders\
  \ that mirror typical commercial banking and BNPL line\n  items.\nsources:\n  - https://www.citizensbank.com\nbillingModel:\n  pricingCategory: Take Rate + Per-Transaction Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Citizens Financial Group\n  ServiceCategory: Banking\n  ProviderName: Citizens Financial Group\n  PublisherName: Citizens Bank, N.A.\n  InvoiceIssuerName: Citizens Bank, N.A.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: payment_transactions\n    description: ACH / Wire / RTP payments initiated via Citizens APIs.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - rail\n      - direction\n      - geography\n  - name: bnpl_volume\n    description: Buy Now Pay Later financed volume routed through Citizens partner APIs.\n    unit: notional\n    aggregation: sum\n    dimensions:\n      - merchant\n    \
  \  - product\n  - name: account_services\n    description: Monthly account-level service charges (statement reporting, balance reporting).\n    unit: account-month\n    aggregation: max\n    dimensions:\n      - account_type\n  - name: api_calls\n    description: API call counts (informational; not directly billed).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use Citizens commercial account-analysis statements, FDX consent dashboards, and the\n      developer portal usage view to track API consumption alongside transaction fees.\n  - name: Allocation\n    description: Tag every API client to a Citizens account, partner, and business unit so wire / ACH /\n      BNPL line items can be attributed back to the consuming team.\n  - name: Optimization\n    description: Route low-priority payments through ACH instead of wire, batch FDX consumer-data\n      pulls during off-peak windows,\
  \ and reuse OAuth tokens.\n  - name: Accountability\n    description: Treasury operations owns Citizens service-fee budgets; partner-integration owners\n      are accountable for clean reconciliation, FDX consent posture, and exception management.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citizens-financial-group/refs/heads/main/finops/citizens-financial-group-finops.yml
sources:
- https://www.citizensbank.com
specification: FinOps Framework
tags:
- Banking
- Financial Services
- Payments
- FinOps
- FOCUS
---
