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
  pricingCategory: Subscription
description: FinOps view of 1inch. Subscription-based developer portal pricing per API key. No usage-based fees beyond the rate cap. On-chain swap revenue (positive slippage) is settled separately by the protocol; not part of the API subscription bill.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: 1inch
  ProviderName: 1inch
  PublisherName: 1inch Network
  ServiceCategory: DeFi Infrastructure
  ServiceName: 1inch Developer Portal
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription per API key.
  dimensions:
  - api_key
  name: subscription
  unit: month
name: One Inch Finops
provider_name: 1inch
provider_slug: one-inch
publisher_name: 1inch Network
service_category: DeFi Infrastructure
slug: one-inch-finops
source_filename: one-inch-finops.yml
source_heading: FinOps Profile
source_url: https://business.1inch.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: 1inch\nproviderId: one-inch\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - DeFi\n  - DEX\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of 1inch. Subscription-based developer portal pricing per API key. No usage-based\n  fees beyond the rate cap. On-chain swap revenue (positive slippage) is settled separately by\n  the protocol; not part of the API subscription bill.\nsources:\n  - https://business.1inch.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: 1inch Network\nserviceCategory: DeFi Infrastructure\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Subscription\nfocusColumns:\n  ServiceName: 1inch Developer Portal\n  ServiceCategory: DeFi Infrastructure\n  ProviderName: 1inch\n  PublisherName: 1inch Network\n  InvoiceIssuerName: 1inch\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly subscription per API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each API key to a single owning workload.\n  - name: Allocation\n    description: Allocate subscription across consuming products.\n  - name: Optimization\n    description: Right-size between Developer / Startup / Business by measured rps.\n  - name: Accountability\n    description: Assign a billing owner; review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/one-inch/refs/heads/main/finops/one-inch-finops.yml
sources:
- https://business.1inch.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- DeFi
- DEX
- FinOps
- FOCUS
---
