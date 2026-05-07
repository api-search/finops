---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: render-openapi.json
  format: json
  label: Render API
  slug: render-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/render/refs/heads/main/openapi/render-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Instance + Workspace Subscription + Usage
description: FOCUS-aligned FinOps for Render.
focus_columns:
  BillingCurrency: USD
  ProviderName: Render
  PublisherName: Render
  ServiceCategory: Hosting
  ServiceName: Render
layout: finops
meters:
- aggregation: sum
  dimensions:
  - plan
  - service_type
  name: instance_hours
  unit: instance-hour
- aggregation: sum
  name: bandwidth
  unit: GB
- aggregation: max
  name: workspace_seats
  unit: seat-month
- aggregation: sum
  name: build_minutes
  unit: minute
- aggregation: max
  name: managed_postgres
  unit: instance-month
name: Render Finops
provider_name: Render
provider_slug: render
publisher_name: Render
service_category: Hosting
slug: render-finops
source_filename: render-finops.yml
source_heading: FinOps Profile
source_url: https://render.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Render\nproviderId: render\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Hosting\ndescription: FOCUS-aligned FinOps for Render.\nsources:\n  - https://render.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Render\nserviceCategory: Hosting\nbillingModel:\n  pricingCategory: Per-Instance + Workspace Subscription + Usage\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Render\n  ServiceCategory: Hosting\n  ProviderName: Render\n  PublisherName: Render\n  BillingCurrency: USD\nmeters:\n  - name: instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      -\
  \ plan\n      - service_type\n  - name: bandwidth\n    unit: GB\n    aggregation: sum\n  - name: workspace_seats\n    unit: seat-month\n    aggregation: max\n  - name: build_minutes\n    unit: minute\n    aggregation: sum\n  - name: managed_postgres\n    unit: instance-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Render consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/render/refs/heads/main/finops/render-finops.yml
sources:
- https://render.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Hosting
---
