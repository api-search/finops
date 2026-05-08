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
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps framing for Glacier Bancorp partner integrations. Glacier Bancorp does not publish a self-service API price list; partner cost is governed by treasury management agreements and bilateral contracts.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Glacier Bancorp, Inc.
  ProviderName: Glacier Bancorp
  PublisherName: Glacier Bancorp, Inc.
  ServiceCategory: Banking
  ServiceName: Glacier Bancorp
layout: finops
meters:
- aggregation: sum
  description: Account inquiry / balance API calls (when available via partner integration)
  name: account_inquiries
  unit: request
- aggregation: sum
  description: ACH originations and returns
  name: ach_transactions
  unit: transaction
- aggregation: sum
  description: Wire transfer originations
  name: wire_transactions
  unit: transaction
- aggregation: sum
  description: Treasury management or partner-program flat monthly fee
  name: monthly_service_fee
  unit: month
name: Glacier Bancorp Finops
provider_name: Glacier Bancorp
provider_slug: glacier-bancorp
publisher_name: Glacier Bancorp, Inc.
service_category: Banking
slug: glacier-bancorp-finops
source_filename: glacier-bancorp-finops.yml
source_heading: FinOps Profile
source_url: https://www.glacierbancorp.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Glacier Bancorp\nproviderId: glacier-bancorp\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Financial Services\ndescription: FinOps framing for Glacier Bancorp partner integrations. Glacier Bancorp does not publish\n  a self-service API price list; partner cost is governed by treasury management agreements and bilateral\n  contracts.\nnotes: Reconcile after a public developer program is launched. Meters below describe likely partner-billed\n  units rather than published rates.\nsources:\n  - https://www.glacierbancorp.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Glacier Bancorp, Inc.\nserviceCategory: Banking\n\
  billingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Glacier Bancorp\n  ServiceCategory: Banking\n  ProviderName: Glacier Bancorp\n  PublisherName: Glacier Bancorp, Inc.\n  InvoiceIssuerName: Glacier Bancorp, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: account_inquiries\n    description: Account inquiry / balance API calls (when available via partner integration)\n    unit: request\n    aggregation: sum\n  - name: ach_transactions\n    description: ACH originations and returns\n    unit: transaction\n    aggregation: sum\n  - name: wire_transactions\n    description: Wire transfer originations\n    unit: transaction\n    aggregation: sum\n  - name: monthly_service_fee\n    description: Treasury management or partner-program flat monthly fee\n    unit: month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile\
  \ partner usage against bank-issued treasury management statements and ACH/wire\n      activity reports.\n  - name: Allocation\n    description: Allocate banking-service charges to the legal entity holding the account; tag transactional\n      volume by the originating product/business unit.\n  - name: Optimization\n    description: Negotiate volume tiers in the treasury management contract; consolidate accounts to qualify\n      for relationship pricing.\n  - name: Accountability\n    description: Treasury function owns banking-fee management and reviews bank statement variances monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/glacier-bancorp/refs/heads/main/finops/glacier-bancorp-finops.yml
sources:
- https://www.glacierbancorp.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Financial Services
---
