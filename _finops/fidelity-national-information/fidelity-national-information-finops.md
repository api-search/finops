---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (operating fees) + Annual (license / professional services)
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Tax
  chargeFrequency: Recurring
  pricingCategory: Multi-Year Platform Contract + Transaction Volume Tiers
description: 'FOCUS-aligned FinOps for FIS: cost is bundled into multi-year platform contracts covering core banking (Modern Banking Platform, IBS, Profile), payments (Worldpay-from-FIS, FedNow), capital markets, wealth, and risk/compliance products. The Code Connect APIs are entitlements within those contracts rather than a per-call billed product. FinOps focuses on transaction-volume tiering, professional-services spend, and managed-service tier selection rather than API-call meters.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Fidelity National Information Services, Inc.
  PricingCategory: Subscription + Transaction Volume
  PricingUnit: contract | transaction
  ProviderName: FIS
  PublisherName: Fidelity National Information Services, Inc.
  ServiceCategory: Financial Services Technology
  ServiceName: FIS
layout: finops
meters:
- aggregation: sum
  description: Code Connect API call volume per consumer application (where reported).
  dimensions:
  - api
  - application
  - environment
  name: api_calls
  unit: call
- aggregation: sum
  description: Card transactions processed via Worldpay-from-FIS.
  dimensions:
  - merchant
  - card_brand
  - country
  name: card_transactions
  unit: transaction
- aggregation: sum
  description: Real-time / batch payments processed (FedNow, RTP, ACH via FIS).
  dimensions:
  - rail
  - originator
  name: payments
  unit: payment
- aggregation: max
  description: Active deposit / wealth accounts on the FIS platform.
  dimensions:
  - product_module
  name: accounts_under_management
  unit: account
- aggregation: sum
  description: Consumed professional-services hours against the contracted bank.
  dimensions:
  - engagement
  name: professional_services_hours
  unit: hour
name: Fidelity National Information Finops
provider_name: Fidelity National Information Services (FIS)
provider_slug: fidelity-national-information
publisher_name: Fidelity National Information Services, Inc.
service_category: Financial Services Technology
slug: fidelity-national-information-finops
source_filename: fidelity-national-information-finops.yml
source_heading: FinOps Profile
source_url: https://codeconnect.fisglobal.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Fidelity National Information Services (FIS)\nproviderId: fidelity-national-information\npublisherName: Fidelity National Information Services, Inc.\nserviceCategory: Financial Services Technology\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Financial Services\n  - Payments\n  - Banking\n  - Capital Markets\n  - Wealth Management\n  - Risk and Compliance\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for FIS: cost is bundled into multi-year platform contracts covering\n  core banking (Modern Banking Platform, IBS, Profile), payments (Worldpay-from-FIS, FedNow), capital\n  markets, wealth, and risk/compliance products. The Code\
  \ Connect APIs are entitlements within those\n  contracts rather than a per-call billed product. FinOps focuses on transaction-volume tiering, professional-services\n  spend, and managed-service tier selection rather than API-call meters.'\nnotes: FIS publishes no list prices. Reconcile FinOps values from the active FIS product contract and\n  monthly invoice line items.\nsources:\n  - https://codeconnect.fisglobal.com/\n  - https://www.fisglobal.com/\nprinciples:\n  - name: Visibility\n    description: Pull monthly FIS invoices and reconcile against contracted volume tiers; track API call\n      volume in Code Connect developer dashboards (where exposed); track transaction volume in the underlying\n      product (e.g. card transactions in Worldpay reporting, payments in Modern Banking Platform reports).\n  - name: Allocation\n    description: Allocate FIS contract cost by line of business (retail banking, commercial banking, capital\n      markets, wealth) and by contracted module; tag\
  \ API calls by Code Connect application/consumer.\n  - name: Optimization\n    description: Right-size contract volume tiers each annual review; consolidate overlapping FIS products\n      where possible; avoid redundant API integrations across teams; leverage included professional-services\n      hours rather than buying additional engagements.\n  - name: Accountability\n    description: Vendor management / strategic sourcing owns the FIS master agreement; product line owners\n      own per-module consumption; quarterly business reviews with FIS to true up volumes and identify\n      optimization candidates.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n  \
  \  capabilities:\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - Invoicing and Chargeback\n      - Onboarding Workloads\nbillingModel:\n  pricingCategory: Multi-Year Platform Contract + Transaction Volume Tiers\n  billingFrequency: Monthly (operating fees) + Annual (license / professional services)\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Tax\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: FIS\n  ServiceCategory: Financial Services Technology\n  ProviderName: FIS\n  PublisherName: Fidelity National Information Services, Inc.\n  InvoiceIssuerName: Fidelity National Information Services, Inc.\n  PricingCategory: Subscription + Transaction Volume\n  PricingUnit: contract | transaction\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: api_calls\n    description:\
  \ Code Connect API call volume per consumer application (where reported).\n    unit: call\n    aggregation: sum\n    dimensions:\n      - api\n      - application\n      - environment\n  - name: card_transactions\n    description: Card transactions processed via Worldpay-from-FIS.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - merchant\n      - card_brand\n      - country\n  - name: payments\n    description: Real-time / batch payments processed (FedNow, RTP, ACH via FIS).\n    unit: payment\n    aggregation: sum\n    dimensions:\n      - rail\n      - originator\n  - name: accounts_under_management\n    description: Active deposit / wealth accounts on the FIS platform.\n    unit: account\n    aggregation: max\n    dimensions:\n      - product_module\n  - name: professional_services_hours\n    description: Consumed professional-services hours against the contracted bank.\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - engagement\napis:\n  - name:\
  \ FIS Code Connect API Marketplace\n    baseURL: https://codeconnect.fisglobal.com/\n    serviceName: FIS Code Connect API Marketplace\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Card Transaction (Worldpay)\n    metric: card_processing_cost / card_transactions\n    target: contract-dependent\n  - name: Cost per Account / month (Modern Banking Platform)\n    metric: platform_cost / accounts_under_management\n    target: contract-dependent\n  - name: PS Hours Burn vs. Contracted Bank\n    metric: professional_services_hours / contracted_hours\n    target: less than 100% before renewal\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fidelity-national-information/refs/heads/main/finops/fidelity-national-information-finops.yml
sources:
- https://codeconnect.fisglobal.com/
- https://www.fisglobal.com/
specification: FinOps Framework
tags:
- Financial Services
- Payments
- Banking
- Capital Markets
- Wealth Management
- Risk and Compliance
- FinOps
- Cost Management
- FOCUS
---
