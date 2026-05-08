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
  - Adjustment
  pricingCategory: Custom Contract
description: FinOps view of Kaiko. Sales-led enterprise contracts only. Cost lines are typically a base platform fee plus per-module subscription (REST, Stream, Cloud Delivery, On-chain, Indices). Cloud Delivery may include cloud-marketplace pass-through.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Kaiko
  ProviderName: Kaiko
  PublisherName: Kaiko
  ServiceCategory: Crypto Market Data
  ServiceName: Kaiko Market Data
layout: finops
meters:
- aggregation: sum
  description: Per-module REST subscription.
  dimensions:
  - api_key
  name: rest_subscription
  unit: month
- aggregation: sum
  description: Stream subscription per market or instrument set.
  dimensions:
  - api_key
  name: stream_subscription
  unit: month
name: Kaiko Finops
provider_name: Kaiko
provider_slug: kaiko
publisher_name: Kaiko
service_category: Crypto Market Data
slug: kaiko-finops
source_filename: kaiko-finops.yml
source_heading: FinOps Profile
source_url: https://www.kaiko.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kaiko\nproviderId: kaiko\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Crypto\n  - Market Data\n  - Institutional\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Kaiko. Sales-led enterprise contracts only. Cost lines are typically a base\n  platform fee plus per-module subscription (REST, Stream, Cloud Delivery, On-chain, Indices).\n  Cloud Delivery may include cloud-marketplace pass-through.\nsources:\n  - https://www.kaiko.com/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kaiko\nserviceCategory: Crypto Market Data\nbillingModel:\n  pricingCategory: Custom Contract\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: Kaiko Market Data\n  ServiceCategory: Crypto Market Data\n  ProviderName: Kaiko\n  PublisherName: Kaiko\n  InvoiceIssuerName: Kaiko\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: rest_subscription\n    description: Per-module REST subscription.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\n  - name: stream_subscription\n    description: Stream subscription per market or instrument set.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Track per-module usage; fold cloud-marketplace pass-through into FinOps store.\n  - name: Allocation\n    description: Allocate per module to consuming desk or product.\n  - name: Optimization\n    description: Right-size exchange / instrument coverage at renewal.\n  - name: Accountability\n    description:\
  \ Assign a billing owner; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kaiko/refs/heads/main/finops/kaiko-finops.yml
sources:
- https://www.kaiko.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Crypto
- Market Data
- Institutional
- FinOps
- FOCUS
---
