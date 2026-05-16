---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger-v3.v3.json
  format: json
  label: Jira Cloud Platform REST API
  slug: jira-cloud-platform-rest-api
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/platform/swagger-v3.v3.json
- filename: swagger.v3.json
  format: json
  label: Jira Software Cloud REST API
  slug: jira-software-cloud-rest-api
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/software/swagger.v3.json
- filename: swagger.v3.json
  format: json
  label: Jira Service Management REST API
  slug: jira-service-management-rest-api
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/service-desk/swagger.v3.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription (Tiered)
description: FOCUS-aligned FinOps for Jira Cloud.
focus_columns:
  BillingCurrency: USD
  ProviderName: Jira Cloud
  PublisherName: Jira Cloud
  ServiceCategory: Project Management
  ServiceName: Jira Cloud
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
name: Jira Finops
provider_name: Jira
provider_slug: jira
publisher_name: Jira Cloud
service_category: Project Management
slug: jira-finops
source_filename: jira-finops.yml
source_heading: FinOps Profile
source_url: https://www.atlassian.com/software/jira/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Jira Cloud\nproviderId: jira\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Project Management\ndescription: FOCUS-aligned FinOps for Jira Cloud.\nsources:\n  - https://www.atlassian.com/software/jira/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Jira Cloud\nserviceCategory: Project Management\nbillingModel:\n  pricingCategory: Per-User Subscription (Tiered)\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Jira Cloud\n  ServiceCategory: Project Management\n  ProviderName: Jira Cloud\n  PublisherName: Jira Cloud\n  BillingCurrency: USD\nmeters:\n  - name: user_seats\n    unit: seat-month\n\
  \    aggregation: max\n    dimensions:\n      - plan\n  - name: storage\n    unit: GB-month\n    aggregation: max\n  - name: atlassian_intelligence_uses\n    unit: use\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Jira Cloud consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jira/refs/heads/main/finops/jira-finops.yml
sources:
- https://www.atlassian.com/software/jira/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Project Management
---
