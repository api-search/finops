---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: replicate-openapi.yml
  format: yaml
  label: Replicate
  slug: replicate
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/replicate/refs/heads/main/openapi/replicate-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Second GPU
description: FOCUS-aligned FinOps for Replicate.
focus_columns:
  BillingCurrency: USD
  ProviderName: Replicate
  PublisherName: Replicate
  ServiceCategory: ML Inference
  ServiceName: Replicate
layout: finops
meters:
- aggregation: sum
  dimensions:
  - hardware
  - model
  name: gpu_seconds
  unit: second
- aggregation: sum
  name: predictions_count
  unit: prediction
- aggregation: sum
  name: deployment_idle_seconds
  unit: second
name: Replicate Finops
provider_name: Replicate
provider_slug: replicate
publisher_name: Replicate
service_category: ML Inference
slug: replicate-finops
source_filename: replicate-finops.yml
source_heading: FinOps Profile
source_url: https://replicate.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Replicate\nproviderId: replicate\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - ML Inference\ndescription: FOCUS-aligned FinOps for Replicate.\nsources:\n  - https://replicate.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Replicate\nserviceCategory: ML Inference\nbillingModel:\n  pricingCategory: Per-Second GPU\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Replicate\n  ServiceCategory: ML Inference\n  ProviderName: Replicate\n  PublisherName: Replicate\n  BillingCurrency: USD\nmeters:\n  - name: gpu_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n      - hardware\n\
  \      - model\n  - name: predictions_count\n    unit: prediction\n    aggregation: sum\n  - name: deployment_idle_seconds\n    unit: second\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Replicate consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/replicate/refs/heads/main/finops/replicate-finops.yml
sources:
- https://replicate.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- ML Inference
---
