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
  - Refund
  chargeFrequency: Recurring
  pricingCategory: Take Rate + Flat (per merchant agreement)
description: FOCUS-aligned FinOps stub for Heartland Payment Systems. Take-rate + per-transaction billing through Global Payments; rates negotiated per merchant agreement.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Global Payments Inc.
  PricingCategory: Take Rate
  PricingUnit: transaction
  ProviderName: Heartland Payment Systems
  PublisherName: Global Payments Inc.
  ServiceCategory: Payments
  ServiceName: Heartland Payment Systems
layout: finops
meters:
- aggregation: sum
  description: Authorized card transactions processed through Heartland
  dimensions:
  - merchant_id
  - mid
  - card_brand
  - channel
  - country
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Gross dollar volume of processed transactions
  dimensions:
  - merchant_id
  - card_brand
  - channel
  name: transaction_volume
  unit: USD
- aggregation: sum
  description: Chargeback events; surcharge applies per the merchant agreement
  dimensions:
  - merchant_id
  - reason_code
  name: chargebacks
  unit: event
- aggregation: sum
  description: Refund events
  dimensions:
  - merchant_id
  name: refunds
  unit: event
- aggregation: sum
  description: Gift / loyalty card activity (issuance, reload, redemption)
  dimensions:
  - merchant_id
  - program
  name: gift_loyalty_activity
  unit: event
- aggregation: sum
  description: Heartland payroll run events
  dimensions:
  - merchant_id
  name: payroll_runs
  unit: run
name: Heartland Payment Systems Finops
provider_name: Heartland Payment Systems
provider_slug: heartland-payment-systems
publisher_name: Global Payments Inc. (Heartland brand)
service_category: Payments
slug: heartland-payment-systems-finops
source_filename: heartland-payment-systems-finops.yml
source_heading: FinOps Profile
source_url: https://www.heartland.us/payments
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Heartland Payment Systems\nproviderId: heartland-payment-systems\npublisherName: Global Payments Inc. (Heartland brand)\nserviceCategory: Payments\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Payments\n  - Payment Processing\n  - Card Present\n  - Ecommerce\n  - Payroll\n  - FinOps\n  - FOCUS\nnotes: Heartland Payment Systems sells merchant processing on a quote basis - no public price book is\n  available. The FinOps shape is take-rate (per-transaction percentage + flat) plus optional subscription\n  add-ons (gift/loyalty, payroll), but the actual rates are bilateral. Meters below are the right shape;\n  the price column is intentionally left as 'see merchant\
  \ agreement'.\ndescription: 'FOCUS-aligned FinOps stub for Heartland Payment Systems. Take-rate + per-transaction billing\n  through Global Payments; rates negotiated per merchant agreement.'\nsources:\n  - https://www.heartland.us/payments\n  - https://developer.globalpayments.com/\nbillingModel:\n  pricingCategory: Take Rate + Flat (per merchant agreement)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Heartland Payment Systems\n  ServiceCategory: Payments\n  ProviderName: Heartland Payment Systems\n  PublisherName: Global Payments Inc.\n  InvoiceIssuerName: Global Payments Inc.\n  PricingCategory: Take Rate\n  PricingUnit: transaction\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Use Heartland's merchant portal and the Portico Gateway reporting endpoints to track\n     \
  \ authorizations, captures, refunds, and chargebacks; reconcile against the monthly merchant statement.\n  - name: Allocation\n    description: Tag transactions with merchant location, channel (card-present vs e-commerce), and\n      product line via ClientTransactionId / TagData fields so revenue and fee can be attributed downstream.\n  - name: Optimization\n    description: Cost levers are merchant-agreement-level - renegotiate at volume tiers, route appropriate\n      traffic to lower-cost interchange categories (e.g. Level II/III data on commercial cards), and\n      minimize chargebacks through 3DS / fraud screening to avoid fee surcharges.\n  - name: Accountability\n    description: Assign a treasury / finance owner who reconciles statements monthly, owns chargeback\n      response, and renegotiates rates at thresholds defined in the merchant agreement.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n      -\
  \ Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nmeters:\n  - name: card_transactions\n    description: Authorized card transactions processed through Heartland\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - mid\n      - card_brand\n      - channel\n      - country\n  - name: transaction_volume\n    description: Gross dollar volume of processed transactions\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - card_brand\n      - channel\n  - name: chargebacks\n    description: Chargeback events; surcharge\
  \ applies per the merchant agreement\n    unit: event\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - reason_code\n  - name: refunds\n    description: Refund events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - merchant_id\n  - name: gift_loyalty_activity\n    description: Gift / loyalty card activity (issuance, reload, redemption)\n    unit: event\n    aggregation: sum\n    dimensions:\n      - merchant_id\n      - program\n  - name: payroll_runs\n    description: Heartland payroll run events\n    unit: run\n    aggregation: sum\n    dimensions:\n      - merchant_id\napis:\n  - name: Heartland Portico Gateway API\n    baseURL: ''\n    tags:\n      - Payments\n      - Card Present\n      - Card Not Present\n    serviceName: Heartland Portico Gateway API\n    serviceCategory: Payments\n  - name: Heartland Card Present API\n    baseURL: ''\n    tags:\n      - Payments\n      - Card Present\n      - Point of Sale\n    serviceName: Heartland Card Present\
  \ API\n    serviceCategory: Payments\n  - name: Heartland Bill Pay API\n    baseURL: ''\n    tags:\n      - Bill Pay\n      - Payments\n    serviceName: Heartland Bill Pay API\n    serviceCategory: Payments\n  - name: Heartland Gift and Loyalty API\n    baseURL: ''\n    tags:\n      - Gift\n      - Loyalty\n    serviceName: Heartland Gift and Loyalty API\n    serviceCategory: Payments\n  - name: Heartland Payroll API\n    baseURL: ''\n    tags:\n      - Payroll\n    serviceName: Heartland Payroll API\n    serviceCategory: Payments\nunitEconomics:\n  - name: Effective Take Rate\n    metric: total_processing_fees / transaction_volume\n    target: per merchant agreement\n  - name: Cost per Transaction\n    metric: total_processing_fees / card_transactions\n    target: per merchant agreement\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/heartland-payment-systems/refs/heads/main/finops/heartland-payment-systems-finops.yml
sources:
- https://www.heartland.us/payments
- https://developer.globalpayments.com/
specification: FinOps Framework
tags:
- Payments
- Payment Processing
- Card Present
- Ecommerce
- Payroll
- FinOps
- FOCUS
---
