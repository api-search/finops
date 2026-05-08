---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: planetscale-platform-api-openapi.yml
  format: yaml
  label: PlanetScale Platform API
  slug: platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/planetscale/refs/heads/main/openapi/planetscale-platform-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: SKU-Based (Cluster Size + Storage + Egress)
description: FOCUS-aligned FinOps for PlanetScale.
focus_columns:
  BillingCurrency: USD
  ProviderName: PlanetScale
  PublisherName: PlanetScale
  ServiceCategory: Distributed Database
  ServiceName: PlanetScale
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster_size
  - engine
  - region
  name: cluster_hours
  unit: cluster-hour
- aggregation: max
  name: storage
  unit: GB-month
- aggregation: max
  name: backups
  unit: GB-month
- aggregation: sum
  name: egress
  unit: GB
- aggregation: sum
  name: replicas
  unit: replica-hour
name: Planetscale Finops
provider_name: planetscale
provider_slug: planetscale
publisher_name: PlanetScale
service_category: Distributed Database
slug: planetscale-finops
source_filename: planetscale-finops.yml
source_heading: FinOps Profile
source_url: https://planetscale.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PlanetScale\nproviderId: planetscale\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Distributed Database\ndescription: FOCUS-aligned FinOps for PlanetScale.\nsources:\n  - https://planetscale.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PlanetScale\nserviceCategory: Distributed Database\nbillingModel:\n  pricingCategory: SKU-Based (Cluster Size + Storage + Egress)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: PlanetScale\n  ServiceCategory: Distributed Database\n  ProviderName: PlanetScale\n  PublisherName: PlanetScale\n  BillingCurrency: USD\nmeters:\n  - name: cluster_hours\n\
  \    unit: cluster-hour\n    aggregation: sum\n    dimensions:\n      - cluster_size\n      - engine\n      - region\n  - name: storage\n    unit: GB-month\n    aggregation: max\n  - name: backups\n    unit: GB-month\n    aggregation: max\n  - name: egress\n    unit: GB\n    aggregation: sum\n  - name: replicas\n    unit: replica-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track PlanetScale consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/planetscale/refs/heads/main/finops/planetscale-finops.yml
sources:
- https://planetscale.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Distributed Database
---
