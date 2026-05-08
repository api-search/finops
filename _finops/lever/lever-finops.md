---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: lever-openapi.yml
  format: yaml
  label: Lever Opportunities API
  slug: lever-opportunities-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/lever/refs/heads/main/openapi/lever-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Tax
  pricingCategory: Annual Subscription
description: Lever's billing model is annual subscription on the LeverTRM bundle plus optional add-ons (Nurture, Analytics, Automation). Pricing is custom-quoted by company size and hiring volume. This artifact maps Lever charges to FOCUS columns for FinOps allocation across recruiting cost centers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Lever
  ProviderName: Lever
  PublisherName: Lever
  ServiceCategory: HR
  ServiceName: Lever
layout: finops
meters:
- aggregation: sum
  description: Annual LeverTRM subscription on the negotiated tier.
  dimensions:
  - tier
  - cost_center
  name: lever_trm_subscription
  unit: license-year
- aggregation: sum
  description: Add-ons (Nurture, Analytics, Automation, Advanced Reports).
  dimensions:
  - addon
  - cost_center
  name: lever_addons
  unit: addon-year
- aggregation: count
  description: One-time implementation, integration, or onboarding fees.
  dimensions:
  - service
  name: implementation_fee
  unit: events
name: Lever Finops
provider_name: Lever
provider_slug: lever
publisher_name: Lever
service_category: HR
slug: lever-finops
source_filename: lever-finops.yml
source_heading: FinOps Profile
source_url: https://www.lever.co/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Lever\nproviderId: lever\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - HR\n  - ATS\n  - Recruiting\n  - Talent Acquisition\n  - FinOps\n  - FOCUS\ndescription: >-\n  Lever's billing model is annual subscription on the LeverTRM bundle plus\n  optional add-ons (Nurture, Analytics, Automation). Pricing is custom-quoted\n  by company size and hiring volume. This artifact maps Lever charges to\n  FOCUS columns for FinOps allocation across recruiting cost centers.\nsources:\n  - https://www.lever.co/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Lever\nserviceCategory: HR\nbillingModel:\n\
  \  pricingCategory: Annual Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Tax\nfocusColumns:\n  ServiceName: Lever\n  ServiceCategory: HR\n  ProviderName: Lever\n  PublisherName: Lever\n  InvoiceIssuerName: Lever\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: lever_trm_subscription\n    description: Annual LeverTRM subscription on the negotiated tier.\n    unit: license-year\n    aggregation: sum\n    dimensions:\n      - tier\n      - cost_center\n  - name: lever_addons\n    description: Add-ons (Nurture, Analytics, Automation, Advanced Reports).\n    unit: addon-year\n    aggregation: sum\n    dimensions:\n      - addon\n      - cost_center\n  - name: implementation_fee\n    description: One-time implementation, integration, or onboarding fees.\n    unit: events\n    aggregation: count\n    dimensions:\n      - service\nprinciples:\n  - name: Visibility\n    description: >-\n    \
  \  Pull annual Lever invoices and renewal quotes; reconcile against\n      configured user count and active integrations.\n  - name: Allocation\n    description: >-\n      Allocate Lever cost to recruiting / talent functions; tag by\n      department or cost center via the Recruiting cost center.\n  - name: Optimization\n    description: >-\n      Audit unused add-ons before renewal; consolidate user counts and\n      negotiate volume discounts based on hiring forecast.\n  - name: Accountability\n    description: >-\n      Designate Talent Operations as the contract owner; review quarterly\n      against the master service agreement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/lever/refs/heads/main/finops/lever-finops.yml
sources:
- https://www.lever.co/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- HR
- ATS
- Recruiting
- Talent Acquisition
- FinOps
- FOCUS
---
