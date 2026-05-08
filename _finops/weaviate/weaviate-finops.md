---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: weaviate-openapi.yml
  format: yaml
  label: Weaviate REST API
  slug: weaviate-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/weaviate/refs/heads/main/openapi/weaviate-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Per-GiB
description: FOCUS-aligned FinOps for Weaviate.
focus_columns:
  BillingCurrency: USD
  ProviderName: Weaviate
  PublisherName: Weaviate
  ServiceCategory: Vector Database
  ServiceName: Weaviate
layout: finops
meters:
- aggregation: max
  dimensions:
  - cluster
  - tier
  name: storage
  unit: GiB-month
- aggregation: max
  name: backup_storage
  unit: GiB-month
- aggregation: max
  name: vector_dimensions
  unit: dimension-month
name: Weaviate Finops
provider_name: Weaviate
provider_slug: weaviate
publisher_name: Weaviate
service_category: Vector Database
slug: weaviate-finops
source_filename: weaviate-finops.yml
source_heading: FinOps Profile
source_url: https://weaviate.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Weaviate\nproviderId: weaviate\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Vector Database\ndescription: FOCUS-aligned FinOps for Weaviate.\nsources:\n  - https://weaviate.io/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Weaviate\nserviceCategory: Vector Database\nbillingModel:\n  pricingCategory: Subscription + Per-GiB\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Weaviate\n  ServiceCategory: Vector Database\n  ProviderName: Weaviate\n  PublisherName: Weaviate\n  BillingCurrency: USD\nmeters:\n  - name: storage\n    unit: GiB-month\n    aggregation: max\n    dimensions:\n  \
  \    - cluster\n      - tier\n  - name: backup_storage\n    unit: GiB-month\n    aggregation: max\n  - name: vector_dimensions\n    unit: dimension-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Weaviate consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/weaviate/refs/heads/main/finops/weaviate-finops.yml
sources:
- https://weaviate.io/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Vector Database
---
