---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: postman-webhooks-asyncapi.yml
  format: yaml
  label: Postman
  slug: postman
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/asyncapi/postman-webhooks-asyncapi.yml
- filename: postman-collections-api-openapi.yml
  format: yaml
  label: Postman Collections API
  slug: collections-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-collections-api-openapi.yml
- filename: postman-workspaces-api-openapi.yml
  format: yaml
  label: Postman Workspaces API
  slug: workspaces-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-workspaces-api-openapi.yml
- filename: postman-environments-api-openapi.yml
  format: yaml
  label: Postman Environments API
  slug: environments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-environments-api-openapi.yml
- filename: postman-mock-servers-api-openapi.yml
  format: yaml
  label: Postman Mock Servers API
  slug: mock-servers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-mock-servers-api-openapi.yml
- filename: postman-monitors-api-openapi.yml
  format: yaml
  label: Postman Monitors API
  slug: monitors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-monitors-api-openapi.yml
- filename: postman-apis-api-openapi.yml
  format: yaml
  label: Postman APIs / Spec Hub API
  slug: apis-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-apis-api-openapi.yml
- filename: postman-private-api-network-api-openapi.yml
  format: yaml
  label: Postman Private API Network API
  slug: private-api-network-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-private-api-network-api-openapi.yml
- filename: postman-webhooks-api-openapi.yml
  format: yaml
  label: Postman Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-webhooks-api-openapi.yml
- filename: postman-collection-runs-api-openapi.yml
  format: yaml
  label: Postman Collection Runs API
  slug: collection-runs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-collection-runs-api-openapi.yml
- filename: postman-tags-api-openapi.yml
  format: yaml
  label: Postman Tags API
  slug: tags-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-tags-api-openapi.yml
- filename: postman-audit-logs-api-openapi.yml
  format: yaml
  label: Postman Audit Logs API
  slug: audit-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-audit-logs-api-openapi.yml
- filename: postman-secret-scanner-api-openapi.yml
  format: yaml
  label: Postman Secret Scanner API
  slug: secret-scanner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-secret-scanner-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Tiered Subscription + Usage
description: 'FOCUS-aligned FinOps for Postman: per-seat tiered subscription (Solo $9, Team $19, Enterprise $49 per user/month, billed annually) layered with metered consumption surfaces (AI credits, automation flow credits, monitoring requests, Postman API calls). Add-ons (custom domains, private NPM, data-driven testing) appear as separate Purchase line items.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Postman, Inc.
  PricingUnit: seat-month
  ProviderName: Postman
  PublisherName: Postman, Inc.
  ServiceCategory: Developer Tools
  ServiceName: Postman
  ServiceSubcategory: API Platform
layout: finops
meters:
- aggregation: max
  description: Per-user subscription seats on Solo, Team, and Enterprise.
  dimensions:
  - plan
  - team
  name: seats
  unit: seat-month
- aggregation: sum
  description: AI credits consumed by Postbot and AI features.
  dimensions:
  - user
  - workspace
  - feature
  name: ai_credits
  unit: credit
- aggregation: sum
  description: Automation Flow runs charged in credits, pooled per team on Team and Enterprise.
  dimensions:
  - workspace
  - flow
  name: automation_flow_credits
  unit: credit
- aggregation: sum
  description: Outbound API monitor invocations.
  dimensions:
  - monitor
  - workspace
  - region
  name: monitoring_requests
  unit: request
- aggregation: sum
  description: Calls against the Postman REST API authenticated with a Postman API key.
  dimensions:
  - api_key
  - endpoint
  name: postman_api_calls
  unit: request
- aggregation: max
  description: Configured third-party integrations against the per-plan ceiling.
  dimensions:
  - workspace
  name: integrations
  unit: integration
- aggregation: count
  description: Optional purchases (custom domains, private NPM packages, data-driven testing).
  dimensions:
  - addon_type
  - workspace
  name: addons
  unit: addon
name: Postman Finops
provider_name: Postman
provider_slug: postman
publisher_name: Postman, Inc.
service_category: Developer Tools
slug: postman-finops
source_filename: postman-finops.yml
source_heading: FinOps Profile
source_url: https://www.postman.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Postman\nproviderId: postman\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - API Development\n  - Collaboration\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Postman: per-seat tiered subscription (Solo $9,\n  Team $19, Enterprise $49 per user/month, billed annually) layered with\n  metered consumption surfaces (AI credits, automation flow credits,\n  monitoring requests, Postman API calls). Add-ons (custom domains, private\n  NPM, data-driven testing) appear as separate Purchase line items.\nsources:\n  - https://www.postman.com/pricing/\n  - https://learning.postman.com/docs/developer/postman-api/postman-api-rate-limits/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Postman, Inc.\nserviceCategory: Developer Tools\nbillingModel:\n  pricingCategory: Tiered Subscription + Usage\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Postman\n  ServiceCategory: Developer Tools\n  ServiceSubcategory: API Platform\n  ProviderName: Postman\n  PublisherName: Postman, Inc.\n  InvoiceIssuerName: Postman, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingUnit: seat-month\nmeters:\n  - name: seats\n    description: Per-user subscription seats on Solo, Team, and Enterprise.\n    unit: seat-month\n    aggregation: max\n    dimensions:\n      - plan\n      - team\n  - name: ai_credits\n    description: AI credits consumed by Postbot and AI features.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - user\n      - workspace\n      - feature\n  - name: automation_flow_credits\n    description: Automation Flow runs\
  \ charged in credits, pooled per team on Team and Enterprise.\n    unit: credit\n    aggregation: sum\n    dimensions:\n      - workspace\n      - flow\n  - name: monitoring_requests\n    description: Outbound API monitor invocations.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - monitor\n      - workspace\n      - region\n  - name: postman_api_calls\n    description: Calls against the Postman REST API authenticated with a Postman API key.\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api_key\n      - endpoint\n  - name: integrations\n    description: Configured third-party integrations against the per-plan ceiling.\n    unit: integration\n    aggregation: max\n    dimensions:\n      - workspace\n  - name: addons\n    description: Optional purchases (custom domains, private NPM packages, data-driven testing).\n    unit: addon\n    aggregation: count\n    dimensions:\n      - addon_type\n      - workspace\nprinciples:\n  - name: Visibility\n   \
  \ description: Use the Postman resource-usage dashboard and the Postman API (which exposes RateLimit and monthly X-RateLimit headers on every response) to observe seat and consumption-meter consumption.\n  - name: Allocation\n    description: Allocate by workspace and team; pooled meters (Enterprise AI credits, Team automation credits) should be tagged at the workspace level for chargeback.\n  - name: Optimization\n    description: Right-size plan selection on per-user pricing breakpoints ($9 Solo, $19 Team, $49 Enterprise); cap AI-credit consumption per user; consolidate monitors to share the 10k/month monitoring quota.\n  - name: Accountability\n    description: Workspace owners are accountable for their AI credits, monitoring requests, and integration counts; admins should set alerts before the per-plan ceilings are reached and renegotiate seat counts at renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/finops/postman-finops.yml
sources:
- https://www.postman.com/pricing/
- https://learning.postman.com/docs/developer/postman-api/postman-api-rate-limits/
specification: FinOps Framework
tags:
- API Development
- Collaboration
- FinOps
- FOCUS
---
