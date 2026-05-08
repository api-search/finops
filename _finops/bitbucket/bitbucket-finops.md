---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: bitbucket-cloud-rest-api-openapi.json
  format: json
  label: Bitbucket Cloud REST API
  slug: bitbucket-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/bitbucket/refs/heads/main/openapi/bitbucket-cloud-rest-api-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-User Subscription
description: FOCUS-aligned FinOps for Bitbucket Cloud.
focus_columns:
  BillingCurrency: USD
  ProviderName: Bitbucket Cloud
  PublisherName: Bitbucket Cloud
  ServiceCategory: Source Control + CI/CD
  ServiceName: Bitbucket Cloud
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  name: user_seats
  unit: seat-month
- aggregation: sum
  name: build_minutes
  unit: minute
- aggregation: max
  name: git_lfs_storage
  unit: GB-month
- aggregation: max
  name: deployment_environments
  unit: env-month
name: Bitbucket Finops
provider_name: Bitbucket
provider_slug: bitbucket
publisher_name: Bitbucket Cloud
service_category: Source Control + CI/CD
slug: bitbucket-finops
source_filename: bitbucket-finops.yml
source_heading: FinOps Profile
source_url: https://www.atlassian.com/software/bitbucket/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Bitbucket Cloud\nproviderId: bitbucket\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Source Control + CI/CD\ndescription: FOCUS-aligned FinOps for Bitbucket Cloud.\nsources:\n  - https://www.atlassian.com/software/bitbucket/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Bitbucket Cloud\nserviceCategory: Source Control + CI/CD\nbillingModel:\n  pricingCategory: Per-User Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Bitbucket Cloud\n  ServiceCategory: Source Control + CI/CD\n  ProviderName: Bitbucket Cloud\n  PublisherName: Bitbucket Cloud\n  BillingCurrency: USD\nmeters:\n\
  \  - name: user_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n  - name: build_minutes\n    unit: minute\n    aggregation: sum\n  - name: git_lfs_storage\n    unit: GB-month\n    aggregation: max\n  - name: deployment_environments\n    unit: env-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Bitbucket Cloud consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bitbucket/refs/heads/main/finops/bitbucket-finops.yml
sources:
- https://www.atlassian.com/software/bitbucket/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Source Control + CI/CD
---
