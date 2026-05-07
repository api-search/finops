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
  pricingCategory: Custom Usage-Based
description: FOCUS-aligned FinOps for Modern Treasury.
focus_columns:
  BillingCurrency: USD
  ProviderName: Modern Treasury
  PublisherName: Modern Treasury
  ServiceCategory: Bank Payments
  ServiceName: Modern Treasury
layout: finops
meters:
- aggregation: sum
  name: ach_transactions
  unit: transaction
- aggregation: sum
  name: wire_transactions
  unit: transaction
- aggregation: sum
  name: rtp_transactions
  unit: transaction
- aggregation: sum
  name: push_to_card_transactions
  unit: transaction
- aggregation: sum
  name: stablecoin_transactions
  unit: transaction
- aggregation: max
  name: internal_accounts
  unit: account-month
name: Modern Treasury Finops
provider_name: Modern Treasury
provider_slug: modern-treasury
publisher_name: Modern Treasury
service_category: Bank Payments
slug: modern-treasury-finops
source_filename: modern-treasury-finops.yml
source_heading: FinOps Profile
source_url: https://www.moderntreasury.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Modern Treasury\nproviderId: modern-treasury\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Bank Payments\ndescription: FOCUS-aligned FinOps for Modern Treasury.\nsources:\n  - https://www.moderntreasury.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Modern Treasury\nserviceCategory: Bank Payments\nbillingModel:\n  pricingCategory: Custom Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Modern Treasury\n  ServiceCategory: Bank Payments\n  ProviderName: Modern Treasury\n  PublisherName: Modern Treasury\n  BillingCurrency: USD\nmeters:\n  - name: ach_transactions\n   \
  \ unit: transaction\n    aggregation: sum\n  - name: wire_transactions\n    unit: transaction\n    aggregation: sum\n  - name: rtp_transactions\n    unit: transaction\n    aggregation: sum\n  - name: push_to_card_transactions\n    unit: transaction\n    aggregation: sum\n  - name: stablecoin_transactions\n    unit: transaction\n    aggregation: sum\n  - name: internal_accounts\n    unit: account-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Modern Treasury consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/modern-treasury/refs/heads/main/finops/modern-treasury-finops.yml
sources:
- https://www.moderntreasury.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Bank Payments
---
