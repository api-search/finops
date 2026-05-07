---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amberflo-metering-openapi.yaml
  format: yaml
  label: Amberflo Metering API
  slug: metering-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amberflo/refs/heads/main/openapi/amberflo-metering-openapi.yaml
- filename: amberflo-billing-openapi.yaml
  format: yaml
  label: Amberflo Billing API
  slug: billing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amberflo/refs/heads/main/openapi/amberflo-billing-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Overage
description: 'FOCUS-aligned FinOps for Amberflo: tiered monthly subscription (Startups, Growth, Enterprise) with included pools of billing volume and meter events plus overage at 0.54% on additional billing volume and $5 per additional 10,000 meter events. Amberflo itself is a metering-and-billing platform, so its FinOps posture mirrors the SaaS subscription archetype.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Amberflo.io, Inc.
  ProviderName: Amberflo
  PublisherName: Amberflo.io, Inc.
  ServiceCategory: Business Applications
  ServiceName: Amberflo
  ServiceSubcategory: Metering and Billing
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tier
  name: subscription_months
  unit: month
- aggregation: sum
  dimensions:
  - account
  - meter_name
  name: meter_events_ingested
  unit: event
- aggregation: sum
  dimensions:
  - account
  - product
  name: billing_volume_processed
  unit: USD
- aggregation: sum
  dimensions:
  - account
  name: overage_events
  unit: event
- aggregation: sum
  dimensions:
  - account
  name: overage_billing_volume
  unit: USD
name: Amberflo Finops
provider_name: Amberflo
provider_slug: amberflo
publisher_name: Amberflo.io, Inc.
service_category: FinOps / Metering and Billing
slug: amberflo-finops
source_filename: amberflo-finops.yml
source_heading: FinOps Profile
source_url: https://www.amberflo.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amberflo\nproviderId: amberflo\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Usage-Based Billing\n  - Metering\n  - Amberflo\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amberflo: tiered monthly subscription (Startups, Growth, Enterprise)\n  with included pools of billing volume and meter events plus overage at 0.54% on additional billing\n  volume and $5 per additional 10,000 meter events. Amberflo itself is a metering-and-billing platform,\n  so its FinOps posture mirrors the SaaS subscription archetype.'\nsources:\n  - https://www.amberflo.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amberflo.io,\
  \ Inc.\nserviceCategory: FinOps / Metering and Billing\nbillingModel:\n  pricingCategory: Tiered Subscription + Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Amberflo\n  ServiceCategory: Business Applications\n  ServiceSubcategory: Metering and Billing\n  ProviderName: Amberflo\n  PublisherName: Amberflo.io, Inc.\n  InvoiceIssuerName: Amberflo.io, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: subscription_months\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: meter_events_ingested\n    unit: event\n    aggregation: sum\n    dimensions:\n      - account\n      - meter_name\n  - name: billing_volume_processed\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account\n      - product\n  - name: overage_events\n    unit: event\n    aggregation: sum\n    dimensions:\n      - account\n\
  \  - name: overage_billing_volume\n    unit: USD\n    aggregation: sum\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Use Amberflo's own usage and revenue dashboards (eat-your-own-dogfood); export billable\n      events to your data warehouse and reconcile against the Amberflo invoice.\n  - name: Allocation\n    description: Tag meters and customers with product, environment, and team; chargeback subscription\n      cost via meter-event share.\n  - name: Optimization\n    description: Right-size the Growth tier (250K vs 500K vs 1M request bracket) to your actual ingest\n      volume; batch meter events to minimize request count; consolidate redundant meters.\n  - name: Accountability\n    description: Owner of monetization/finance team owns the Amberflo subscription; alert on overage thresholds\n      and review monthly billing-volume utilization against tier inclusions.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url:\
  \ https://apievangelist.com\n  - name: Amberflo\n    email: support@amberflo.io\n    url: https://www.amberflo.io\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amberflo/refs/heads/main/finops/amberflo-finops.yml
sources:
- https://www.amberflo.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Usage-Based Billing
- Metering
- Amberflo
- Cost Management
---
