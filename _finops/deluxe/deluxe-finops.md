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
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Take Rate + Per-Item + Subscription
description: 'FOCUS-aligned FinOps for Deluxe Corporation services: take-rate plus per-item plus subscription blend across payments, treasury, payroll/HR, and marketing/data product lines. No public per-call API fees; cost is driven by underlying merchant or SaaS contract.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Deluxe Corporation
  PricingCategory: Mixed (Take Rate + Per-Item + Subscription)
  PricingUnit: varies
  ProviderName: Deluxe Corporation
  PublisherName: Deluxe Corporation
  ServiceCategory: Payments / Treasury / Business Services
  ServiceName: Deluxe Corporation API
layout: finops
meters:
- aggregation: sum
  description: Card payment transactions processed via Deluxe Payment Exchange
  dimensions:
  - merchant
  - card_brand
  - present
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: ACH origination transactions
  dimensions:
  - merchant
  - sec_code
  name: ach_originations
  unit: transaction
- aggregation: sum
  description: Printed checks, lockbox items, or remittance items processed
  dimensions:
  - merchant
  - product
  name: check_items
  unit: item
- aggregation: max
  description: Payroll / HR module seats
  dimensions:
  - subscription
  name: payroll_seats
  unit: seat
- aggregation: sum
  description: Monthly subscription fees for SaaS modules
  dimensions:
  - subscription
  - product
  name: subscription_fee
  unit: month
name: Deluxe Finops
provider_name: Deluxe Corporation
provider_slug: deluxe
publisher_name: Deluxe Corporation
service_category: Payments / Treasury / Business Services
slug: deluxe-finops
source_filename: deluxe-finops.yml
source_heading: FinOps Profile
source_url: https://www.deluxe.com/payments/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Deluxe Corporation\nproviderId: deluxe\npublisherName: Deluxe Corporation\nserviceCategory: Payments / Treasury / Business Services\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\nnotes: Deluxe is a multi-product business-services provider (payments, payroll/HR, treasury, marketing/data,\n  check services). FinOps shape is mixed take-rate (payments), per-item (check / lockbox / ACH), and SaaS\n  subscription (payroll, HR, promo). Reconcile per merchant agreement when available.\ntags:\n  - Payments\n  - Payroll\n  - Merchant Services\n  - Treasury\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Deluxe Corporation services: take-rate plus per-item plus subscription\n\
  \  blend across payments, treasury, payroll/HR, and marketing/data product lines. No public per-call API\n  fees; cost is driven by underlying merchant or SaaS contract.'\nsources:\n  - https://www.deluxe.com/payments/\n  - https://developer.deluxe.com/\nprinciples:\n  - name: Visibility\n    description: Track Deluxe Payment Exchange transaction volume via merchant statements; reconcile per-item\n      counts (check / lockbox / ACH) against monthly invoices; track SaaS seat counts in payroll / HR\n      portals.\n  - name: Allocation\n    description: Allocate take-rate fees by merchant and product line; allocate per-item fees by department\n      processing the items; allocate SaaS seats by HR cost-center mapping.\n  - name: Optimization\n    description: Tune interchange optimization (Level 2 / Level 3 data) on B2B card transactions, batch\n      ACH origination to minimize per-file fees, prune unused payroll seats, and consolidate check / lockbox\n      volumes.\n  - name: Accountability\n\
  \    description: Treasury owns merchant statements; HR owns payroll subscription costs; marketing owns\n      promotional / data subscriptions. Route invoice anomalies through Deluxe account team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Take Rate + Per-Item + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n \
  \   - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Deluxe Corporation API\n  ServiceCategory: Payments / Treasury / Business Services\n  ProviderName: Deluxe Corporation\n  PublisherName: Deluxe Corporation\n  InvoiceIssuerName: Deluxe Corporation\n  PricingCategory: Mixed (Take Rate + Per-Item + Subscription)\n  PricingUnit: varies\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: card_transactions\n    description: Card payment transactions processed via Deluxe Payment Exchange\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant\n      - card_brand\n      - present\n  - name: ach_originations\n    description: ACH origination transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant\n      - sec_code\n  - name: check_items\n    description: Printed checks, lockbox items, or remittance items processed\n    unit: item\n    aggregation: sum\n\
  \    dimensions:\n      - merchant\n      - product\n  - name: payroll_seats\n    description: Payroll / HR module seats\n    unit: seat\n    aggregation: max\n    dimensions:\n      - subscription\n  - name: subscription_fee\n    description: Monthly subscription fees for SaaS modules\n    unit: month\n    aggregation: sum\n    dimensions:\n      - subscription\n      - product\napis:\n  - name: Deluxe Corporation API\n    baseURL: https://api.deluxe.com\n    tags:\n      - Payments\n      - Payroll\n      - Treasury\n      - Marketing\n    serviceName: Deluxe Corporation API\n    serviceCategory: API\nunitEconomics:\n  - name: Effective Take Rate\n    metric: payments_revenue / payments_volume\n    target: TBD\n  - name: Cost per Item Processed\n    metric: per_item_cost / items_processed\n    target: TBD\n  - name: Cost per Payroll Seat\n    metric: payroll_subscription_cost / payroll_seats\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/deluxe/refs/heads/main/finops/deluxe-finops.yml
sources:
- https://www.deluxe.com/payments/
- https://developer.deluxe.com/
specification: FinOps Framework
tags:
- Payments
- Payroll
- Merchant Services
- Treasury
- FinOps
- FOCUS
---
