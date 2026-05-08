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
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Hybrid
description: FOCUS-aligned FinOps profile. Merchants pay SaaS + processing; developers earn via app market revenue share.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Clover
  ProviderName: Clover
  PublisherName: Clover
  ServiceCategory: Payments & POS
  ServiceName: Clover
layout: finops
meters:
- aggregation: sum
  description: Monthly merchant SaaS subscription.
  dimensions:
  - merchant
  name: merchant_saas
  unit: subscription
- aggregation: sum
  description: Card-present and online processing volume.
  dimensions:
  - merchant
  name: processing_volume
  unit: USD
- aggregation: sum
  description: App Market subscription revenue share.
  dimensions:
  - app
  - merchant
  name: app_market_revshare
  unit: USD
name: Clover Finops
provider_name: Clover
provider_slug: clover
publisher_name: Clover
service_category: Payments & POS
slug: clover-finops
source_filename: clover-finops.yml
source_heading: FinOps Profile
source_url: https://www.clover.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Clover\nproviderId: clover\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- POS\n- Payments\n- Retail\n- SMB\n- Hardware\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Merchants pay SaaS + processing; developers earn via app market\n  revenue share.\nnotes: 'Two distinct billing personas: merchant and app developer.'\nsources:\n- https://www.clover.com/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Clover\nserviceCategory: Payments & POS\nbillingModel:\n  pricingCategory: Hybrid\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n\
  \  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Clover\n  ServiceCategory: Payments & POS\n  ProviderName: Clover\n  PublisherName: Clover\n  InvoiceIssuerName: Clover\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: merchant_saas\n  description: Monthly merchant SaaS subscription.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - merchant\n- name: processing_volume\n  description: Card-present and online processing volume.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - merchant\n- name: app_market_revshare\n  description: App Market subscription revenue share.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - app\n  - merchant\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing\
  \ model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/clover/refs/heads/main/finops/clover-finops.yml
sources:
- https://www.clover.com/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- POS
- Payments
- Retail
- SMB
- Hardware
- FinOps
- Cost Management
- FOCUS
---
