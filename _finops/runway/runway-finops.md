---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: runway-video-generation-openapi.yml
  format: yaml
  label: Runway Video Generation API
  slug: video-generation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/runway/refs/heads/main/openapi/runway-video-generation-openapi.yml
- filename: runway-image-generation-openapi.yml
  format: yaml
  label: Runway Image Generation API
  slug: image-generation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/runway/refs/heads/main/openapi/runway-image-generation-openapi.yml
- filename: runway-characters-openapi.yml
  format: yaml
  label: Runway Characters API
  slug: characters
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/runway/refs/heads/main/openapi/runway-characters-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Credits
description: FOCUS-aligned FinOps for Runway.
focus_columns:
  BillingCurrency: USD
  ProviderName: Runway
  PublisherName: Runway
  ServiceCategory: Video Generation AI
  ServiceName: Runway
layout: finops
meters:
- aggregation: sum
  dimensions:
  - model
  name: credits_used
  unit: credit
- aggregation: max
  name: asset_storage
  unit: GB-month
- aggregation: sum
  name: generations
  unit: generation
name: Runway Finops
provider_name: Runway
provider_slug: runway
publisher_name: Runway
service_category: Video Generation AI
slug: runway-finops
source_filename: runway-finops.yml
source_heading: FinOps Profile
source_url: https://runwayml.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Runway\nproviderId: runway\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Video Generation AI\ndescription: FOCUS-aligned FinOps for Runway.\nsources:\n  - https://runwayml.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Runway\nserviceCategory: Video Generation AI\nbillingModel:\n  pricingCategory: Subscription + Credits\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Runway\n  ServiceCategory: Video Generation AI\n  ProviderName: Runway\n  PublisherName: Runway\n  BillingCurrency: USD\nmeters:\n  - name: credits_used\n    unit: credit\n    aggregation: sum\n    dimensions:\n \
  \     - model\n  - name: asset_storage\n    unit: GB-month\n    aggregation: max\n  - name: generations\n    unit: generation\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Runway consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size models/tiers; use caching and batching.\n  - name: Accountability\n    description: Set hard spend limits; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/runway/refs/heads/main/finops/runway-finops.yml
sources:
- https://runwayml.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Video Generation AI
---
