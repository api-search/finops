---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: zitadel-management-openapi.yml
  format: yaml
  label: Zitadel Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/zitadel/refs/heads/main/openapi/zitadel-management-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps view for ZITADEL Cloud: a tiered subscription anchored on

  Daily Active Users (DAU), with optional Pro add-ons for extended SLA support and

  data-location pinning, and custom volume-based pricing at Enterprise. Self-hosting

  the open-source build has no ZITADEL invoice line.

  '
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: ZITADEL (CAOS AG)
  ProviderName: ZITADEL
  PublisherName: ZITADEL (CAOS AG)
  ServiceCategory: Identity / Authentication
  ServiceName: ZITADEL Cloud
layout: finops
meters:
- aggregation: max
  description: Monthly plan subscription (Free / Pro / Enterprise); the primary ZITADEL Cloud billing line.
  dimensions:
  - plan_tier
  name: plan_subscription
  unit: month
- aggregation: max
  description: DAU consumed against the plan's bundled cap (100 Free / 25,000 Pro / custom Enterprise).
  dimensions:
  - plan_tier
  name: daily_active_users
  unit: dau
- aggregation: max
  description: Optional Pro add-on for 99.95% availability and extended support / SLA at $999/month.
  name: addon_extended_support_sla
  unit: month
- aggregation: max
  description: Optional Pro add-on for region pinning (US / EU / Switzerland / Australia) at $100/month.
  dimensions:
  - region
  name: addon_data_location
  unit: month
name: Zitadel Finops
provider_name: Zitadel
provider_slug: zitadel
publisher_name: ZITADEL (CAOS AG)
service_category: Identity / Authentication
slug: zitadel-finops
source_filename: zitadel-finops.yml
source_heading: FinOps Profile
source_url: https://zitadel.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Zitadel\nproviderId: zitadel\npublisherName: ZITADEL (CAOS AG)\nserviceCategory: Identity / Authentication\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Authentication\n  - Authorization\n  - Identity Management\n  - FinOps\n  - FOCUS\ndescription: |\n  FOCUS-aligned FinOps view for ZITADEL Cloud: a tiered subscription anchored on\n  Daily Active Users (DAU), with optional Pro add-ons for extended SLA support and\n  data-location pinning, and custom volume-based pricing at Enterprise. Self-hosting\n  the open-source build has no ZITADEL invoice line.\nsources:\n  - https://zitadel.com/pricing\n  - https://zitadel.com/docs/legal/policies/rate-limit-policy\n\
  billingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\nfocusColumns:\n  ServiceName: ZITADEL Cloud\n  ServiceCategory: Identity / Authentication\n  ProviderName: ZITADEL\n  PublisherName: ZITADEL (CAOS AG)\n  InvoiceIssuerName: ZITADEL (CAOS AG)\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: plan_subscription\n    description: Monthly plan subscription (Free / Pro / Enterprise); the primary ZITADEL\n      Cloud billing line.\n    unit: month\n    aggregation: max\n    dimensions:\n      - plan_tier\n  - name: daily_active_users\n    description: DAU consumed against the plan's bundled cap (100 Free / 25,000 Pro /\n      custom Enterprise).\n    unit: dau\n    aggregation: max\n    dimensions:\n      - plan_tier\n  - name: addon_extended_support_sla\n    description: Optional Pro add-on for 99.95% availability and extended support /\n      SLA at $999/month.\n\
  \    unit: month\n    aggregation: max\n  - name: addon_data_location\n    description: Optional Pro add-on for region pinning (US / EU / Switzerland /\n      Australia) at $100/month.\n    unit: month\n    aggregation: max\n    dimensions:\n      - region\nprinciples:\n  - name: Visibility\n    description: Use the ZITADEL Cloud customer console for current DAU and plan\n      consumption; self-hosted deployments have no ZITADEL invoice but cost shows up\n      as the underlying compute / DB / storage.\n  - name: Allocation\n    description: Allocate ZITADEL spend per environment (dev / staging / prod) and per\n      tenant organization; tag region pinning to the regulated business unit that\n      requires it.\n  - name: Optimization\n    description: Cost levers are choosing Free vs Pro based on actual DAU, whether the\n      Extended Support and SLA add-on is required by SLAs, and whether self-hosting\n      the open-source build is preferable to ZITADEL Cloud at the customer's scale.\n\
  \  - name: Accountability\n    description: Spend ownership sits with the platform / identity team that owns the\n      ZITADEL deployment; review at the monthly DAU report and at Enterprise contract\n      renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/zitadel/refs/heads/main/finops/zitadel-finops.yml
sources:
- https://zitadel.com/pricing
- https://zitadel.com/docs/legal/policies/rate-limit-policy
specification: FinOps Framework
tags:
- Authentication
- Authorization
- Identity Management
- FinOps
- FOCUS
---
