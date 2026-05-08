---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: posthog-openapi.yml
  format: yaml
  label: PostHog API
  slug: posthog
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/posthog/refs/heads/main/openapi/posthog-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Event / Per-Replay / Per-Request Tiered
description: FOCUS-aligned FinOps for PostHog.
focus_columns:
  BillingCurrency: USD
  ProviderName: PostHog
  PublisherName: PostHog
  ServiceCategory: Product Analytics
  ServiceName: PostHog
layout: finops
meters:
- aggregation: sum
  name: captured_events
  unit: event
- aggregation: sum
  name: session_replays
  unit: replay
- aggregation: sum
  name: feature_flag_requests
  unit: request
- aggregation: max
  name: experiments
  unit: experiment
name: Posthog Finops
provider_name: PostHog
provider_slug: posthog
publisher_name: PostHog
service_category: Product Analytics
slug: posthog-finops
source_filename: posthog-finops.yml
source_heading: FinOps Profile
source_url: https://posthog.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: PostHog\nproviderId: posthog\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Product Analytics\ndescription: FOCUS-aligned FinOps for PostHog.\nsources:\n  - https://posthog.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PostHog\nserviceCategory: Product Analytics\nbillingModel:\n  pricingCategory: Per-Event / Per-Replay / Per-Request Tiered\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: PostHog\n  ServiceCategory: Product Analytics\n  ProviderName: PostHog\n  PublisherName: PostHog\n  BillingCurrency: USD\nmeters:\n  - name: captured_events\n    unit: event\n    aggregation: sum\n\
  \  - name: session_replays\n    unit: replay\n    aggregation: sum\n  - name: feature_flag_requests\n    unit: request\n    aggregation: sum\n  - name: experiments\n    unit: experiment\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track PostHog consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/posthog/refs/heads/main/finops/posthog-finops.yml
sources:
- https://posthog.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Product Analytics
---
