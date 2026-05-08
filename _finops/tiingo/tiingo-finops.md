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
  pricingCategory: Subscription
description: FinOps view of Tiingo. Subscription-based with a free non-commercial Power User plan, a small Commercial subscription (~$10/month), and add-on subscriptions for Fundamentals (~$50/month). Allocation is by API token; there is no usage-based billing beyond the rate cap.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Tiingo
  ProviderName: Tiingo
  PublisherName: Tiingo
  ServiceCategory: Fintech
  ServiceName: Tiingo Market Data API
layout: finops
meters:
- aggregation: sum
  description: Monthly Power User or Commercial subscription per token.
  dimensions:
  - token
  name: subscription
  unit: month
- aggregation: sum
  description: Monthly Fundamentals subscription add-on.
  dimensions:
  - token
  name: fundamentals_addon
  unit: month
name: Tiingo Finops
provider_name: Tiingo
provider_slug: tiingo
publisher_name: Tiingo
service_category: Fintech
slug: tiingo-finops
source_filename: tiingo-finops.yml
source_heading: FinOps Profile
source_url: https://www.tiingo.com/about/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Tiingo\nproviderId: tiingo\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Fintech\n  - Market Data\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Tiingo. Subscription-based with a free non-commercial Power User plan, a small\n  Commercial subscription (~$10/month), and add-on subscriptions for Fundamentals (~$50/month).\n  Allocation is by API token; there is no usage-based billing beyond the rate cap.\nsources:\n  - https://www.tiingo.com/about/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tiingo\nserviceCategory: Fintech\nbillingModel:\n  pricingCategory: Subscription\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: Tiingo Market Data API\n  ServiceCategory: Fintech\n  ProviderName: Tiingo\n  PublisherName: Tiingo\n  InvoiceIssuerName: Tiingo\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly Power User or Commercial subscription per token.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - token\n  - name: fundamentals_addon\n    description: Monthly Fundamentals subscription add-on.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - token\nprinciples:\n  - name: Visibility\n    description: Tag each Tiingo token to a single owning workload.\n  - name: Allocation\n    description: Allocate subscription to consuming product. Commercial use requires paid plan.\n  - name: Optimization\n    description: Drop Fundamentals add-on if research has moved to a different vendor.\n\
  \  - name: Accountability\n    description: Assign a billing owner per token; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tiingo/refs/heads/main/finops/tiingo-finops.yml
sources:
- https://www.tiingo.com/about/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Fintech
- Market Data
- FinOps
- FOCUS
---
