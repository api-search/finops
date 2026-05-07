---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stability-ai-stable-image-generate-openapi.yml
  format: yaml
  label: Stability AI Stable Image Generate API
  slug: stable-image-generate
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/openapi/stability-ai-stable-image-generate-openapi.yml
- filename: stability-ai-stable-image-edit-openapi.yml
  format: yaml
  label: Stability AI Stable Image Edit API
  slug: stable-image-edit
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/openapi/stability-ai-stable-image-edit-openapi.yml
- filename: stability-ai-stable-image-upscale-openapi.yml
  format: yaml
  label: Stability AI Stable Image Upscale API
  slug: stable-image-upscale
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/openapi/stability-ai-stable-image-upscale-openapi.yml
- filename: stability-ai-stable-image-control-openapi.yml
  format: yaml
  label: Stability AI Stable Image Control API
  slug: stable-image-control
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/openapi/stability-ai-stable-image-control-openapi.yml
- filename: stability-ai-stable-video-diffusion-openapi.yml
  format: yaml
  label: Stability AI Stable Video Diffusion API
  slug: stable-video-diffusion
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/openapi/stability-ai-stable-video-diffusion-openapi.yml
- filename: stability-ai-stable-fast-3d-openapi.yml
  format: yaml
  label: Stability AI Stable Fast 3D API
  slug: stable-fast-3d
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/openapi/stability-ai-stable-fast-3d-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Pay-Per-Credit
description: FOCUS-aligned FinOps for Stability AI.
focus_columns:
  BillingCurrency: USD
  ProviderName: Stability AI
  PublisherName: Stability AI
  ServiceCategory: AI Image/Video Generation
  ServiceName: Stability AI
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  name: credits_used
  unit: credit
- aggregation: sum
  dimensions:
  - model
  name: images_generated
  unit: image
- aggregation: sum
  name: video_generated
  unit: video
- aggregation: sum
  name: credits_purchased
  unit: credit
name: Stability Ai Finops
provider_name: Stability AI
provider_slug: stability-ai
publisher_name: Stability AI
service_category: AI Image/Video Generation
slug: stability-ai-finops
source_filename: stability-ai-finops.yml
source_heading: FinOps Profile
source_url: https://platform.stability.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Stability AI\nproviderId: stability-ai\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AI Image/Video Generation\ndescription: FOCUS-aligned FinOps for Stability AI.\nsources:\n  - https://platform.stability.ai/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Stability AI\nserviceCategory: AI Image/Video Generation\nbillingModel:\n  pricingCategory: Subscription + Pay-Per-Credit\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Stability AI\n  ServiceCategory: AI Image/Video Generation\n  ProviderName: Stability AI\n  PublisherName: Stability AI\n  BillingCurrency: USD\nmeters:\n  - name:\
  \ credits_used\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - model\n  - name: images_generated\n    unit: image\n    aggregation: sum\n    dimensions:\n      - model\n  - name: video_generated\n    unit: video\n    aggregation: sum\n  - name: credits_purchased\n    unit: credit\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Stability AI consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stability-ai/refs/heads/main/finops/stability-ai-finops.yml
sources:
- https://platform.stability.ai/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- AI Image/Video Generation
---
