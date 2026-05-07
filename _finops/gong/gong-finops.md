---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gong-calls-openapi.yml
  format: yaml
  label: Gong Calls API
  slug: gong-calls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-calls-openapi.yml
- filename: gong-users-openapi.yml
  format: yaml
  label: Gong Users API
  slug: gong-users-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-users-openapi.yml
- filename: gong-stats-openapi.yml
  format: yaml
  label: Gong Stats API
  slug: gong-stats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-stats-openapi.yml
- filename: gong-crm-openapi.yml
  format: yaml
  label: Gong CRM API
  slug: gong-crm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-crm-openapi.yml
- filename: gong-engage-openapi.yml
  format: yaml
  label: Gong Engage API
  slug: gong-engage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-engage-openapi.yml
- filename: gong-settings-openapi.yml
  format: yaml
  label: Gong Settings API
  slug: gong-settings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-settings-openapi.yml
- filename: gong-library-openapi.yml
  format: yaml
  label: Gong Library API
  slug: gong-library-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-library-openapi.yml
- filename: gong-permissions-openapi.yml
  format: yaml
  label: Gong Permissions API
  slug: gong-permissions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-permissions-openapi.yml
- filename: gong-data-privacy-openapi.yml
  format: yaml
  label: Gong Data Privacy API
  slug: gong-data-privacy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-data-privacy-openapi.yml
- filename: gong-auditing-openapi.yml
  format: yaml
  label: Gong Auditing API
  slug: gong-auditing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-auditing-openapi.yml
- filename: gong-meetings-openapi.yml
  format: yaml
  label: Gong Meetings API
  slug: gong-meetings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-meetings-openapi.yml
- filename: gong-engagement-openapi.yml
  format: yaml
  label: Gong Engagement API
  slug: gong-engagement-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/openapi/gong-engagement-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Per-Seat Subscription + Platform Fee
description: 'FOCUS-aligned FinOps framing for Gong: per-seat subscription plus platform fee scaled by user-band tier. Specific rates are sales-led and not publicly posted.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Gong.io, Inc.
  ProviderName: Gong
  PublisherName: Gong.io, Inc.
  ServiceCategory: Revenue Intelligence
  ServiceName: Gong
layout: finops
meters:
- aggregation: max
  description: Active Gong-licensed seats (typically sales reps, sales managers, customer-success)
  dimensions:
  - role
  - team
  - product_module
  name: licensed_seats
  unit: seat
- aggregation: sum
  description: Annual platform fee scaled by user-band tier
  name: platform_fee
  unit: year
- aggregation: sum
  description: Calls recorded and transcribed (capacity-shaping, not direct billing)
  name: calls_recorded
  unit: call
- aggregation: sum
  description: API request volume against tenant quota
  name: api_requests
  unit: request
name: Gong Finops
provider_name: Gong
provider_slug: gong
publisher_name: Gong.io, Inc.
service_category: Revenue Intelligence (SaaS)
slug: gong-finops
source_filename: gong-finops.yml
source_heading: FinOps Profile
source_url: https://www.gong.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Gong\nproviderId: gong\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - FinOps\n  - FOCUS\n  - Revenue Intelligence\n  - SaaS\ndescription: 'FOCUS-aligned FinOps framing for Gong: per-seat subscription plus platform fee scaled by\n  user-band tier. Specific rates are sales-led and not publicly posted.'\nnotes: Reconcile when Gong publishes a public rate card.\nsources:\n  - https://www.gong.io/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Gong.io, Inc.\nserviceCategory: Revenue Intelligence (SaaS)\nbillingModel:\n  pricingCategory: Per-Seat Subscription + Platform Fee\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Purchase\n    - Adjustment\nfocusColumns:\n  ServiceName: Gong\n  ServiceCategory: Revenue Intelligence\n  ProviderName: Gong\n  PublisherName: Gong.io, Inc.\n  InvoiceIssuerName: Gong.io, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: licensed_seats\n    description: Active Gong-licensed seats (typically sales reps, sales managers, customer-success)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - role\n      - team\n      - product_module\n  - name: platform_fee\n    description: Annual platform fee scaled by user-band tier\n    unit: year\n    aggregation: sum\n  - name: calls_recorded\n    description: Calls recorded and transcribed (capacity-shaping, not direct billing)\n    unit: call\n    aggregation: sum\n  - name: api_requests\n    description: API request volume against tenant quota\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Gong Admin API and console to track licensed-seat utilization and per-team\
  \ adoption;\n      reconcile annual invoice against active seats.\n  - name: Allocation\n    description: Allocate seat cost to the owning sales / customer-success team; platform fee to revenue\n      operations.\n  - name: Optimization\n    description: Reclaim dormant seats quarterly; right-size product-module mix (Capture vs Engage vs\n      Forecast); avoid over-provisioning ahead of hiring plans.\n  - name: Accountability\n    description: Revenue Operations owns Gong spend and renewal; sales managers own per-team seat hygiene.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gong/refs/heads/main/finops/gong-finops.yml
sources:
- https://www.gong.io/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Revenue Intelligence
- SaaS
---
