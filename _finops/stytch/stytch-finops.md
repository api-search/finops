---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: stytch-consumer-openapi.yml
  format: yaml
  label: Stytch Consumer Authentication API
  slug: stytch-consumer-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/openapi/stytch-consumer-openapi.yml
- filename: stytch-b2b-openapi.yml
  format: yaml
  label: Stytch B2B Authentication API
  slug: stytch-b2b-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/openapi/stytch-b2b-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Pay As You Go + Per-Connection
description: FOCUS-aligned FinOps for Stytch.
focus_columns:
  BillingCurrency: USD
  ProviderName: Stytch
  PublisherName: Stytch
  ServiceCategory: B2B Identity
  ServiceName: Stytch
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: max
  name: sso_scim_connections
  unit: connection-month
- aggregation: sum
  name: m2m_tokens
  unit: token
- aggregation: sum
  name: fraud_fingerprints
  unit: fingerprint
name: Stytch Finops
provider_name: Stytch
provider_slug: stytch
publisher_name: Stytch
service_category: B2B Identity
slug: stytch-finops
source_filename: stytch-finops.yml
source_heading: FinOps Profile
source_url: https://stytch.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Stytch\nproviderId: stytch\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - B2B Identity\ndescription: FOCUS-aligned FinOps for Stytch.\nsources:\n  - https://stytch.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Stytch\nserviceCategory: B2B Identity\nbillingModel:\n  pricingCategory: Pay As You Go + Per-Connection\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Stytch\n  ServiceCategory: B2B Identity\n  ProviderName: Stytch\n  PublisherName: Stytch\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n  - name: sso_scim_connections\n\
  \    unit: connection-month\n    aggregation: max\n  - name: m2m_tokens\n    unit: token\n    aggregation: sum\n  - name: fraud_fingerprints\n    unit: fingerprint\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Stytch consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/stytch/refs/heads/main/finops/stytch-finops.yml
sources:
- https://stytch.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- B2B Identity
---
