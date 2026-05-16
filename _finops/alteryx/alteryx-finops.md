---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: alteryx-server-api-v3.yml
  format: yaml
  label: Alteryx Server API V3
  slug: alteryx-server-api-v3
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/alteryx/refs/heads/main/openapi/alteryx-server-api-v3.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Tiered Subscription
description: 'FOCUS-aligned FinOps for Alteryx: tiered seat-based subscription pricing across Starter ($250 per user/month, annual billing), Professional, and Enterprise editions, with optional add-ons for automation capacity, dedicated data processing, and professional services. Three user roles - Viewer, Basic Creator, Full Creator - shape per-seat cost.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Alteryx, Inc.
  PricingUnit: seat-month
  ProviderName: Alteryx
  PublisherName: Alteryx, Inc.
  ServiceCategory: Analytics Platform
  ServiceName: Alteryx Analytics Platform
layout: finops
meters:
- aggregation: max
  description: Full Creator user seats (end-to-end automation across the analytics lifecycle)
  dimensions:
  - edition
  - region
  name: full_creator_seats
  unit: seat-month
- aggregation: max
  description: Basic Creator user seats (essential data prep and analytics tools)
  dimensions:
  - edition
  - region
  name: basic_creator_seats
  unit: seat-month
- aggregation: max
  description: Viewer user seats (access and explore shared workflows and reports)
  dimensions:
  - edition
  - region
  name: viewer_seats
  unit: seat-month
- aggregation: sum
  description: Add-on automation capacity beyond included edition allotments
  dimensions:
  - edition
  name: automation_capacity
  unit: capacity-unit-month
- aggregation: sum
  description: Add-on dedicated data-processing capacity
  dimensions:
  - edition
  name: dedicated_data_processing
  unit: capacity-unit-month
name: Alteryx Finops
provider_name: Alteryx
provider_slug: alteryx
publisher_name: Alteryx, Inc.
service_category: Analytics Platform
slug: alteryx-finops
source_filename: alteryx-finops.yml
source_heading: FinOps Profile
source_url: https://www.alteryx.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Alteryx\nproviderId: alteryx\npublisherName: Alteryx, Inc.\nserviceCategory: Analytics Platform\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Analytics\n  - Automation\n  - Data Engineering\n  - Data Preparation\n  - ETL\n  - Machine Learning\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Alteryx: tiered seat-based subscription pricing across Starter\n  ($250 per user/month, annual billing), Professional, and Enterprise editions, with optional add-ons\n  for automation capacity, dedicated data processing, and professional services. Three user roles - Viewer,\n  Basic Creator, Full Creator - shape per-seat\
  \ cost.'\nsources:\n  - https://www.alteryx.com/pricing\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Alteryx Analytics Platform\n  ServiceCategory: Analytics Platform\n  ProviderName: Alteryx\n  PublisherName: Alteryx, Inc.\n  InvoiceIssuerName: Alteryx, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: seat-month\nmeters:\n  - name: full_creator_seats\n    description: Full Creator user seats (end-to-end automation across the analytics lifecycle)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - edition\n      - region\n  - name: basic_creator_seats\n    description: Basic Creator user seats (essential data prep and analytics tools)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - edition\n\
  \      - region\n  - name: viewer_seats\n    description: Viewer user seats (access and explore shared workflows and reports)\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - edition\n      - region\n  - name: automation_capacity\n    description: Add-on automation capacity beyond included edition allotments\n    unit: capacity-unit-month\n    aggregation: sum\n    dimensions:\n      - edition\n  - name: dedicated_data_processing\n    description: Add-on dedicated data-processing capacity\n    unit: capacity-unit-month\n    aggregation: sum\n    dimensions:\n      - edition\nprinciples:\n  - name: Visibility\n    description: Use the Alteryx Server admin and Analytics Cloud usage dashboards to see seat utilization,\n      workflow run volume, and add-on capacity consumption. Reconcile against the annual subscription\n      schedule.\n  - name: Allocation\n    description: Allocate seats and capacity across analytics teams using Alteryx role assignments and\n      project-level\
  \ chargeback dimensions.\n  - name: Optimization\n    description: Right-size seat counts at renewal (downgrade Full Creators to Basic where possible, increase\n      Viewers for read-only consumption); evaluate add-on capacity utilization to avoid overprovisioning;\n      consolidate workflows to reduce automation-capacity needs.\n  - name: Accountability\n    description: Analytics center-of-excellence or data-engineering leadership owns the contract; run\n      quarterly utilization reviews against analytics outcomes.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/alteryx/refs/heads/main/finops/alteryx-finops.yml
sources:
- https://www.alteryx.com/pricing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Analytics
- Automation
- Data Engineering
- Data Preparation
- ETL
- Machine Learning
- FinOps
- FOCUS
---
