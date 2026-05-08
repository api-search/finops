---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: citizens-bank-accounts-api-openapi.yml
  format: yaml
  label: Citizens Bank Accounts API
  slug: accounts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citizens-financial/refs/heads/main/openapi/citizens-bank-accounts-api-openapi.yml
- filename: citizens-bank-atm-locator-api-openapi.yml
  format: yaml
  label: Citizens Bank ATM Locator API
  slug: atm-locator-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/citizens-financial/refs/heads/main/openapi/citizens-bank-atm-locator-api-openapi.yml
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
description: FOCUS-aligned FinOps shape for Citizens Financial Group's developer APIs. Cost is driven by Citizens' underlying commercial banking, payments, and treasury services - APIs themselves are not separately metered; charges flow from per-transaction wire / ACH / RTP fees and account-level service charges in the master commercial banking agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Citizens Bank, N.A.
  ProviderName: Citizens Financial Group
  PublisherName: Citizens Bank, N.A.
  ServiceCategory: Banking
  ServiceName: Citizens Financial
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
name: Citizens Financial Finops
provider_name: Citizens Financial
provider_slug: citizens-financial
publisher_name: Citizens Bank, N.A.
service_category: Banking
slug: citizens-financial-finops
source_filename: citizens-financial-finops.yml
source_heading: FinOps Profile
source_url: https://www.citizensbank.com/corporate-finance/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Citizens Financial\nproviderId: citizens-financial\npublisherName: Citizens Bank, N.A.\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - Payments\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps shape for Citizens Financial Group's developer APIs. Cost is driven\n  by Citizens' underlying commercial banking, payments, and treasury services - APIs themselves are\n  not separately metered; charges flow from per-transaction wire / ACH / RTP fees and account-level\n  service charges in the master commercial banking agreement.\nnotes: Per-API meters below\
  \ are placeholders that mirror typical commercial banking line items.\nsources:\n  - https://www.citizensbank.com/corporate-finance/\nbillingModel:\n  pricingCategory: Take Rate + Per-Transaction Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Citizens Financial\n  ServiceCategory: Banking\n  ProviderName: Citizens Financial Group\n  PublisherName: Citizens Bank, N.A.\n  InvoiceIssuerName: Citizens Bank, N.A.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: payment_transactions\n    description: ACH / Wire / RTP payments initiated via Citizens APIs.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - rail\n      - direction\n      - geography\n  - name: account_services\n    description: Monthly account-level service charges (statement reporting, balance reporting).\n    unit: account-month\n    aggregation: max\n   \
  \ dimensions:\n      - account_type\n  - name: api_calls\n    description: API call counts (informational; not directly billed).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_product\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use Citizens commercial account-analysis statements and the Citizens developer portal\n      usage dashboard to track API consumption alongside transaction fees.\n  - name: Allocation\n    description: Tag every API client / app to a Citizens account and business unit so payment line\n      items can be attributed back to the consuming team.\n  - name: Optimization\n    description: Route low-priority payments through ACH instead of wire, reuse OAuth tokens, and\n      throttle balance-reporting polling cadence.\n  - name: Accountability\n    description: Treasury operations owns Citizens service-fee budgets; partner integration owners are\n      accountable for clean reconciliation and exception management.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/citizens-financial/refs/heads/main/finops/citizens-financial-finops.yml
sources:
- https://www.citizensbank.com/corporate-finance/
specification: FinOps Framework
tags:
- Banking
- Financial Services
- Payments
- FinOps
- FOCUS
---
