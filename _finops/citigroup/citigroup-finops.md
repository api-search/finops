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
description: FOCUS-aligned FinOps shape for Citi's developer APIs. Cost is driven by Citi's underlying banking, payments, FX, and treasury services - APIs themselves are not separately metered; charges flow from per-transaction wire / ACH / FX fees and account-level service charges in the master cash- management agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Citibank, N.A.
  ProviderName: Citi
  PublisherName: Citibank, N.A.
  ServiceCategory: Banking
  ServiceName: Citigroup
layout: finops
meters:
- aggregation: sum
  description: Wire / ACH / SWIFT payments initiated via CitiConnect / Citi Developer Hub APIs.
  dimensions:
  - rail
  - currency
  - geography
  name: payment_transactions
  unit: transaction
- aggregation: sum
  description: Notional FX volume executed via Citi Velocity APIs.
  dimensions:
  - currency_pair
  - tenor
  name: fx_volume
  unit: notional
- aggregation: max
  description: Monthly account-level service charges (statement reporting, balance reporting, reconciliation files).
  dimensions:
  - account_type
  - geography
  name: account_services
  unit: account-month
- aggregation: sum
  description: API call counts (informational; not directly billed).
  dimensions:
  - api_product
  - environment
  name: api_calls
  unit: request
name: Citigroup Finops
provider_name: Citigroup
provider_slug: citigroup
publisher_name: Citibank, N.A.
service_category: Banking
slug: citigroup-finops
source_filename: citigroup-finops.yml
source_heading: FinOps Profile
source_url: https://developer.citi.com
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citigroup\nproviderId: citigroup\npublisherName: Citibank, N.A.\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - Payments\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Citi's developer APIs. Cost is driven by Citi's underlying\n  banking, payments, FX, and treasury services - APIs themselves are not separately metered; charges\n  flow from per-transaction wire / ACH / FX fees and account-level service charges in the master cash-\n  management agreement.\nnotes: Per-API meters below are placeholders that mirror typical Citi cash-management\
  \ / payments line\n  items. Real billing arrives through bank account analysis statements rather than a developer\n  invoice.\nsources:\n  - https://developer.citi.com\n  - https://www.citibank.com/tts/sa/index.jsp\nbillingModel:\n  pricingCategory: Take Rate + Per-Transaction Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Citigroup\n  ServiceCategory: Banking\n  ProviderName: Citi\n  PublisherName: Citibank, N.A.\n  InvoiceIssuerName: Citibank, N.A.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: payment_transactions\n    description: Wire / ACH / SWIFT payments initiated via CitiConnect / Citi Developer Hub APIs.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - rail\n      - currency\n      - geography\n  - name: fx_volume\n    description: Notional FX volume executed via Citi Velocity APIs.\n    unit: notional\n\
  \    aggregation: sum\n    dimensions:\n      - currency_pair\n      - tenor\n  - name: account_services\n    description: Monthly account-level service charges (statement reporting, balance reporting,\n      reconciliation files).\n    unit: account-month\n    aggregation: max\n    dimensions:\n      - account_type\n      - geography\n  - name: api_calls\n    description: API call counts (informational; not directly billed).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use Citi's Account Analysis (Citi AccountLink / EDI 822) statements and the Citi\n      Developer Hub usage dashboard to track per-product API consumption alongside transaction fees.\n  - name: Allocation\n    description: Tag every API client / app to a Citi account number and business unit so wire / ACH\n      / FX line items can be attributed back to the consuming team.\n  - name: Optimization\n    description:\
  \ Batch low-priority payments to lower per-transaction rails (ACH vs wire), reuse\n      OAuth tokens, and reduce intra-day balance-reporting polling cadence.\n  - name: Accountability\n    description: Treasury operations owns Citi service-fee budgets; partner integration owners are\n      accountable for clean reconciliation and exception management to avoid investigation fees.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citigroup/refs/heads/main/finops/citigroup-finops.yml
sources:
- https://developer.citi.com
- https://www.citibank.com/tts/sa/index.jsp
specification: FinOps Framework
tags:
- Banking
- Financial Services
- Payments
- FinOps
- FOCUS
---
