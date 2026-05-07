---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD (settlement varies)
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Transaction Fees
description: 'FOCUS-aligned FinOps framing for Goldman Sachs institutional API products: Marquee data & analytics subscriptions and Transaction Banking transaction fees. Specific rates are bilateral and not publicly posted.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Goldman Sachs Bank USA
  ProviderName: Goldman Sachs
  PublisherName: The Goldman Sachs Group, Inc.
  ServiceCategory: Banking
  ServiceName: Goldman Sachs
layout: finops
meters:
- aggregation: sum
  description: Marquee data / analytics subscription
  dimensions:
  - product
  - data_set
  name: marquee_subscription
  unit: month
- aggregation: sum
  description: Payment instructions executed via Transaction Banking
  dimensions:
  - rail
  - currency
  name: txb_payments
  unit: transaction
- aggregation: sum
  description: FX execution volume
  dimensions:
  - currency_pair
  name: txb_fx_volume
  unit: USD
- aggregation: sum
  description: Corporate / virtual account maintenance fees
  name: account_maintenance
  unit: account-month
name: Goldman Sachs Finops
provider_name: Goldman Sachs
provider_slug: goldman-sachs
publisher_name: The Goldman Sachs Group, Inc.
service_category: Banking / Capital Markets
slug: goldman-sachs-finops
source_filename: goldman-sachs-finops.yml
source_heading: FinOps Profile
source_url: https://www.goldmansachs.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Goldman Sachs\nproviderId: goldman-sachs\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Banking\n  - Capital Markets\ndescription: 'FOCUS-aligned FinOps framing for Goldman Sachs institutional API products: Marquee data\n  & analytics subscriptions and Transaction Banking transaction fees. Specific rates are bilateral and\n  not publicly posted.'\nnotes: Reconcile once published rate cards exist.\nsources:\n  - https://www.goldmansachs.com/\n  - https://developer.gs.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: The Goldman Sachs Group, Inc.\nserviceCategory: Banking / Capital Markets\nbillingModel:\n  pricingCategory:\
  \ Subscription + Transaction Fees\n  billingFrequency: Monthly\n  billingCurrency: USD (settlement varies)\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Goldman Sachs\n  ServiceCategory: Banking\n  ProviderName: Goldman Sachs\n  PublisherName: The Goldman Sachs Group, Inc.\n  InvoiceIssuerName: Goldman Sachs Bank USA\n  BillingCurrency: USD\nmeters:\n  - name: marquee_subscription\n    description: Marquee data / analytics subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n      - data_set\n  - name: txb_payments\n    description: Payment instructions executed via Transaction Banking\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - rail\n      - currency\n  - name: txb_fx_volume\n    description: FX execution volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - currency_pair\n  - name: account_maintenance\n    description: Corporate / virtual account maintenance\
  \ fees\n    unit: account-month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Reconcile Goldman Sachs invoices and Marquee usage exports against ledger; surface TxB\n      payment volumes via the TxB reporting API.\n  - name: Allocation\n    description: Allocate Marquee subscription cost to the consuming desk; TxB payment fees to the originating\n      product.\n  - name: Optimization\n    description: Right-size Marquee data-set entitlements; route low-value payments to cheaper rails;\n      consolidate accounts to qualify for relationship pricing.\n  - name: Accountability\n    description: Front-office desks own Marquee spend; corporate treasury owns TxB spend; finance reviews\n      monthly statements.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/goldman-sachs/refs/heads/main/finops/goldman-sachs-finops.yml
sources:
- https://www.goldmansachs.com/
- https://developer.gs.com/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Banking
- Capital Markets
---
