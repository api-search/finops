---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: npr-station-finder-openapi-original.yml
  format: yaml
  label: NPR Station Finder
  slug: station-finder
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/npr/main/openapi/npr-station-finder-openapi-original.yml
- filename: npr-identity-openapi-original.yml
  format: yaml
  label: NPR Identity
  slug: identity
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/npr/main/openapi/npr-identity-openapi-original.yml
- filename: npr-authorization-openapi-original.yml
  format: yaml
  label: NPR Authorization
  slug: authorization
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/npr/main/openapi/npr-authorization-openapi-original.yml
billing_model:
  billingCurrency: USD
  billingFrequency: None
  chargeCategories:
  - Usage
  chargeFrequency: None
  pricingCategory: Free / Partner Program
description: 'FOCUS-aligned FinOps for NPR: API access is free under a partner/credentialed program rather than a paid SaaS contract. Cost dimensions are operational (engineering integration time, content licensing obligations) rather than per-call invoicing.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: N/A (free partner program)
  PricingCategory: Free
  PricingUnit: request
  ProviderName: NPR
  PublisherName: National Public Radio, Inc.
  ServiceCategory: Media / Public Broadcasting
  ServiceName: NPR
layout: finops
meters:
- aggregation: sum
  description: Count of API requests across all NPR developer surfaces (operationally tracked, not invoiced)
  dimensions:
  - api
  - oauth_client
  - endpoint
  name: api_requests
  unit: request
- aggregation: sum
  description: Listening API audio recommendations delivered (relevant to content licensing reporting)
  name: audio_recommendations_served
  unit: recommendation
- aggregation: sum
  description: Station Finder lookups by zip/geo
  name: station_lookups
  unit: lookup
name: Npr Finops
provider_name: NPR
provider_slug: npr
publisher_name: National Public Radio, Inc.
service_category: Media / Public Broadcasting
slug: npr-finops
source_filename: npr-finops.yml
source_heading: FinOps Profile
source_url: https://dev.npr.org/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: NPR\nproviderId: npr\npublisherName: National Public Radio, Inc.\nserviceCategory: Media / Public Broadcasting\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Media\n  - News\n  - Radio\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for NPR: API access is free under a partner/credentialed program rather\n  than a paid SaaS contract. Cost dimensions are operational (engineering integration time, content licensing\n  obligations) rather than per-call invoicing.'\nnotes: NPR does not invoice API consumers under the public developer program; the FinOps surface is implementation\n  cost and\
  \ content-licensing compliance, not vendor spend.\nsources:\n  - https://dev.npr.org/\nprinciples:\n  - name: Visibility\n    description: There is no NPR invoice for API usage. Track per-OAuth-client request volumes and content\n      airing/streaming counts internally for licensing and quota-of-fair-use reporting.\n  - name: Allocation\n    description: Allocate API usage to the consuming app or station group via the OAuth client_id.\n  - name: Optimization\n    description: Cache NPR Listening recommendations and Station Finder responses; respect upstream content\n      TTLs to minimize redundant calls and stay within fair use.\n  - name: Accountability\n    description: Each NPR developer account has an owner of record. Assign per-app responsibility for\n      compliance with the NPR API Terms of Use and content rights, and for renewing OAuth credentials.\nbillingModel:\n  pricingCategory: Free / Partner Program\n  billingFrequency: None\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Usage\n  chargeFrequency: None\nfocusColumns:\n  ServiceName: NPR\n  ServiceCategory: Media / Public Broadcasting\n  ProviderName: NPR\n  PublisherName: National Public Radio, Inc.\n  InvoiceIssuerName: N/A (free partner program)\n  PricingCategory: Free\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of API requests across all NPR developer surfaces (operationally tracked, not invoiced)\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - oauth_client\n      - endpoint\n  - name: audio_recommendations_served\n    description: Listening API audio recommendations delivered (relevant to content licensing reporting)\n    unit: recommendation\n    aggregation: sum\n  - name: station_lookups\n    description: Station Finder lookups by zip/geo\n    unit: lookup\n    aggregation: sum\napis:\n  - name: NPR Listening\n    baseURL: https://listening.api.npr.org/\n    tags:\n      -\
  \ Audio\n      - Listening\n    serviceName: NPR Listening\n    serviceCategory: Media\n  - name: NPR Station Finder\n    baseURL: https://station.api.npr.org/\n    tags:\n      - Stations\n    serviceName: NPR Station Finder\n    serviceCategory: Media\n  - name: NPR Identity\n    baseURL: https://identity.api.npr.org/\n    tags:\n      - Identity\n      - Users\n    serviceName: NPR Identity\n    serviceCategory: Media\n  - name: NPR Authorization\n    baseURL: https://authorization.api.npr.org/\n    tags:\n      - Authorization\n    serviceName: NPR Authorization\n    serviceCategory: Media\nunitEconomics:\n  - name: Engineering cost per integrated app\n    metric: integration_engineer_hours * loaded_rate / integrated_apps\n    target: minimize via shared client libraries\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/npr/refs/heads/main/finops/npr-finops.yml
sources:
- https://dev.npr.org/
specification: FinOps Framework
tags:
- Media
- News
- Radio
- FinOps
- Cost Management
- FOCUS
---
