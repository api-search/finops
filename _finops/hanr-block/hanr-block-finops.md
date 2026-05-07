---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps placeholder for H&R Block: no public commercial API. Partner integrations are bilaterally contracted; meters describe partner-side allocation across tax-season workloads.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: HRB Tax Group, Inc.
  PricingCategory: Subscription
  PricingUnit: partner-agreement
  ProviderName: H&R Block
  PublisherName: HRB Tax Group, Inc.
  ServiceCategory: Tax Preparation / Financial Services Partner API
  ServiceName: H&R Block API
layout: finops
meters:
- aggregation: sum
  description: Partner-integration request volume (allocation meter)
  dimensions:
  - partner
  - endpoint
  - season
  name: api_requests
  unit: request
- aggregation: sum
  description: Tax documents (W-2, 1099, etc.) imported via partner integrations
  dimensions:
  - partner
  - document_type
  name: tax_documents_imported
  unit: document
name: Hanr Block Finops
provider_name: H&R Block
provider_slug: hanr-block
publisher_name: HRB Tax Group, Inc.
service_category: Tax Preparation / Financial Services Partner API
slug: hanr-block-finops
source_filename: hanr-block-finops.yml
source_heading: FinOps Profile
source_url: https://www.hrblock.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: H&R Block\nproviderId: hanr-block\npublisherName: HRB Tax Group, Inc.\nserviceCategory: Tax Preparation / Financial Services Partner API\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Tax Preparation\n  - Financial Services\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for H&R Block: no public commercial API. Partner\n  integrations are bilaterally contracted; meters describe partner-side allocation across tax-season\n  workloads.'\nnotes: No public commercial model is published. Reconcile against the partner agreement.\nsources:\n  - https://www.hrblock.com/\nprinciples:\n\
  \  - name: Visibility\n    description: Track partner-integration request volume via the H&R Block partner gateway logs;\n      pay particular attention to peak tax-season throughput.\n  - name: Allocation\n    description: Allocate integration cost across partner business lines (employer W-2 imports,\n      fintech partnerships, retail-channel referrals).\n  - name: Optimization\n    description: Cache static reference data; batch tax-document lookups; pre-warm capacity ahead\n      of January–April peak.\n  - name: Accountability\n    description: Designate a partner-program owner; review API utilization quarterly with extra\n      review post-tax-season.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit\
  \ Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: H&R Block API\n  ServiceCategory: Tax Preparation / Financial Services Partner API\n  ProviderName: H&R Block\n  PublisherName: HRB Tax Group, Inc.\n  InvoiceIssuerName: HRB Tax Group, Inc.\n  PricingCategory: Subscription\n  PricingUnit: partner-agreement\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name:\
  \ api_requests\n    description: Partner-integration request volume (allocation meter)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - partner\n      - endpoint\n      - season\n  - name: tax_documents_imported\n    description: Tax documents (W-2, 1099, etc.) imported via partner integrations\n    unit: document\n    aggregation: sum\n    dimensions:\n      - partner\n      - document_type\napis:\n  - name: H&R Block API\n    baseURL: https://api.hrblock.com\n    tags:\n      - Tax Preparation\n      - Financial Services\n    serviceName: H&R Block API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per Tax-Filing Season\n    metric: billed_cost / season\n    target: TBD\n  - name: Cost per Document Imported\n    metric: billed_cost / tax_documents_imported\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hanr-block/refs/heads/main/finops/hanr-block-finops.yml
sources:
- https://www.hrblock.com/
specification: FinOps Framework
tags:
- Tax Preparation
- Financial Services
- FinOps
- Cost Management
- FOCUS
---
