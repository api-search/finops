---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: quickbooks-accounting.yml
  format: yaml
  label: QuickBooks Online Accounting API
  slug: quickbooks-accounting
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intuit/refs/heads/main/openapi/quickbooks-accounting.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Subscription + Take Rate
description: 'FOCUS-aligned FinOps for Intuit: free developer access plus end-customer-paid QuickBooks Online subscriptions and pass-through QuickBooks Payments processing fees. Developer cost is dominated by infrastructure to integrate, not Intuit API fees.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Intuit Inc.
  ProviderName: Intuit
  PublisherName: Intuit Inc.
  ServiceCategory: Accounting and Financial Software
  ServiceName: Intuit Developer
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - country
  name: qbo_subscription
  unit: month
- aggregation: sum
  dimensions:
  - card_present
  - card_brand
  name: qbo_payments_card_volume
  unit: USD
- aggregation: sum
  dimensions:
  - channel
  name: qbo_payments_card_count
  unit: transaction
- aggregation: sum
  name: qbo_payments_ach_volume
  unit: USD
- aggregation: sum
  dimensions:
  - api
  - realm
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  dimensions:
  - employees
  name: payroll_run
  unit: payroll_run
name: Intuit Finops
provider_name: Intuit
provider_slug: intuit
publisher_name: Intuit Inc.
service_category: Accounting and Financial Software
slug: intuit-finops
source_filename: intuit-finops.yml
source_heading: FinOps Profile
source_url: https://developer.intuit.com/app/developer/homepage
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Intuit\nproviderId: intuit\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Accounting\n  - Payments\n  - Small Business\ndescription: 'FOCUS-aligned FinOps for Intuit: free developer access plus end-customer-paid QuickBooks\n  Online subscriptions and pass-through QuickBooks Payments processing fees. Developer cost is dominated\n  by infrastructure to integrate, not Intuit API fees.'\nsources:\n  - https://developer.intuit.com/app/developer/homepage\n  - https://quickbooks.intuit.com/pricing/\n  - https://quickbooks.intuit.com/payments/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Intuit Inc.\nserviceCategory: Accounting\
  \ and Financial Software\nbillingModel:\n  pricingCategory: Subscription + Take Rate\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Intuit Developer\n  ServiceCategory: Accounting and Financial Software\n  ProviderName: Intuit\n  PublisherName: Intuit Inc.\n  InvoiceIssuerName: Intuit Inc.\n  BillingCurrency: USD\nmeters:\n  - name: qbo_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - plan\n      - country\n  - name: qbo_payments_card_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - card_present\n      - card_brand\n  - name: qbo_payments_card_count\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - channel\n  - name: qbo_payments_ach_volume\n    unit: USD\n    aggregation: sum\n  - name: api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n  \
  \    - realm\n      - endpoint\n  - name: payroll_run\n    unit: payroll_run\n    aggregation: sum\n    dimensions:\n      - employees\nprinciples:\n  - name: Visibility\n    description: Use the QuickBooks Online Sales endpoints and Reports API to surface pass-through\n      Payments fees; reconcile against Intuit merchant statements monthly.\n  - name: Allocation\n    description: Tag OAuth tokens / app installs by tenant so Payments fees and per-realm API usage\n      can be allocated back to each end-customer or product line.\n  - name: Optimization\n    description: Negotiate QuickBooks Payments rates at scale; use ACH for high-value invoices to lower\n      effective take rate; cache QBO read endpoints to stay under the per-realm 500/min throttle.\n  - name: Accountability\n    description: Designate a developer-relations owner to monitor API throttle incidents; finance owner\n      reconciles QuickBooks Payments fees against Intuit settlement reports.\nmaintainers:\n  - FN: API\
  \ Evangelist\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/intuit/refs/heads/main/finops/intuit-finops.yml
sources:
- https://developer.intuit.com/app/developer/homepage
- https://quickbooks.intuit.com/pricing/
- https://quickbooks.intuit.com/payments/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Accounting
- Payments
- Small Business
---
