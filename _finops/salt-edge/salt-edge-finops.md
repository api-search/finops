---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: EUR
  billingFrequency: Monthly
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps view of Salt Edge. Sales-led contracts. Cost is per consented end user (Account Information), per initiated payment (Payment Initiation), or flat-fee SaaS (Compliance Solution and AML).
focus_columns:
  BillingCurrency: EUR
  ChargeCategory: Usage
  InvoiceIssuerName: Salt Edge Inc.
  ProviderName: Salt Edge Inc.
  PublisherName: Salt Edge Inc.
  ServiceCategory: Open Banking
  ServiceName: Salt Edge Open Banking
layout: finops
meters:
- aggregation: count_distinct
  description: Per active consented end user (Account Information).
  dimensions:
  - end_user
  name: consented_user
  unit: user_month
- aggregation: sum
  description: Per initiated payment.
  dimensions:
  - client
  name: payment_initiation
  unit: payment
- aggregation: sum
  description: Compliance Solution flat SaaS subscription.
  dimensions:
  - client
  name: compliance_subscription
  unit: month
name: Salt Edge Finops
provider_name: Salt Edge
provider_slug: salt-edge
publisher_name: Salt Edge Inc.
service_category: Open Banking
slug: salt-edge-finops
source_filename: salt-edge-finops.yml
source_heading: FinOps Profile
source_url: https://www.saltedge.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Salt Edge\nproviderId: salt-edge\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Open Banking\n  - Fintech\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Salt Edge. Sales-led contracts. Cost is per consented end user (Account\n  Information), per initiated payment (Payment Initiation), or flat-fee SaaS (Compliance\n  Solution and AML).\nsources:\n  - https://www.saltedge.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Salt Edge Inc.\nserviceCategory: Open Banking\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency: Monthly\n  billingCurrency: EUR\n  chargeCategories:\n\
  \    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Salt Edge Open Banking\n  ServiceCategory: Open Banking\n  ProviderName: Salt Edge Inc.\n  PublisherName: Salt Edge Inc.\n  InvoiceIssuerName: Salt Edge Inc.\n  BillingCurrency: EUR\n  ChargeCategory: Usage\nmeters:\n  - name: consented_user\n    description: Per active consented end user (Account Information).\n    unit: user_month\n    aggregation: count_distinct\n    dimensions:\n      - end_user\n  - name: payment_initiation\n    description: Per initiated payment.\n    unit: payment\n    aggregation: sum\n    dimensions:\n      - client\n  - name: compliance_subscription\n    description: Compliance Solution flat SaaS subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - client\nprinciples:\n  - name: Visibility\n    description: Track per-product per-event cost; reconcile vendor invoices monthly.\n  - name: Allocation\n    description: Allocate per consuming product line; tag\
  \ end-user IDs to cost center.\n  - name: Optimization\n    description: Reduce unnecessary refreshes; respect SCA cadence; cache categorized signals.\n  - name: Accountability\n    description: Assign a billing owner; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salt-edge/refs/heads/main/finops/salt-edge-finops.yml
sources:
- https://www.saltedge.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Open Banking
- Fintech
- FinOps
- FOCUS
---
