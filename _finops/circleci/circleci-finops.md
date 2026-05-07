---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: circleci-rest-api-v2-openapi.yml
  format: yaml
  label: CircleCI REST API V2
  slug: rest-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/openapi/circleci-rest-api-v2-openapi.yml
- filename: circleci-rest-api-v1-openapi.yml
  format: yaml
  label: CircleCI REST API V1
  slug: rest-api-v1
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/openapi/circleci-rest-api-v1-openapi.yml
- filename: circleci-runner-api-openapi.yml
  format: yaml
  label: CircleCI Self-Hosted Runner API
  slug: runner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/openapi/circleci-runner-api-openapi.yml
- filename: circleci-webhooks-asyncapi.yml
  format: yaml
  label: CircleCI Webhooks
  slug: webhooks
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/asyncapi/circleci-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Subscription + Credit-Based
description: FOCUS-aligned FinOps for CircleCI.
focus_columns:
  BillingCurrency: USD
  ProviderName: CircleCI
  PublisherName: CircleCI
  ServiceCategory: CI/CD
  ServiceName: CircleCI
layout: finops
meters:
- aggregation: sum
  dimensions:
  - resource_class
  - executor
  name: credits_consumed
  unit: credit
- aggregation: sum
  name: build_minutes
  unit: minute
- aggregation: max
  name: active_users
  unit: user-month
- aggregation: max
  name: storage
  unit: GB-month
name: Circleci Finops
provider_name: CircleCI
provider_slug: circleci
publisher_name: CircleCI
service_category: CI/CD
slug: circleci-finops
source_filename: circleci-finops.yml
source_heading: FinOps Profile
source_url: https://circleci.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CircleCI\nproviderId: circleci\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - CI/CD\ndescription: FOCUS-aligned FinOps for CircleCI.\nsources:\n  - https://circleci.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CircleCI\nserviceCategory: CI/CD\nbillingModel:\n  pricingCategory: Subscription + Credit-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: CircleCI\n  ServiceCategory: CI/CD\n  ProviderName: CircleCI\n  PublisherName: CircleCI\n  BillingCurrency: USD\nmeters:\n  - name: credits_consumed\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - resource_class\n\
  \      - executor\n  - name: build_minutes\n    unit: minute\n    aggregation: sum\n  - name: active_users\n    unit: user-month\n    aggregation: max\n  - name: storage\n    unit: GB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track CircleCI consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circleci/refs/heads/main/finops/circleci-finops.yml
sources:
- https://circleci.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- CI/CD
---
