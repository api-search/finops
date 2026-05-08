---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: optimizely-web-experimentation-openapi.yml
  format: yaml
  label: Optimizely Web Experimentation REST API
  slug: web-experimentation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-web-experimentation-openapi.yml
- filename: optimizely-feature-experimentation-openapi.yml
  format: yaml
  label: Optimizely Feature Experimentation REST API
  slug: feature-experimentation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-feature-experimentation-openapi.yml
- filename: optimizely-campaign-openapi.yml
  format: yaml
  label: Optimizely Campaign REST API
  slug: campaign
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-campaign-openapi.yml
- filename: optimizely-content-delivery-openapi.yml
  format: yaml
  label: Optimizely Content Delivery API
  slug: content-delivery
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-content-delivery-openapi.yml
- filename: optimizely-content-management-openapi.yml
  format: yaml
  label: Optimizely Content Management API
  slug: content-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-content-management-openapi.yml
- filename: optimizely-graph-openapi.yml
  format: yaml
  label: Optimizely Graph API
  slug: graph
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-graph-openapi.yml
- filename: optimizely-data-platform-openapi.yml
  format: yaml
  label: Optimizely Data Platform REST API
  slug: data-platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-data-platform-openapi.yml
- filename: optimizely-cmp-openapi.yml
  format: yaml
  label: Optimizely CMP Open REST API
  slug: cmp
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-cmp-openapi.yml
- filename: optimizely-commerce-service-openapi.yml
  format: yaml
  label: Optimizely Commerce Service API
  slug: commerce-service
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/openapi/optimizely-commerce-service-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Modular Annual Subscription (MTU/Sessions/Impressions)
description: FOCUS-aligned FinOps for Optimizely.
focus_columns:
  BillingCurrency: USD
  ProviderName: Optimizely
  PublisherName: Optimizely
  ServiceCategory: Digital Experience Platform
  ServiceName: Optimizely
layout: finops
meters:
- aggregation: max
  name: monthly_tracked_users
  unit: MTU
- aggregation: sum
  name: monthly_impressions
  unit: impression
- aggregation: max
  name: experiments
  unit: experiment-month
- aggregation: sum
  name: feature_flag_evaluations
  unit: evaluation
name: Optimizely Finops
provider_name: Optimizely
provider_slug: optimizely
publisher_name: Optimizely
service_category: Digital Experience Platform
slug: optimizely-finops
source_filename: optimizely-finops.yml
source_heading: FinOps Profile
source_url: https://www.optimizely.com/plans/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Optimizely\nproviderId: optimizely\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Digital Experience Platform\ndescription: FOCUS-aligned FinOps for Optimizely.\nsources:\n  - https://www.optimizely.com/plans/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Optimizely\nserviceCategory: Digital Experience Platform\nbillingModel:\n  pricingCategory: Modular Annual Subscription (MTU/Sessions/Impressions)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Optimizely\n  ServiceCategory: Digital Experience Platform\n  ProviderName: Optimizely\n  PublisherName: Optimizely\n  BillingCurrency: USD\nmeters:\n\
  \  - name: monthly_tracked_users\n    unit: MTU\n    aggregation: max\n  - name: monthly_impressions\n    unit: impression\n    aggregation: sum\n  - name: experiments\n    unit: experiment-month\n    aggregation: max\n  - name: feature_flag_evaluations\n    unit: evaluation\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Optimizely consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/optimizely/refs/heads/main/finops/optimizely-finops.yml
sources:
- https://www.optimizely.com/plans/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Digital Experience Platform
---
