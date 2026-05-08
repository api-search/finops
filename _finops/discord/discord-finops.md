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
  pricingCategory: Consumer Subscription
description: FOCUS-aligned FinOps for Discord.
focus_columns:
  BillingCurrency: USD
  ProviderName: Discord
  PublisherName: Discord
  ServiceCategory: Communities
  ServiceName: Discord
layout: finops
meters:
- aggregation: max
  dimensions:
  - tier
  name: nitro_subscriptions
  unit: sub-month
- aggregation: max
  name: server_boosts
  unit: boost-month
- aggregation: sum
  name: bot_api_requests
  unit: request
name: Discord Finops
provider_name: Discord
provider_slug: discord
publisher_name: Discord
service_category: Communities
slug: discord-finops
source_filename: discord-finops.yml
source_heading: FinOps Profile
source_url: https://discord.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Discord\nproviderId: discord\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Communities\ndescription: FOCUS-aligned FinOps for Discord.\nsources:\n  - https://discord.com/pricing\n  - https://discord.com/nitro\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Discord\nserviceCategory: Communities\nbillingModel:\n  pricingCategory: Consumer Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Discord\n  ServiceCategory: Communities\n  ProviderName: Discord\n  PublisherName: Discord\n  BillingCurrency: USD\nmeters:\n  - name: nitro_subscriptions\n    unit: sub-month\n    aggregation: max\n\
  \    dimensions:\n      - tier\n  - name: server_boosts\n    unit: boost-month\n    aggregation: max\n  - name: bot_api_requests\n    unit: request\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Track Discord consumption monthly via admin/billing exports.\n  - name: Allocation\n    description: Tag seats/usage to teams or cost centers for chargeback.\n  - name: Optimization\n    description: Right-size tier and seat count quarterly; reclaim inactive seats.\n  - name: Accountability\n    description: Set spend alerts and renew at observed active utilization.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/discord/refs/heads/main/finops/discord-finops.yml
sources:
- https://discord.com/pricing
- https://discord.com/nitro
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Communities
---
