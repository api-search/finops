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
  pricingCategory: Custom (Partner Contract) + AWS Marketplace Subscription
description: 'FOCUS-aligned FinOps for Carvana''s partner integration surface. Two billing shapes coexist: partner-negotiated contracts for the Partner / Collective APIs (no public per-call price), and an AWS Data Exchange subscription for Carvana Car Sales Data (priced + invoiced through AWS Marketplace).'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Carvana, LLC / Amazon Web Services, Inc.
  ProviderName: Carvana
  PublisherName: Carvana, LLC
  ServiceCategory: Automotive Data
  ServiceName: Carvana Partner / Data APIs
layout: finops
meters:
- aggregation: sum
  dimensions:
  - subscription_key
  - operation
  name: partner_api_requests
  unit: request
- aggregation: count
  dimensions:
  - partner
  - operation
  name: inventory_records_managed
  unit: record
- aggregation: sum
  dimensions:
  - product
  name: data_exchange_subscription
  unit: month
- aggregation: sum
  dimensions:
  - product
  - region
  name: data_exchange_data_delivered
  unit: GB
name: Carvana Finops
provider_name: Carvana
provider_slug: carvana
publisher_name: Carvana, LLC
service_category: Automotive Data + Partner Integration
slug: carvana-finops
source_filename: carvana-finops.yml
source_heading: FinOps Profile
source_url: https://api-developer.carvana.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Carvana\nproviderId: carvana\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Automotive\n  - Partner API\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Carvana''s partner integration surface. Two billing shapes coexist:\n  partner-negotiated contracts for the Partner / Collective APIs (no public per-call price), and an\n  AWS Data Exchange subscription for Carvana Car Sales Data (priced + invoiced through AWS Marketplace).'\nnotes: Partner API pricing is private. AWS Data Exchange listing surfaces actual invoice lines via the\n  AWS Marketplace billing report.\nsources:\n  - https://api-developer.carvana.com/\n  - https://aws.amazon.com/marketplace/pp/prodview-y77x3t6zisn4w\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion:\
  \ '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Carvana, LLC\nserviceCategory: Automotive Data + Partner Integration\nbillingModel:\n  pricingCategory: Custom (Partner Contract) + AWS Marketplace Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Carvana Partner / Data APIs\n  ServiceCategory: Automotive Data\n  ProviderName: Carvana\n  PublisherName: Carvana, LLC\n  InvoiceIssuerName: Carvana, LLC / Amazon Web Services, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: partner_api_requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - subscription_key\n      - operation\n  - name: inventory_records_managed\n    unit: record\n    aggregation: count\n    dimensions:\n      - partner\n      - operation\n  - name: data_exchange_subscription\n    unit: month\n    aggregation: sum\n    dimensions:\n      - product\n\
  \  - name: data_exchange_data_delivered\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - product\n      - region\nprinciples:\n  - name: Visibility\n    description: For Partner API, rely on the per-partner reporting Carvana surfaces during onboarding;\n      for AWS Data Exchange, ingest the AWS Marketplace Billing and CUR reports to see Carvana line\n      items.\n  - name: Allocation\n    description: Tag the AWS Marketplace subscription with the consuming product team; allocate Partner\n      API contract fees to the inventory operations function that owns the Carvana relationship.\n  - name: Optimization\n    description: Batch inventory updates rather than polling; subscribe to AWS Data Exchange revisions\n      only for the regions / data fields needed to avoid paying for unused breadth.\n  - name: Accountability\n    description: Assign a single inventory-operations owner for the Carvana Partner contract and a data-platform\n      owner for the AWS Data Exchange subscription;\
  \ review monthly Marketplace invoices.\nmaintainers:\n  - FN: Kin Lane\n    email: info@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/carvana/refs/heads/main/finops/carvana-finops.yml
sources:
- https://api-developer.carvana.com/
- https://aws.amazon.com/marketplace/pp/prodview-y77x3t6zisn4w
specification: FinOps Framework
tags:
- Automotive
- Partner API
- FinOps
- FOCUS
---
