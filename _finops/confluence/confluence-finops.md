---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.v3.json
  format: json
  label: Confluence Cloud REST API v1
  slug: ''
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/confluence/swagger.v3.json
- filename: openapi.yaml
  format: yaml
  label: Confluence Cloud REST API v2
  slug: ''
  spec_type: OpenAPI
  url: https://developer.atlassian.com/cloud/confluence/rest/v2/api-spec/
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription (Tiered)
description: FOCUS-aligned FinOps for Confluence Cloud.
focus_columns:
  BillingCurrency: USD
  ProviderName: Confluence Cloud
  PublisherName: Confluence Cloud
  ServiceCategory: Wiki
  ServiceName: Confluence Cloud
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: max
  name: storage
  unit: GB-month
- aggregation: sum
  name: atlassian_intelligence_uses
  unit: use
name: Confluence Finops
provider_name: Confluence
provider_slug: confluence
publisher_name: Confluence Cloud
service_category: Wiki
slug: confluence-finops
source_filename: confluence-finops.yml
source_heading: FinOps Profile
source_url: https://www.atlassian.com/software/confluence/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Confluence Cloud\nproviderId: confluence\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Wiki\ndescription: FOCUS-aligned FinOps for Confluence Cloud.\nsources:\n  - https://www.atlassian.com/software/confluence/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Confluence Cloud\nserviceCategory: Wiki\nbillingModel:\n  pricingCategory: Per-User Subscription (Tiered)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Confluence Cloud\n  ServiceCategory: Wiki\n  ProviderName: Confluence Cloud\n  PublisherName: Confluence Cloud\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit:\
  \ seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: storage\n    unit: GB-month\n    aggregation: max\n  - name: atlassian_intelligence_uses\n    unit: use\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Confluence Cloud consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/confluence/refs/heads/main/finops/confluence-finops.yml
sources:
- https://www.atlassian.com/software/confluence/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Wiki
---
