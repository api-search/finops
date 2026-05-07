---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: litmus-instant-openapi.yml
  format: yaml
  label: Litmus Instant API
  slug: litmus-instant-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/litmus/refs/heads/main/openapi/litmus-instant-openapi.yml
- filename: litmus-legacy-previews-openapi.yml
  format: yaml
  label: Litmus Legacy Previews API
  slug: litmus-legacy-previews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/litmus/refs/heads/main/openapi/litmus-legacy-previews-openapi.yml
- filename: litmus-email-analytics-openapi.yml
  format: yaml
  label: Litmus Email Analytics API
  slug: litmus-email-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/litmus/refs/heads/main/openapi/litmus-email-analytics-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  - Credit
  pricingCategory: Subscription + Add-Ons
description: 'FOCUS-aligned FinOps for Litmus: enterprise SaaS with one base subscription plus opt-in add-on subscriptions (Deliverability, Sender Certification, Competitive Intel, Email Guardian, Mailcharts). Litmus Instant API access is partner-program-gated. Pricing is custom; charges land as monthly or annual subscription invoices rather than per-call usage.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Litmus Software, Inc.
  ProviderName: Litmus
  PublisherName: Litmus Software, Inc.
  ServiceCategory: Email Testing / Marketing Tools
  ServiceName: Litmus
layout: finops
meters:
- aggregation: count
  dimensions:
  - contract
  name: enterprise_subscription
  unit: contract
- aggregation: count
  dimensions:
  - addon
  - contract
  name: addon_subscriptions
  unit: contract
- aggregation: sum
  dimensions:
  - subaccount
  - email_client
  name: email_previews
  unit: preview
- aggregation: sum
  dimensions:
  - endpoint
  - partner_app
  name: instant_api_calls
  unit: request
- aggregation: count
  dimensions:
  - subaccount
  name: full_users
  unit: seat
name: Litmus Finops
provider_name: Litmus
provider_slug: litmus
publisher_name: Litmus Software, Inc.
service_category: Email Testing / Marketing Tools
slug: litmus-finops
source_filename: litmus-finops.yml
source_heading: FinOps Profile
source_url: https://www.litmus.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Litmus\nproviderId: litmus\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Email Testing\n  - Marketing Tools\n  - Developer Tools\ndescription: 'FOCUS-aligned FinOps for Litmus: enterprise SaaS with one base subscription plus opt-in\n  add-on subscriptions (Deliverability, Sender Certification, Competitive Intel, Email Guardian, Mailcharts).\n  Litmus Instant API access is partner-program-gated. Pricing is custom; charges land as monthly or annual\n  subscription invoices rather than per-call usage.'\nsources:\n  - https://www.litmus.com/pricing\n  - https://docs.litmus.com/instant\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Litmus Software, Inc.\nserviceCategory: Email Testing / Marketing Tools\nbillingModel:\n  pricingCategory: Subscription + Add-Ons\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Litmus\n  ServiceCategory: Email Testing / Marketing Tools\n  ProviderName: Litmus\n  PublisherName: Litmus Software, Inc.\n  InvoiceIssuerName: Litmus Software, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: enterprise_subscription\n    unit: contract\n    aggregation: count\n    dimensions:\n      - contract\n  - name: addon_subscriptions\n    unit: contract\n    aggregation: count\n    dimensions:\n      - addon\n      - contract\n  - name: email_previews\n    unit: preview\n    aggregation: sum\n    dimensions:\n      - subaccount\n      - email_client\n  - name: instant_api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - partner_app\n  - name: full_users\n \
  \   unit: seat\n    aggregation: count\n    dimensions:\n      - subaccount\nprinciples:\n  - name: Visibility\n    description: Track preview / API usage in the Litmus admin and via partner reporting; cross-reference\n      against Litmus invoices for the Enterprise subscription and each active add-on.\n  - name: Allocation\n    description: Use Litmus subaccounts to scope usage to brands, business units, or campaigns; allocate\n      the Enterprise subscription cost by subaccount activity.\n  - name: Optimization\n    description: Cull unused full-user seats; review add-on ROI annually (Deliverability vs Sender Certification\n      vs Email Guardian); for partner integrations, batch preview captures and reuse email_guids within\n      the 48-hour upload window.\n  - name: Accountability\n    description: Assign a Litmus contract owner who reviews subaccount usage and add-on consumption ahead\n      of each renewal; partners running Instant API integrations report usage back to that owner.\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/litmus/refs/heads/main/finops/litmus-finops.yml
sources:
- https://www.litmus.com/pricing
- https://docs.litmus.com/instant
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Email Testing
- Marketing Tools
- Developer Tools
---
