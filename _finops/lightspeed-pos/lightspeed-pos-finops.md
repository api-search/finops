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
  pricingCategory: Subscription
description: FOCUS-aligned FinOps profile. Monthly merchant SaaS with optional payment processing.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Lightspeed
  ProviderName: Lightspeed
  PublisherName: Lightspeed
  ServiceCategory: Payments & POS
  ServiceName: Lightspeed
layout: finops
meters:
- aggregation: sum
  description: Monthly merchant SaaS subscription.
  dimensions:
  - merchant
  name: merchant_saas
  unit: subscription
- aggregation: sum
  description: Lightspeed Payments processing volume.
  dimensions:
  - merchant
  name: processing_volume
  unit: USD
name: Lightspeed Pos Finops
provider_name: Lightspeed
provider_slug: lightspeed-pos
publisher_name: Lightspeed
service_category: Payments & POS
slug: lightspeed-pos-finops
source_filename: lightspeed-pos-finops.yml
source_heading: FinOps Profile
source_url: https://www.lightspeedhq.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lightspeed\nproviderId: lightspeed-pos\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: false\ntags:\n- POS\n- Retail\n- Restaurant\n- Ecommerce\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile. Monthly merchant SaaS with optional payment processing.\nnotes: Region-specific currencies (USD, CAD, EUR, GBP, AUD).\nsources:\n- https://www.lightspeedhq.com/pricing/\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lightspeed\nserviceCategory: Payments & POS\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n\
  \  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Lightspeed\n  ServiceCategory: Payments & POS\n  ProviderName: Lightspeed\n  PublisherName: Lightspeed\n  InvoiceIssuerName: Lightspeed\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n- name: merchant_saas\n  description: Monthly merchant SaaS subscription.\n  unit: subscription\n  aggregation: sum\n  dimensions:\n  - merchant\n- name: processing_volume\n  description: Lightspeed Payments processing volume.\n  unit: USD\n  aggregation: sum\n  dimensions:\n  - merchant\nprinciples:\n- name: Visibility\n  description: Pull provider invoices or usage exports until a self-serve usage feed is documented.\n- name: Allocation\n  description: Tag invoice line items to consuming business units in your FinOps store.\n- name: Optimization\n  description: Levers depend on the provider's billing model; review at renewal once reconciled.\n- name: Accountability\n  description: Assign a contract owner to review billing against negotiated\
  \ terms.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lightspeed-pos/refs/heads/main/finops/lightspeed-pos-finops.yml
sources:
- https://www.lightspeedhq.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- POS
- Retail
- Restaurant
- Ecommerce
- FinOps
- Cost Management
- FOCUS
---
