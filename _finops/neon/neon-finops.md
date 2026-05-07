---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: neon-management-api-openapi.yml
  format: yaml
  label: Neon Management API
  slug: management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neon/refs/heads/main/openapi/neon-management-api-openapi.yml
- filename: neon-auth-webhooks-asyncapi.yml
  format: yaml
  label: Neon Auth
  slug: auth
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/neon/refs/heads/main/asyncapi/neon-auth-webhooks-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay-As-You-Go Per Compute Hour + Storage
description: FOCUS-aligned FinOps for Neon.
focus_columns:
  BillingCurrency: USD
  ProviderName: Neon
  PublisherName: Neon
  ServiceCategory: Serverless Postgres
  ServiceName: Neon
layout: finops
meters:
- aggregation: sum
  dimensions:
  - project
  - branch
  name: compute_hours
  unit: CU-hour
- aggregation: max
  name: storage
  unit: GB-month
- aggregation: sum
  name: egress
  unit: GB
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: max
  name: instant_restore
  unit: GB-month
- aggregation: sum
  name: private_networking
  unit: GB
name: Neon Finops
provider_name: Neon
provider_slug: neon
publisher_name: Neon
service_category: Serverless Postgres
slug: neon-finops
source_filename: neon-finops.yml
source_heading: FinOps Profile
source_url: https://neon.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Neon\nproviderId: neon\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Serverless Postgres\ndescription: FOCUS-aligned FinOps for Neon.\nsources:\n  - https://neon.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Neon\nserviceCategory: Serverless Postgres\nbillingModel:\n  pricingCategory: Pay-As-You-Go Per Compute Hour + Storage\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Neon\n  ServiceCategory: Serverless Postgres\n  ProviderName: Neon\n  PublisherName: Neon\n  BillingCurrency: USD\nmeters:\n  - name: compute_hours\n    unit: CU-hour\n    aggregation: sum\n    dimensions:\n\
  \      - project\n      - branch\n  - name: storage\n    unit: GB-month\n    aggregation: max\n  - name: egress\n    unit: GB\n    aggregation: sum\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name: instant_restore\n    unit: GB-month\n    aggregation: max\n  - name: private_networking\n    unit: GB\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Neon consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/neon/refs/heads/main/finops/neon-finops.yml
sources:
- https://neon.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Serverless Postgres
---
