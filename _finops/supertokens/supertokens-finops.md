---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: supertokens-core-driver-interface-openapi.yml
  format: yaml
  label: SuperTokens Core Driver Interface
  slug: core-driver-interface
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/supertokens/refs/heads/main/openapi/supertokens-core-driver-interface-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Self-hosted Free + Per-MAU Add-ons
description: FOCUS-aligned FinOps for SuperTokens.
focus_columns:
  BillingCurrency: USD
  ProviderName: SuperTokens
  PublisherName: SuperTokens
  ServiceCategory: Identity
  ServiceName: SuperTokens
layout: finops
meters:
- aggregation: max
  name: monthly_active_users
  unit: MAU
- aggregation: max
  name: mfa_addon_mau
  unit: MAU
- aggregation: max
  name: account_linking_addon_mau
  unit: MAU
- aggregation: max
  name: dashboard_users
  unit: user-month
name: Supertokens Finops
provider_name: SuperTokens
provider_slug: supertokens
publisher_name: SuperTokens
service_category: Identity
slug: supertokens-finops
source_filename: supertokens-finops.yml
source_heading: FinOps Profile
source_url: https://supertokens.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SuperTokens\nproviderId: supertokens\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Identity\ndescription: FOCUS-aligned FinOps for SuperTokens.\nsources:\n  - https://supertokens.com/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SuperTokens\nserviceCategory: Identity\nbillingModel:\n  pricingCategory: Self-hosted Free + Per-MAU Add-ons\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: SuperTokens\n  ServiceCategory: Identity\n  ProviderName: SuperTokens\n  PublisherName: SuperTokens\n  BillingCurrency: USD\nmeters:\n  - name: monthly_active_users\n    unit: MAU\n    aggregation: max\n\
  \  - name: mfa_addon_mau\n    unit: MAU\n    aggregation: max\n  - name: account_linking_addon_mau\n    unit: MAU\n    aggregation: max\n  - name: dashboard_users\n    unit: user-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track SuperTokens consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/supertokens/refs/heads/main/finops/supertokens-finops.yml
sources:
- https://supertokens.com/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Identity
---
