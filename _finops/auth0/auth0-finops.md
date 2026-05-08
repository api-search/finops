---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: auth0-api-openapi.yml
  format: yaml
  label: Auth0 Management API
  slug: auth0-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/auth0/refs/heads/main/openapi/auth0-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-MAU + Tier
description: FOCUS-aligned FinOps for Auth0.
focus_columns:
  BillingCurrency: USD
  ProviderName: Auth0
  PublisherName: Auth0
  ServiceCategory: Identity
  ServiceName: Auth0
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: sum
  name: m2m_tokens
  unit: token
- aggregation: max
  name: enterprise_connections
  unit: connection-month
- aggregation: max
  name: organizations
  unit: org-month
name: Auth0 Finops
provider_name: Auth0
provider_slug: auth0
publisher_name: Auth0
service_category: Identity
slug: auth0-finops
source_filename: auth0-finops.yml
source_heading: FinOps Profile
source_url: https://auth0.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Auth0\nproviderId: auth0\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Identity\ndescription: FOCUS-aligned FinOps for Auth0.\nsources:\n  - https://auth0.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Auth0\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Per-MAU + Tier\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Auth0\n  ServiceCategory: Identity\n  ProviderName: Auth0\n  PublisherName: Auth0\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name: m2m_tokens\n    unit: token\n    aggregation: sum\n  -\
  \ name: enterprise_connections\n    unit: connection-month\n    aggregation: max\n  - name: organizations\n    unit: org-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Auth0 consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size tier; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/auth0/refs/heads/main/finops/auth0-finops.yml
sources:
- https://auth0.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Identity
---
