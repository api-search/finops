---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: freshdesk-rest-api-openapi.yml
  format: yaml
  label: Freshdesk REST API
  slug: rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshdesk/refs/heads/main/openapi/freshdesk-rest-api-openapi.yml
- filename: freshdesk-webhook-api-asyncapi.yml
  format: yaml
  label: Freshdesk Webhook API
  slug: webhook-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshdesk/refs/heads/main/asyncapi/freshdesk-webhook-api-asyncapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Tiered Subscription + Usage Add-ons
description: 'FOCUS-aligned FinOps for Freshdesk: tiered per-agent SaaS subscription (Growth / Pro / Enterprise) billed annually, plus add-on usage for Freddy AI Agent sessions and purchased API capacity.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Freshworks Inc.
  ProviderName: Freshworks
  PublisherName: Freshworks Inc.
  ServiceCategory: Customer Support SaaS
  ServiceName: Freshdesk
layout: finops
meters:
- aggregation: max
  dimensions:
  - plan
  - account
  name: agent_seats
  unit: seat-month
- aggregation: sum
  dimensions:
  - account
  name: freddy_ai_sessions
  unit: session
- aggregation: sum
  dimensions:
  - endpoint
  - account
  name: api_calls
  unit: request
- aggregation: max
  dimensions:
  - account
  name: api_capacity_addon
  unit: capacity-block
name: Freshdesk Finops
provider_name: freshdesk
provider_slug: freshdesk
publisher_name: Freshworks Inc.
service_category: Customer Support SaaS
slug: freshdesk-finops
source_filename: freshdesk-finops.yml
source_heading: FinOps Profile
source_url: https://www.freshworks.com/freshdesk/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: freshdesk\nproviderId: freshdesk\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Support\n  - SaaS\ndescription: 'FOCUS-aligned FinOps for Freshdesk: tiered per-agent SaaS subscription (Growth / Pro\n  / Enterprise) billed annually, plus add-on usage for Freddy AI Agent sessions and purchased API\n  capacity.'\nsources:\n  - https://www.freshworks.com/freshdesk/pricing/\n  - https://developers.freshdesk.com/api/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Freshworks Inc.\nserviceCategory: Customer Support SaaS\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage Add-ons\n  billingFrequency: Annual\n  billingCurrency:\
  \ USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Freshdesk\n  ServiceCategory: Customer Support SaaS\n  ProviderName: Freshworks\n  PublisherName: Freshworks Inc.\n  InvoiceIssuerName: Freshworks Inc.\n  BillingCurrency: USD\nmeters:\n  - name: agent_seats\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n      - account\n  - name: freddy_ai_sessions\n    unit: session\n    aggregation: sum\n    dimensions:\n      - account\n  - name: api_calls\n    unit: request\n    aggregation: sum\n    dimensions:\n      - endpoint\n      - account\n  - name: api_capacity_addon\n    unit: capacity-block\n    aggregation: max\n    dimensions:\n      - account\nprinciples:\n  - name: Visibility\n    description: Use the Freshworks Admin / Billing console to see committed seats, Freddy\n      session consumption, and API rate-limit headroom; rely on X-RateLimit-* headers for\n      live API spend\
  \ signals.\n  - name: Allocation\n    description: Map agent seats to teams/queues; tag tickets with custom fields to allocate\n      effort to product lines or customers.\n  - name: Optimization\n    description: Right-size annual seat commitments against active agent count; use Freddy AI\n      Copilot to deflect tickets and reduce headcount growth; cache list responses and\n      batch-update where the API contract allows.\n  - name: Accountability\n    description: Customer-support leader owns annual seat commit; finance reviews Freddy\n      session usage and any purchased API capacity blocks.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/freshdesk/refs/heads/main/finops/freshdesk-finops.yml
sources:
- https://www.freshworks.com/freshdesk/pricing/
- https://developers.freshdesk.com/api/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Support
- SaaS
---
