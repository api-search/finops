---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: discord-api-spec
  format: yaml
  label: Discord REST API
  slug: discord-rest-api
  spec_type: OpenAPI
  url: https://github.com/discord/discord-api-spec
- filename: discord-gateway-api-asyncapi.yml
  format: yaml
  label: Discord Gateway API
  slug: discord-gateway-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/asyncapi/discord-gateway-api-asyncapi.yml
- filename: discord-interactions-api-openapi.yml
  format: yaml
  label: Discord Interactions API
  slug: discord-interactions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/openapi/discord-interactions-api-openapi.yml
- filename: discord-oauth2-api-openapi.yml
  format: yaml
  label: Discord OAuth2 API
  slug: discord-oauth2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/openapi/discord-oauth2-api-openapi.yml
- filename: discord-webhook-events-api-openapi.yml
  format: yaml
  label: Discord Webhook Events API
  slug: discord-webhook-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/openapi/discord-webhook-events-api-openapi.yml
- filename: discord-voice-api-asyncapi.yml
  format: yaml
  label: Discord Voice API
  slug: discord-voice-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/asyncapi/discord-voice-api-asyncapi.yml
- filename: discord-linked-roles-api-openapi.yml
  format: yaml
  label: Discord Linked Roles API
  slug: discord-linked-roles-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/openapi/discord-linked-roles-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Discord API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Discord
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Discord
  PublisherName: Discord
  ServiceCategory: Developer Tools / API
  ServiceName: Discord
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Discord Finops
provider_name: Discord
provider_slug: discord
publisher_name: Discord
service_category: API
slug: discord-finops
source_filename: discord-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Discord\nproviderId: discord\npublisherName: Discord\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Chat\n  - Communication\n  - Gaming\n  - Messaging\n  - Social\n  - Video\n  - Voice\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Discord API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Discord\n  ServiceCategory: Developer Tools / API\n  ProviderName: Discord\n  PublisherName: Discord\n  InvoiceIssuerName: Discord\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Discord REST API\n    baseURL: https://discord.com/api/v10\n    tags:\n      - Channels\n      - Guilds\n      - Messaging\n      - REST\n      - Users\n      - Webhooks\n    serviceName: Discord REST API\n    serviceCategory: API\n  - name: Discord Gateway API\n    baseURL: ''\n    tags:\n      - Events\n      - Gateway\n      - Real-Time\n      - WebSocket\n    serviceName: Discord Gateway API\n    serviceCategory: API\n  - name: Discord Interactions API\n    baseURL: ''\n    tags:\n      - Components\n      - Interactions\n      - Modals\n      - Slash Commands\n    serviceName: Discord Interactions API\n    serviceCategory: API\n  - name: Discord OAuth2 API\n    baseURL: ''\n    tags:\n      - Authentication\n\
  \      - Authorization\n      - OAuth2\n    serviceName: Discord OAuth2 API\n    serviceCategory: API\n  - name: Discord Webhook Events API\n    baseURL: ''\n    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Discord Webhook Events API\n    serviceCategory: API\n  - name: Discord Embedded App SDK\n    baseURL: ''\n    tags:\n      - Activities\n      - Embedded\n      - Games\n      - SDK\n    serviceName: Discord Embedded App SDK\n    serviceCategory: API\n  - name: Discord Voice API\n    baseURL: ''\n    tags:\n      - Real-Time\n      - UDP\n      - Voice\n      - WebSocket\n    serviceName: Discord Voice API\n    serviceCategory: API\n  - name: Discord Linked Roles API\n    baseURL: ''\n    tags:\n      - Metadata\n      - OAuth2\n      - Roles\n      - Verification\n    serviceName: Discord Linked Roles API\n    serviceCategory: API\n  - name: Discord Social SDK\n    baseURL: ''\n    tags:\n      - Gaming\n      - Rich Presence\n      - SDK\n    \
  \  - Social\n      - Voice\n    serviceName: Discord Social SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n  - name: Discord Inc.\n    twitter: discord\n    email: support@discord.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/finops/discord-finops.yml
sources: []
specification: FinOps Framework
tags:
- Chat
- Communication
- Gaming
- Messaging
- Social
- Video
- Voice
- FinOps
- Cost Management
- FOCUS
---
