---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Bookings API
  slug: cal-com-bookings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Event Types API
  slug: cal-com-event-types-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Schedules API
  slug: cal-com-schedules-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Availability API
  slug: cal-com-availability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Slots API
  slug: cal-com-slots-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Webhooks API
  slug: cal-com-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com OAuth & Auth API
  slug: cal-com-oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Teams API
  slug: cal-com-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Organizations API
  slug: cal-com-organizations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Out-of-Office API
  slug: cal-com-ooo-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Conferencing API
  slug: cal-com-conferencing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Destination Calendars API
  slug: cal-com-destination-calendars-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
- filename: cal-com-openapi.json
  format: json
  label: Cal.com Atoms (Platform)
  slug: cal-com-atoms-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/openapi/cal-com-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription (Per Seat) + Platform Volume
description: FOCUS-aligned FinOps profile for Cal.com. The managed cloud bills per-user monthly across Free, Teams ($12), Organizations ($28), and Enterprise (custom). The Cal.com Platform (Atoms / managed users) is sold separately, typically priced on managed-user volume. Self-hosted has no platform fees.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cal.com, Inc.
  ProviderName: Cal.com
  PublisherName: Cal.com, Inc.
  ServiceCategory: Productivity
  ServiceName: Cal.com
layout: finops
meters:
- aggregation: sum
  description: Per-user monthly subscription. Teams $12, Organizations $28, Enterprise contract.
  dimensions:
  - account
  - team
  - plan
  name: user_seats
  unit: seat
- aggregation: sum
  description: Cal.com Platform managed-user volume meter for embedded SaaS deployments.
  dimensions:
  - oauth_client
  - account
  name: platform_managed_users
  unit: managed_user
name: Cal Com Finops
provider_name: Cal.com
provider_slug: cal-com
publisher_name: Cal.com, Inc.
service_category: Productivity
slug: cal-com-finops
source_filename: cal-com-finops.yml
source_heading: FinOps Profile
source_url: https://cal.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Cal.com\nproviderId: cal-com\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Scheduling\n- Calendar\n- Open Source\n- Booking\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Cal.com. The managed cloud bills per-user\n  monthly across Free, Teams ($12), Organizations ($28), and Enterprise (custom). The\n  Cal.com Platform (Atoms / managed users) is sold separately, typically priced on\n  managed-user volume. Self-hosted has no platform fees.\nsources:\n- https://cal.com/pricing\n- https://cal.com/docs/platform\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Cal.com, Inc.\nserviceCategory: Productivity\nbillingModel:\n  pricingCategory: Subscription (Per Seat) + Platform Volume\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Usage\n  - Adjustment\nfocusColumns:\n  ServiceName: Cal.com\n  ServiceCategory: Productivity\n  ProviderName: Cal.com\n  PublisherName: Cal.com, Inc.\n  InvoiceIssuerName: Cal.com, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: user_seats\n  description: Per-user monthly subscription. Teams $12, Organizations $28, Enterprise\n    contract.\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - account\n  - team\n  - plan\n- name: platform_managed_users\n  description: Cal.com Platform managed-user volume meter for embedded SaaS deployments.\n  unit: managed_user\n  aggregation: sum\n  dimensions:\n  - oauth_client\n  - account\nprinciples:\n- name: Visibility\n  description: Inventory active users in the Cal.com admin panel; track Platform\
  \ managed-user\n    counts separately.\n- name: Allocation\n  description: Allocate user seats by team membership; allocate Platform spend to the SaaS\n    product embedding scheduling.\n- name: Optimization\n  description: Reclaim seats from inactive users; choose annual billing for the 25% discount;\n    consider self-hosting for very large deployments where engineering capacity is available.\n- name: Accountability\n  description: Assign an owner per Cal.com organization; review Platform managed-user count\n    against forecast.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cal-com/refs/heads/main/finops/cal-com-finops.yml
sources:
- https://cal.com/pricing
- https://cal.com/docs/platform
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Scheduling
- Calendar
- Open Source
- Booking
- FinOps
- Cost Management
- FOCUS
---
