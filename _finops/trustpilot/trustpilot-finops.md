---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: trustpilot-business-units-openapi.yml
  format: yaml
  label: Trustpilot Business Units API
  slug: trustpilot-business-units-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustpilot/refs/heads/main/openapi/trustpilot-business-units-openapi.yml
- filename: trustpilot-service-reviews-openapi.yml
  format: yaml
  label: Trustpilot Service Reviews API
  slug: trustpilot-service-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustpilot/refs/heads/main/openapi/trustpilot-service-reviews-openapi.yml
- filename: trustpilot-invitation-openapi.yml
  format: yaml
  label: Trustpilot Invitation API
  slug: trustpilot-invitation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustpilot/refs/heads/main/openapi/trustpilot-invitation-openapi.yml
- filename: trustpilot-product-reviews-openapi.yml
  format: yaml
  label: Trustpilot Product Reviews API
  slug: trustpilot-product-reviews-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/trustpilot/refs/heads/main/openapi/trustpilot-product-reviews-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  pricingCategory: Tiered Subscription
description: FOCUS-aligned FinOps for Trustpilot's tiered SaaS — annual prepaid subscriptions priced per domain (Free, $99 Starter, $319 Plus, $799 Premium, custom Enterprise) with seat, widget, integration, and review-invitation caps per tier and a separate API add-on on Premium/Enterprise.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Trustpilot A/S
  ProviderName: Trustpilot
  PublisherName: Trustpilot A/S
  ServiceCategory: Reviews & Reputation SaaS
  ServiceName: Trustpilot Business
layout: finops
meters:
- aggregation: sum
  description: Annual subscription per domain at the chosen tier (Free, Starter $99/mo, Plus $319/mo, Premium $799/mo, Enterprise custom).
  dimensions:
  - tier
  - domain
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Monthly review invitations sent (50 Free, 100 Starter, 300 Plus, 1000 Premium, unlimited Enterprise).
  dimensions:
  - tier
  - domain
  name: review_invitations
  unit: invitation
- aggregation: max
  description: Active business users on the account.
  dimensions:
  - tier
  name: seats
  unit: seat
- aggregation: max
  description: Domains under management (1 Starter, up to 3 Plus, unlimited Premium/Enterprise).
  dimensions:
  - tier
  name: domains
  unit: domain
- aggregation: sum
  description: API access add-on, available on Premium and Enterprise tiers.
  dimensions:
  - tier
  name: api_addon
  unit: month
name: Trustpilot Finops
provider_name: Trustpilot
provider_slug: trustpilot
publisher_name: Trustpilot A/S
service_category: Reviews & Reputation SaaS
slug: trustpilot-finops
source_filename: trustpilot-finops.yml
source_heading: FinOps Profile
source_url: https://business.trustpilot.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Trustpilot\nproviderId: trustpilot\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Reviews\n  - Reputation\n  - SaaS\n  - FinOps\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Trustpilot's tiered SaaS — annual prepaid subscriptions priced per\n  domain (Free, $99 Starter, $319 Plus, $799 Premium, custom Enterprise) with seat, widget, integration,\n  and review-invitation caps per tier and a separate API add-on on Premium/Enterprise.\nsources:\n  - https://business.trustpilot.com/pricing\n  - https://developers.trustpilot.com/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Trustpilot A/S\nserviceCategory: Reviews & Reputation SaaS\nbillingModel:\n\
  \  pricingCategory: Tiered Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\nfocusColumns:\n  ServiceName: Trustpilot Business\n  ServiceCategory: Reviews & Reputation SaaS\n  ProviderName: Trustpilot\n  PublisherName: Trustpilot A/S\n  InvoiceIssuerName: Trustpilot A/S\n  BillingCurrency: USD\nmeters:\n  - name: subscription_fee\n    description: Annual subscription per domain at the chosen tier (Free, Starter $99/mo, Plus $319/mo,\n      Premium $799/mo, Enterprise custom).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - domain\n  - name: review_invitations\n    description: Monthly review invitations sent (50 Free, 100 Starter, 300 Plus, 1000 Premium, unlimited\n      Enterprise).\n    unit: invitation\n    aggregation: sum\n    dimensions:\n      - tier\n      - domain\n  - name: seats\n    description: Active business users on the account.\n    unit: seat\n    aggregation: max\n    dimensions:\n  \
  \    - tier\n  - name: domains\n    description: Domains under management (1 Starter, up to 3 Plus, unlimited Premium/Enterprise).\n    unit: domain\n    aggregation: max\n    dimensions:\n      - tier\n  - name: api_addon\n    description: API access add-on, available on Premium and Enterprise tiers.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Track the per-domain tier subscription on the Trustpilot invoice and monitor invitation\n      send volume in the Business app to confirm you stay within the monthly cap of your tier.\n  - name: Allocation\n    description: Allocate spend per domain (each Plus/Premium domain is its own line) and per business\n      unit; review-invitation volume can be attributed to the same domain dimension.\n  - name: Optimization\n    description: Right-size the tier (Starter caps at 100 invitations, Plus at 300, Premium at 1000) and\n      avoid the Premium/Enterprise API add-on unless\
  \ you actually need programmatic access; consume reviews\n      via webhooks rather than polling to avoid scaling pressure on the API tier.\n  - name: Accountability\n    description: Assign a marketing or CX owner per domain who controls invitation sends, integrations,\n      and renewal of the 12-month prepaid contract.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/trustpilot/refs/heads/main/finops/trustpilot-finops.yml
sources:
- https://business.trustpilot.com/pricing
- https://developers.trustpilot.com/
specification: FinOps Framework
tags:
- Reviews
- Reputation
- SaaS
- FinOps
- FOCUS
---
