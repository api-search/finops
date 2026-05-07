---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: yodlee-core-openapi.yml
  format: yaml
  label: Yodlee Core API
  slug: yodlee-core-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/yodlee/refs/heads/main/openapi/yodlee-core-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Per-Invoice
  chargeCategories:
  - Usage
  - Purchase
  pricingCategory: Contact Sales
description: 'Yodlee''s commercial model is a sales-negotiated B2B contract; this artifact is a

  Contact Sales placeholder pending the customer''s master agreement.

  '
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Yodlee, Inc.
  ProviderName: Yodlee
  PublisherName: Yodlee, Inc.
  ServiceCategory: Financial Data Aggregation
  ServiceName: Yodlee
layout: finops
meters:
- aggregation: count
  description: Aggregated end-user financial accounts under the cobrand; commonly the primary commercial unit on Yodlee invoices.
  name: linked_accounts
  unit: account
- aggregation: sum
  description: API call volume (FastLink / Aggregation / Verification / Transactions); priced per the cobrand agreement.
  name: api_calls
  unit: request
name: Yodlee Finops
provider_name: Yodlee
provider_slug: yodlee
publisher_name: Yodlee, Inc.
service_category: Financial Data Aggregation
slug: yodlee-finops
source_filename: yodlee-finops.yml
source_heading: FinOps Profile
source_url: https://www.yodlee.com/products
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Yodlee\nproviderId: yodlee\npublisherName: Yodlee, Inc.\nserviceCategory: Financial Data Aggregation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Data\n  - Data Aggregation\n  - FinOps\n  - FOCUS\ndescription: |\n  Yodlee's commercial model is a sales-negotiated B2B contract; this artifact is a\n  Contact Sales placeholder pending the customer's master agreement.\nsources:\n  - https://www.yodlee.com/products\nnotes: |\n  Yodlee does not publish per-meter pricing publicly. Meter and FOCUS column values\n  below are minimal placeholders pending the signed Yodlee data-services agreement.\nbillingModel:\n \
  \ pricingCategory: Contact Sales\n  billingFrequency: Per-Invoice\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\nfocusColumns:\n  ServiceName: Yodlee\n  ServiceCategory: Financial Data Aggregation\n  ProviderName: Yodlee\n  PublisherName: Yodlee, Inc.\n  InvoiceIssuerName: Yodlee, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: linked_accounts\n    description: Aggregated end-user financial accounts under the cobrand; commonly the\n      primary commercial unit on Yodlee invoices.\n    unit: account\n    aggregation: count\n  - name: api_calls\n    description: API call volume (FastLink / Aggregation / Verification / Transactions);\n      priced per the cobrand agreement.\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Visibility comes from cobrand-level reports issued by the Yodlee account\n      team rather than a self-serve usage API.\n  - name: Allocation\n    description: Allocate Yodlee spend by cobrand identifier\
  \ and by downstream product /\n      use case (origination, verification, PFM).\n  - name: Optimization\n    description: Optimize via refresh-cadence policy, MFA / OAuth coverage, and pruning\n      stale linked accounts to reduce billable account counts.\n  - name: Accountability\n    description: Spend ownership sits with the data / risk / lending product owner who\n      signed the Yodlee master agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/yodlee/refs/heads/main/finops/yodlee-finops.yml
sources:
- https://www.yodlee.com/products
specification: FinOps Framework
tags:
- Financial Data
- Data Aggregation
- FinOps
- FOCUS
---
