---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: postman.yaml
  format: yaml
  label: Railway Public GraphQL API
  slug: public-api
  spec_type: Postman
  url: https://raw.githubusercontent.com/api-evangelist/railway/refs/heads/main/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Per-Resource Metered
description: FOCUS-aligned FinOps for Railway.
focus_columns:
  BillingCurrency: USD
  ProviderName: Railway
  PublisherName: Railway
  ServiceCategory: Edge Hosting
  ServiceName: Railway
layout: finops
meters:
- aggregation: sum
  name: memory_gb_seconds
  unit: GB-second
- aggregation: sum
  name: cpu_vcpu_seconds
  unit: vCPU-second
- aggregation: sum
  name: volume_gb_seconds
  unit: GB-second
- aggregation: sum
  name: egress
  unit: GB
- aggregation: max
  name: workspace_seats
  unit: seat-month
name: Railway Finops
provider_name: Railway
provider_slug: railway
publisher_name: Railway
service_category: Edge Hosting
slug: railway-finops
source_filename: railway-finops.yml
source_heading: FinOps Profile
source_url: https://railway.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Railway\nproviderId: railway\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Edge Hosting\ndescription: FOCUS-aligned FinOps for Railway.\nsources:\n  - https://railway.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Railway\nserviceCategory: Edge Hosting\nbillingModel:\n  pricingCategory: Subscription + Per-Resource Metered\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Railway\n  ServiceCategory: Edge Hosting\n  ProviderName: Railway\n  PublisherName: Railway\n  BillingCurrency: USD\nmeters:\n  - name: memory_gb_seconds\n    unit: GB-second\n    aggregation: sum\n  - name: cpu_vcpu_seconds\n\
  \    unit: vCPU-second\n    aggregation: sum\n  - name: volume_gb_seconds\n    unit: GB-second\n    aggregation: sum\n  - name: egress\n    unit: GB\n    aggregation: sum\n  - name: workspace_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Railway consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/railway/refs/heads/main/finops/railway-finops.yml
sources:
- https://railway.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Edge Hosting
---
