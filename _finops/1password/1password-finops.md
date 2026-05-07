---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 1password-connect-openapi.yml
  format: yaml
  label: 1Password Connect Server API
  slug: 1password-connect-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/openapi/1password-connect-openapi.yml
- filename: 1password-events-openapi.yml
  format: yaml
  label: 1Password Events API
  slug: 1password-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/openapi/1password-events-openapi.yml
- filename: 1password-partnership-openapi.yml
  format: yaml
  label: 1Password Partnership API
  slug: 1password-partnership-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/openapi/1password-partnership-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  - Refund
  pricingCategory: Subscription
description: FOCUS-aligned FinOps for 1Password — per-seat, per-month subscription billing across business plans. APIs (Connect, Events, SCIM, Service Accounts) are entitlements of the seat plan rather than metered services; there is no per-call charge.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: AgileBits Inc.
  PricingCategory: Subscription
  PricingUnit: seat-month
  ProviderName: 1Password
  PublisherName: AgileBits Inc.
  ServiceCategory: Identity
  ServiceName: 1Password
layout: finops
meters:
- aggregation: sum
  description: Active billable user seats per month (Business, Teams Starter, Individual, Families).
  dimensions:
  - plan
  - billing_period
  - region
  name: seat_month
  unit: seat
- aggregation: count
  description: Flat family-plan billing unit (single charge regardless of family size up to 5).
  dimensions:
  - plan
  name: family_account_month
  unit: month
- aggregation: sum
  description: Audit / sign-in event API requests (entitlement metric — not separately billed but governed by 600/min and 30k/hour ceilings).
  dimensions:
  - endpoint
  - account
  name: events_api_calls
  unit: request
- aggregation: count
  description: Number of self-hosted Connect Server instances (entitlement metric for fair-use planning).
  dimensions:
  - account
  name: connect_servers_active
  unit: instance
name: 1Password Finops
provider_name: 1Password
provider_slug: 1password
publisher_name: AgileBits Inc.
service_category: Identity
slug: 1password-finops
source_filename: 1password-finops.yml
source_heading: FinOps Profile
source_url: https://1password.com/business-pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: 1Password\nproviderId: 1password\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Password Manager\n  - Security\n  - Secrets\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for 1Password — per-seat, per-month subscription billing across business\n  plans. APIs (Connect, Events, SCIM, Service Accounts) are entitlements of the seat plan rather than\n  metered services; there is no per-call charge.\nsources:\n  - https://1password.com/business-pricing\n  - https://developer.1password.com/docs/events-api/rate-limits/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: AgileBits Inc.\nserviceCategory:\
  \ Identity\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: 1Password\n  ServiceCategory: Identity\n  ProviderName: 1Password\n  PublisherName: AgileBits Inc.\n  InvoiceIssuerName: AgileBits Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\n  PricingUnit: seat-month\nmeters:\n  - name: seat_month\n    description: Active billable user seats per month (Business, Teams Starter, Individual, Families).\n    unit: seat\n    aggregation: sum\n    dimensions:\n      - plan\n      - billing_period\n      - region\n  - name: family_account_month\n    description: Flat family-plan billing unit (single charge regardless of family size up to 5).\n    unit: month\n    aggregation: count\n    dimensions:\n      - plan\n  - name: events_api_calls\n    description: Audit / sign-in event API requests\
  \ (entitlement metric — not separately billed but governed\n      by 600/min and 30k/hour ceilings).\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - account\n  - name: connect_servers_active\n    description: Number of self-hosted Connect Server instances (entitlement metric for fair-use planning).\n    unit: instance\n    aggregation: count\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Use the 1Password admin console seat report and the Events API to track active vs licensed\n      seats and identify dormant accounts before renewal.\n  - name: Allocation\n    description: Tag vaults and groups by team / cost center; use the Business plan's group structure to\n      attribute seat costs to consuming teams.\n  - name: Optimization\n    description: Right-size by deactivating unused seats before the annual renewal anniversary; consolidate\n      family-plan licenses into business plans only when individual usage\
  \ justifies the shift.\n  - name: Accountability\n    description: Designate a security/IT owner for license counts and a finance owner for the annual renewal;\n      review seat utilization quarterly via Watchtower and SCIM provisioning logs.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/1password/refs/heads/main/finops/1password-finops.yml
sources:
- https://1password.com/business-pricing
- https://developer.1password.com/docs/events-api/rate-limits/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Password Manager
- Security
- Secrets
- FinOps
- FOCUS
---
