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
description: FinOps view of Messari. Subscription-based tiers (Free, Pro, Enterprise). Pro and Enterprise contracts include access to proprietary research, Token Unlocks dataset, and Messari Copilot AI agent. Allocation is by API key and by published research seat.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: Messari
  ProviderName: Messari
  PublisherName: Messari
  ServiceCategory: Crypto Research
  ServiceName: Messari API
layout: finops
meters:
- aggregation: sum
  description: Monthly Pro or Enterprise subscription per API key.
  dimensions:
  - api_key
  name: subscription
  unit: month
name: Messari Finops
provider_name: Messari
provider_slug: messari
publisher_name: Messari
service_category: Crypto Research
slug: messari-finops
source_filename: messari-finops.yml
source_heading: FinOps Profile
source_url: https://messari.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Messari\nproviderId: messari\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Crypto\n  - Research\n  - FinOps\n  - FOCUS\ndescription: >-\n  FinOps view of Messari. Subscription-based tiers (Free, Pro, Enterprise). Pro and Enterprise\n  contracts include access to proprietary research, Token Unlocks dataset, and Messari Copilot\n  AI agent. Allocation is by API key and by published research seat.\nsources:\n  - https://messari.io/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Messari\nserviceCategory: Crypto Research\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency:\
  \ Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Adjustment\nfocusColumns:\n  ServiceName: Messari API\n  ServiceCategory: Crypto Research\n  ProviderName: Messari\n  PublisherName: Messari\n  InvoiceIssuerName: Messari\n  BillingCurrency: USD\n  ChargeCategory: Subscription\nmeters:\n  - name: subscription\n    description: Monthly Pro or Enterprise subscription per API key.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - api_key\nprinciples:\n  - name: Visibility\n    description: Tag each API key to a single owning workload; track research seats separately.\n  - name: Allocation\n    description: Allocate subscription across consuming research and engineering teams.\n  - name: Optimization\n    description: Right-size between Pro and Enterprise based on Token Unlocks usage and Copilot need.\n  - name: Accountability\n    description: Assign a billing owner and review at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/messari/refs/heads/main/finops/messari-finops.yml
sources:
- https://messari.io/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Crypto
- Research
- FinOps
- FOCUS
---
