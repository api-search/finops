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
  pricingCategory: Subscription with Metered Allowance (Sunset)
description: IEX Cloud sunset on 2024-08-31. Historical billing was monthly subscription with a message-based allowance (Launch / Grow / Scale / Business). Existing customers were transitioned to refund or alternative providers. This artifact preserves the historical billing model for migration cost comparison.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: IEX Cloud
  ProviderName: IEX Cloud
  PublisherName: IEX Cloud
  ServiceCategory: Fintech
  ServiceName: IEX Cloud Core Data API (sunset)
layout: finops
meters:
- aggregation: sum
  description: Per-call message cost against the monthly allowance.
  dimensions:
  - token
  - endpoint
  name: messages
  unit: message
name: Iex Cloud Finops
provider_name: IEX Cloud
provider_slug: iex-cloud
publisher_name: IEX Cloud (IEX Group)
service_category: Fintech
slug: iex-cloud-finops
source_filename: iex-cloud-finops.yml
source_heading: FinOps Profile
source_url: https://iexcloud.io/community/blog/iex-cloud-end-of-life-announcement
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: IEX Cloud\nproviderId: iex-cloud\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Fintech\n  - Market Data\n  - Sunset\n  - FinOps\n  - FOCUS\ndescription: >-\n  IEX Cloud sunset on 2024-08-31. Historical billing was monthly subscription with a message-based\n  allowance (Launch / Grow / Scale / Business). Existing customers were transitioned to refund or\n  alternative providers. This artifact preserves the historical billing model for migration cost\n  comparison.\nsources:\n  - https://iexcloud.io/community/blog/iex-cloud-end-of-life-announcement\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ IEX Cloud (IEX Group)\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory: Subscription with Metered Allowance (Sunset)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: IEX Cloud Core Data API (sunset)\n  ServiceCategory: Fintech\n  ProviderName: IEX Cloud\n  PublisherName: IEX Cloud\n  InvoiceIssuerName: IEX Cloud\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: messages\n    description: Per-call message cost against the monthly allowance.\n    unit: message\n    aggregation: sum\n    dimensions:\n      - token\n      - endpoint\nprinciples:\n  - name: Visibility\n    description: Service sunset; only historical invoices apply.\n  - name: Allocation\n    description: Allocate any residual refund to the originating cost center.\n  - name: Optimization\n    description: Migrate consumers to a successor provider; track migration cost delta.\n  - name: Accountability\n\
  \    description: Close out vendor relationship and ensure tokens revoked.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/iex-cloud/refs/heads/main/finops/iex-cloud-finops.yml
sources:
- https://iexcloud.io/community/blog/iex-cloud-end-of-life-announcement
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Market Data
- Sunset
- FinOps
- FOCUS
---
