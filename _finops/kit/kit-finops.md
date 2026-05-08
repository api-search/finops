---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Subscription (tiered by subscriber count)
description: FOCUS-aligned FinOps profile for Kit's subscriber-tier subscription pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Kit
  ProviderName: Kit
  PublisherName: Kit
  ServiceCategory: Email Marketing
  ServiceName: Kit Email Marketing
layout: finops
meters:
- aggregation: max
  description: Active subscribers on the account; pricing tier scales with this number.
  dimensions:
  - account
  name: subscriber_count
  unit: subscribers
- aggregation: sum
  description: Monthly or annual plan fee.
  dimensions:
  - plan_tier
  name: plan_subscription
  unit: months
name: Kit Finops
provider_name: Kit
provider_slug: kit
publisher_name: Kit
service_category: Email Marketing
slug: kit-finops
source_filename: kit-finops.yml
source_heading: FinOps Profile
source_url: https://kit.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Kit\nproviderId: kit\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Email Marketing\n- Creator Economy\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Kit's subscriber-tier subscription pricing.\nnotes: >-\n  Kit charges a subscription fee that scales with active subscriber count. API access is\n  included in the eligible plans rather than metered separately.\nsources:\n- https://kit.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Kit\nserviceCategory: Email Marketing\nbillingModel:\n  pricingCategory: Subscription (tiered by subscriber count)\n  billingFrequency:\
  \ Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Kit Email Marketing\n  ServiceCategory: Email Marketing\n  ProviderName: Kit\n  PublisherName: Kit\n  InvoiceIssuerName: Kit\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscriber_count\n  description: Active subscribers on the account; pricing tier scales with this number.\n  unit: subscribers\n  aggregation: max\n  dimensions:\n  - account\n- name: plan_subscription\n  description: Monthly or annual plan fee.\n  unit: months\n  aggregation: sum\n  dimensions:\n  - plan_tier\nprinciples:\n- name: Visibility\n  description: Track subscriber-count growth against pricing-tier breakpoints to forecast plan upgrades.\n- name: Allocation\n  description: Allocate plan cost to the marketing/newsletter cost center.\n- name: Optimization\n  description: Prune unengaged subscribers regularly to stay within the lower price tier.\n- name: Accountability\n\
  \  description: Assign a marketing-ops owner to review plan tier vs. actual subscriber count quarterly.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kit/refs/heads/main/finops/kit-finops.yml
sources:
- https://kit.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Email Marketing
- Creator Economy
- FinOps
- Cost Management
- FOCUS
---
