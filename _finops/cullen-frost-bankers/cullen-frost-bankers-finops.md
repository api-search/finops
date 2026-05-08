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
  chargeFrequency: Recurring
  pricingCategory: Per-Service Banking Fees
description: 'FOCUS-aligned FinOps for Cullen/Frost Bankers: banking-relationship fees (account, treasury, ACH, wire) per the bank''s schedule rather than API-call metering; no public developer API.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Frost Bank
  PricingCategory: Per-Service Fee
  ProviderName: Cullen/Frost Bankers
  PublisherName: Cullen/Frost Bankers, Inc.
  ServiceCategory: Banking
  ServiceName: Frost Bank
layout: finops
meters:
- aggregation: sum
  description: ACH credits / debits originated through Frost
  dimensions:
  - account
  - entity
  name: ach_transactions
  unit: transaction
- aggregation: sum
  description: Domestic / international wire transfers
  dimensions:
  - account
  - direction
  name: wire_transfers
  unit: wire
- aggregation: sum
  description: Maintenance and treasury services billed via account analysis
  dimensions:
  - account
  name: account_analysis_fees
  unit: month
name: Cullen Frost Bankers Finops
provider_name: Cullen/Frost Bankers
provider_slug: cullen-frost-bankers
publisher_name: Cullen/Frost Bankers, Inc.
service_category: Banking
slug: cullen-frost-bankers-finops
source_filename: cullen-frost-bankers-finops.yml
source_heading: FinOps Profile
source_url: https://www.frostbank.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cullen/Frost Bankers\nproviderId: cullen-frost-bankers\npublisherName: Cullen/Frost Bankers, Inc.\nserviceCategory: Banking\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Banking\n  - Financial Services\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Cullen/Frost Bankers: banking-relationship fees (account, treasury,\n  ACH, wire) per the bank''s schedule rather than API-call metering; no public developer API.'\nsources:\n  - https://www.frostbank.com/\nnotes: No public API or API pricing. Reconcile against the bank's customer fee schedule.\nprinciples:\n  - name: Visibility\n    description: Use Frost's\
  \ commercial banking statements and treasury reports to see fee categories\n      and transaction counts.\n  - name: Allocation\n    description: Tag accounts / sub-accounts by entity / cost-center for chargeback of treasury and ACH\n      activity.\n  - name: Optimization\n    description: Right-size accounts / services to match transaction volume; consolidate ACH batches;\n      eliminate unused treasury services at quarterly relationship review.\n  - name: Accountability\n    description: Treasury / finance owns the banking relationship; review monthly account analysis statements\n      for fee drift.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Allocation\n      - Reporting and Analytics\n  - name: Quantify Business Value\n    capabilities:\n      - Forecasting\n      - Budgeting\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Rate Optimization\n  - name: Manage the FinOps Practice\n    capabilities:\n      - Invoicing and Chargeback\nbillingModel:\n\
  \  pricingCategory: Per-Service Banking Fees\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Frost Bank\n  ServiceCategory: Banking\n  ProviderName: Cullen/Frost Bankers\n  PublisherName: Cullen/Frost Bankers, Inc.\n  InvoiceIssuerName: Frost Bank\n  PricingCategory: Per-Service Fee\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: ach_transactions\n    description: ACH credits / debits originated through Frost\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - account\n      - entity\n  - name: wire_transfers\n    description: Domestic / international wire transfers\n    unit: wire\n    aggregation: sum\n    dimensions:\n      - account\n      - direction\n  - name: account_analysis_fees\n    description: Maintenance and treasury services billed via account analysis\n    unit: month\n    aggregation: sum\n    dimensions:\n\
  \      - account\napis:\n  - name: Cullen/Frost Bankers API\n    baseURL: https://api.cullenfrost.com\n    tags:\n      - Banking\n      - Financial Services\n      - Texas\n    serviceName: Cullen/Frost Bankers API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per ACH Transaction\n    metric: billed_cost / ach_transactions\n    target: TBD\n  - name: Cost per Account\n    metric: billed_cost / accounts\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cullen-frost-bankers/refs/heads/main/finops/cullen-frost-bankers-finops.yml
sources:
- https://www.frostbank.com/
specification: FinOps Framework
tags:
- Banking
- Financial Services
- FinOps
- FOCUS
---
