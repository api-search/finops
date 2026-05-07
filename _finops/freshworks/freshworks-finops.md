---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: freshworks-freshdesk-api-openapi.yml
  format: yaml
  label: Freshworks Freshdesk API
  slug: freshdesk-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/openapi/freshworks-freshdesk-api-openapi.yml
- filename: freshworks-freshservice-api-openapi.yml
  format: yaml
  label: Freshworks Freshservice API
  slug: freshservice-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/openapi/freshworks-freshservice-api-openapi.yml
- filename: freshworks-freshsales-api-openapi.yml
  format: yaml
  label: Freshworks Freshsales API
  slug: freshsales-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/openapi/freshworks-freshsales-api-openapi.yml
- filename: freshworks-freshchat-api-openapi.yml
  format: yaml
  label: Freshworks Freshchat API
  slug: freshchat-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/openapi/freshworks-freshchat-api-openapi.yml
- filename: freshworks-freshcaller-api-openapi.yml
  format: yaml
  label: Freshworks Freshcaller API
  slug: freshcaller-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/openapi/freshworks-freshcaller-api-openapi.yml
- filename: freshworks-freshteam-api-openapi.yml
  format: yaml
  label: Freshworks Freshteam API
  slug: freshteam-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/openapi/freshworks-freshteam-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Per-Agent Subscription
description: FOCUS-aligned FinOps for Freshworks.
focus_columns:
  BillingCurrency: USD
  ProviderName: Freshworks
  PublisherName: Freshworks
  ServiceCategory: Customer Support / CRM
  ServiceName: Freshworks
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - tier
  name: agent_seats
  unit: seat-month
- aggregation: sum
  name: freddy_ai_sessions
  unit: session
- aggregation: sum
  name: tickets_created
  unit: ticket
- aggregation: max
  name: collaborators
  unit: collaborator-month
name: Freshworks Finops
provider_name: freshworks
provider_slug: freshworks
publisher_name: Freshworks
service_category: Customer Support / CRM
slug: freshworks-finops
source_filename: freshworks-finops.yml
source_heading: FinOps Profile
source_url: https://www.freshworks.com/freshdesk/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Freshworks\nproviderId: freshworks\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Customer Support / CRM\ndescription: FOCUS-aligned FinOps for Freshworks.\nsources:\n  - https://www.freshworks.com/freshdesk/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Freshworks\nserviceCategory: Customer Support / CRM\nbillingModel:\n  pricingCategory: Per-Agent Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: Freshworks\n  ServiceCategory: Customer Support / CRM\n  ProviderName: Freshworks\n  PublisherName: Freshworks\n  BillingCurrency: USD\nmeters:\n  - name: agent_seats\n    unit:\
  \ seat-month\n    aggregation: max\n    dimensions:\n      - product\n      - tier\n  - name: freddy_ai_sessions\n    unit: session\n    aggregation: sum\n  - name: tickets_created\n    unit: ticket\n    aggregation: sum\n  - name: collaborators\n    unit: collaborator-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track Freshworks consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/freshworks/refs/heads/main/finops/freshworks-finops.yml
sources:
- https://www.freshworks.com/freshdesk/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Customer Support / CRM
---
