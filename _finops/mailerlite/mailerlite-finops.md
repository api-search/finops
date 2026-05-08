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
description: FOCUS-aligned FinOps profile for MailerLite's subscriber-tier subscription pricing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: MailerLite
  ProviderName: MailerLite
  PublisherName: MailerLite
  ServiceCategory: Email Marketing
  ServiceName: MailerLite Email Marketing
layout: finops
meters:
- aggregation: max
  description: Active subscribers; drives plan-tier breakpoints.
  dimensions:
  - account
  name: subscriber_count
  unit: subscribers
- aggregation: sum
  description: Monthly email send volume (capped on Free at 12k).
  dimensions:
  - account
  name: monthly_emails
  unit: emails
- aggregation: sum
  description: Monthly/annual plan fee.
  dimensions:
  - plan_tier
  name: plan_subscription
  unit: months
name: Mailerlite Finops
provider_name: MailerLite
provider_slug: mailerlite
publisher_name: MailerLite
service_category: Email Marketing
slug: mailerlite-finops
source_filename: mailerlite-finops.yml
source_heading: FinOps Profile
source_url: https://www.mailerlite.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: MailerLite\nproviderId: mailerlite\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Email Marketing\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for MailerLite's subscriber-tier subscription pricing.\nnotes: >-\n  MailerLite charges a monthly subscription that scales with subscriber count. API access\n  is included with all paid and free plans.\nsources:\n- https://www.mailerlite.com/pricing\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: MailerLite\nserviceCategory: Email Marketing\nbillingModel:\n  pricingCategory: Subscription (tiered by subscriber count)\n  billingFrequency:\
  \ Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: MailerLite Email Marketing\n  ServiceCategory: Email Marketing\n  ProviderName: MailerLite\n  PublisherName: MailerLite\n  InvoiceIssuerName: MailerLite\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: subscriber_count\n  description: Active subscribers; drives plan-tier breakpoints.\n  unit: subscribers\n  aggregation: max\n  dimensions:\n  - account\n- name: monthly_emails\n  description: Monthly email send volume (capped on Free at 12k).\n  unit: emails\n  aggregation: sum\n  dimensions:\n  - account\n- name: plan_subscription\n  description: Monthly/annual plan fee.\n  unit: months\n  aggregation: sum\n  dimensions:\n  - plan_tier\nprinciples:\n- name: Visibility\n  description: Track subscriber count vs. plan tier and email volume vs. cap.\n- name: Allocation\n  description: Allocate plan cost to the marketing/newsletter cost center.\n\
  - name: Optimization\n  description: Prune unengaged subscribers; consider annual billing for discounts.\n- name: Accountability\n  description: Quarterly review of plan tier vs. actual subscriber count.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mailerlite/refs/heads/main/finops/mailerlite-finops.yml
sources:
- https://www.mailerlite.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Email Marketing
- FinOps
- Cost Management
- FOCUS
---
