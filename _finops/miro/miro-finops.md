---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: miro-openapi.json
  format: json
  label: Miro Boards API
  slug: miro-boards-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Board Items API
  slug: miro-board-items-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Connectors API
  slug: miro-connectors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Tags API
  slug: miro-tags-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Mind Map API
  slug: miro-mind-map-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Board Members API
  slug: miro-board-members-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Webhooks API
  slug: miro-webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Organization API
  slug: miro-organization-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Teams API
  slug: miro-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Audit Logs API
  slug: miro-audit-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro SCIM API
  slug: miro-scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
- filename: miro-openapi.json
  format: json
  label: Miro Web SDK
  slug: miro-web-sdk
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/openapi/miro-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly or Annual
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Per Seat)
description: FOCUS-aligned FinOps profile for Miro. Miro bills as a per-Member monthly subscription across Free, Starter, Business, and Enterprise tiers. AI usage is metered via per-member monthly AI credit allowances; overage requires plan upgrade or enterprise contract terms. Visitors and Guests are free on paid tiers.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Miro
  ProviderName: Miro
  PublisherName: Miro
  ServiceCategory: Productivity
  ServiceName: Miro
layout: finops
meters:
- aggregation: sum
  description: Per-Member subscription. Starter $8/$10, Business $20/$25, Enterprise contract.
  dimensions:
  - workspace
  - team
  - plan
  name: member_seats
  unit: seat
- aggregation: sum
  description: Monthly AI credits per member; Free 10/team, Starter 25/member, Business 50/member, Enterprise custom.
  dimensions:
  - workspace
  - member
  name: ai_credits
  unit: credit
name: Miro Finops
provider_name: Miro
provider_slug: miro
publisher_name: Miro
service_category: Productivity
slug: miro-finops
source_filename: miro-finops.yml
source_heading: FinOps Profile
source_url: https://miro.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Miro\nproviderId: miro\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Whiteboard\n- Visual Collaboration\n- Diagramming\n- SaaS\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Miro. Miro bills as a per-Member monthly\n  subscription across Free, Starter, Business, and Enterprise tiers. AI usage is metered\n  via per-member monthly AI credit allowances; overage requires plan upgrade or enterprise\n  contract terms. Visitors and Guests are free on paid tiers.\nsources:\n- https://miro.com/pricing/\n- https://developers.miro.com/reference/overview\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Miro\nserviceCategory: Productivity\nbillingModel:\n  pricingCategory: Subscription (Per Seat)\n  billingFrequency: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Miro\n  ServiceCategory: Productivity\n  ProviderName: Miro\n  PublisherName: Miro\n  InvoiceIssuerName: Miro\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: member_seats\n  description: Per-Member subscription. Starter $8/$10, Business $20/$25, Enterprise\n    contract.\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - workspace\n  - team\n  - plan\n- name: ai_credits\n  description: Monthly AI credits per member; Free 10/team, Starter 25/member,\n    Business 50/member, Enterprise custom.\n  unit: credit\n  aggregation: sum\n  dimensions:\n  - workspace\n  - member\nprinciples:\n- name: Visibility\n  description: Use Miro admin reports to inventory active members per workspace and team;\n    AI credit usage\
  \ per member.\n- name: Allocation\n  description: Allocate seats by team membership; tag enterprise contracts to procuring\n    business units.\n- name: Optimization\n  description: Reclaim seats from inactive members; choose annual billing for the discount;\n    exploit free Visitors/Guests for read-only collaborators; right-size plan tier to AI\n    credit needs.\n- name: Accountability\n  description: Assign workspace and organization owners; review quarterly seat counts\n    against active-user reports.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/miro/refs/heads/main/finops/miro-finops.yml
sources:
- https://miro.com/pricing/
- https://developers.miro.com/reference/overview
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Whiteboard
- Visual Collaboration
- Diagramming
- SaaS
- FinOps
- Cost Management
- FOCUS
---
