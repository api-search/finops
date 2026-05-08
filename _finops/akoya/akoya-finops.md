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
  - Subscription
  - Usage
  - Adjustment
  pricingCategory: Custom Network Contract
description: FinOps view of Akoya. Network-membership commercial model. Cost lines are network membership, per-call / per-consumer fees on the recipient side, and reciprocal fee schedules on the data-provider side. FDX-standard data shape eases consumer migration between providers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Akoya LLC
  ProviderName: Akoya LLC
  PublisherName: Akoya LLC
  ServiceCategory: Open Banking
  ServiceName: Akoya Data Access Network
layout: finops
meters:
- aggregation: sum
  description: Network membership subscription.
  dimensions:
  - client
  name: network_membership
  unit: month
- aggregation: sum
  description: Per-call usage fee.
  dimensions:
  - client
  - data_provider
  name: api_call
  unit: call
- aggregation: count_distinct
  description: Per consented consumer fee.
  dimensions:
  - end_user
  name: consented_consumer
  unit: consumer_month
name: Akoya Finops
provider_name: Akoya
provider_slug: akoya
publisher_name: Akoya LLC
service_category: Open Banking
slug: akoya-finops
source_filename: akoya-finops.yml
source_heading: FinOps Profile
source_url: https://akoya.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Akoya\nproviderId: akoya\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Open Banking\n  - US\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Akoya. Network-membership commercial model. Cost lines are network membership,\n  per-call / per-consumer fees on the recipient side, and reciprocal fee schedules on the\n  data-provider side. FDX-standard data shape eases consumer migration between providers.\nsources:\n  - https://akoya.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Akoya LLC\nserviceCategory: Open Banking\nbillingModel:\n  pricingCategory: Custom Network Contract\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: Akoya Data Access Network\n  ServiceCategory: Open Banking\n  ProviderName: Akoya LLC\n  PublisherName: Akoya LLC\n  InvoiceIssuerName: Akoya LLC\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: network_membership\n    description: Network membership subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - client\n  - name: api_call\n    description: Per-call usage fee.\n    unit: call\n    aggregation: sum\n    dimensions:\n      - client\n      - data_provider\n  - name: consented_consumer\n    description: Per consented consumer fee.\n    unit: consumer_month\n    aggregation: count_distinct\n    dimensions:\n      - end_user\nprinciples:\n  - name: Visibility\n    description: Track per-data-provider call volume; reconcile against recipient invoice.\n  - name: Allocation\n    description: Allocate per\
  \ consuming product; tag end-user IDs per cost center.\n  - name: Optimization\n    description: Cache infrequently changing endpoints (e.g. account details); reduce Transactions polls.\n  - name: Accountability\n    description: Assign a billing owner; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/akoya/refs/heads/main/finops/akoya-finops.yml
sources:
- https://akoya.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Open Banking
- US
- FinOps
- FOCUS
---
