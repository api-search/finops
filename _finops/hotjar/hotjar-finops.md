---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hotjar-rest-api-openapi.yml
  format: yaml
  label: Hotjar REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hotjar/refs/heads/main/openapi/hotjar-rest-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription (Tiered by Sessions)
description: FOCUS-aligned FinOps for Hotjar (Contentsquare).
focus_columns:
  BillingCurrency: USD
  ProviderName: Hotjar (Contentsquare)
  PublisherName: Hotjar (Contentsquare)
  ServiceCategory: Digital Experience
  ServiceName: Hotjar (Contentsquare)
layout: finops
meters:
- aggregation: sum
  name: session_recordings
  unit: session
- aggregation: max
  name: heatmaps
  unit: heatmap-month
- aggregation: max
  name: surveys
  unit: survey
- aggregation: max
  name: user_seats
  unit: seat-month
name: Hotjar Finops
provider_name: hotjar
provider_slug: hotjar
publisher_name: Hotjar (Contentsquare)
service_category: Digital Experience
slug: hotjar-finops
source_filename: hotjar-finops.yml
source_heading: FinOps Profile
source_url: https://contentsquare.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Hotjar (Contentsquare)\nproviderId: hotjar\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Digital Experience\ndescription: FOCUS-aligned FinOps for Hotjar (Contentsquare).\nsources:\n  - https://contentsquare.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Hotjar (Contentsquare)\nserviceCategory: Digital Experience\nbillingModel:\n  pricingCategory: Subscription (Tiered by Sessions)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Hotjar (Contentsquare)\n  ServiceCategory: Digital Experience\n  ProviderName: Hotjar (Contentsquare)\n  PublisherName: Hotjar (Contentsquare)\n  BillingCurrency:\
  \ USD\nmeters:\n  - name: session_recordings\n    unit: session\n    aggregation: sum\n  - name: heatmaps\n    unit: heatmap-month\n    aggregation: max\n  - name: surveys\n    unit: survey\n    aggregation: max\n  - name: user_seats\n    unit: seat-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Hotjar (Contentsquare) consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hotjar/refs/heads/main/finops/hotjar-finops.yml
sources:
- https://contentsquare.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Digital Experience
---
