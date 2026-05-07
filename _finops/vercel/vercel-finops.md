---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Vercel REST API
  slug: vercel-rest-api
  spec_type: OpenAPI
  url: https://openapi.vercel.sh/
- filename: vercel-ai-gateway-openapi.yml
  format: yaml
  label: Vercel AI Gateway API
  slug: vercel-ai-gateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vercel/refs/heads/main/openapi/vercel-ai-gateway-openapi.yml
- filename: vercel-v0-platform-openapi.yml
  format: yaml
  label: V0 Platform API
  slug: v0-platform-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/vercel/refs/heads/main/openapi/vercel-v0-platform-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Usage-Based
description: FOCUS-aligned FinOps for Vercel.
focus_columns:
  BillingCurrency: USD
  ProviderName: Vercel
  PublisherName: Vercel Inc.
  ServiceCategory: Edge Hosting
  ServiceName: Vercel
layout: finops
meters:
- aggregation: max
  name: developer_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - project
  - edge_region
  name: bandwidth
  unit: GB
- aggregation: sum
  name: edge_requests
  unit: request
- aggregation: sum
  dimensions:
  - project
  - function
  name: fn_invocations
  unit: invocation
- aggregation: sum
  name: active_cpu_hours
  unit: cpu-hour
- aggregation: sum
  name: provisioned_memory
  unit: GB-hour
- aggregation: sum
  name: image_transformations
  unit: transformation
- aggregation: max
  name: blob_storage
  unit: GB-month
- aggregation: sum
  name: kv_requests
  unit: request
name: Vercel Finops
provider_name: Vercel
provider_slug: vercel
publisher_name: Vercel Inc.
service_category: Edge Hosting
slug: vercel-finops
source_filename: vercel-finops.yml
source_heading: FinOps Profile
source_url: https://vercel.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Vercel\nproviderId: vercel\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Hosting\ndescription: FOCUS-aligned FinOps for Vercel.\nsources:\n  - https://vercel.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Vercel Inc.\nserviceCategory: Edge Hosting\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Vercel\n  ServiceCategory: Edge Hosting\n  ProviderName: Vercel\n  PublisherName: Vercel Inc.\n  BillingCurrency: USD\nmeters:\n  - name: developer_seats\n    unit: seat-month\n    aggregation: max\n  - name: bandwidth\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - project\n      - edge_region\n  - name: edge_requests\n    unit: request\n    aggregation: sum\n  - name: fn_invocations\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - project\n      - function\n  - name: active_cpu_hours\n    unit: cpu-hour\n    aggregation: sum\n  - name: provisioned_memory\n    unit: GB-hour\n    aggregation: sum\n  - name: image_transformations\n    unit: transformation\n    aggregation: sum\n  - name: blob_storage\n    unit: GB-month\n    aggregation: max\n  - name: kv_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use Usage page and per-project breakdown; configure billing alerts at $X/day.\n  - name: Allocation\n    description: One project per app/feature; teams for cost-center isolation.\n  - name: Optimization\n    description: Cache aggressively at the edge; downgrade ISR frequency; profile fn duration.\n  - name: Accountability\n\
  \    description: Hard spend limits per team; weekly usage review during high-velocity periods.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/vercel/refs/heads/main/finops/vercel-finops.yml
sources:
- https://vercel.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Hosting
---
