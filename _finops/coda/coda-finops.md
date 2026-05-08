---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: coda-openapi.json
  format: json
  label: Coda Docs API
  slug: coda-docs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Folders API
  slug: coda-folders-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Pages API
  slug: coda-pages-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Tables API
  slug: coda-tables-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Columns API
  slug: coda-columns-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Rows API
  slug: coda-rows-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Formulas API
  slug: coda-formulas-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Controls API
  slug: coda-controls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Automations API
  slug: coda-automations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Permissions API
  slug: coda-permissions-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Publishing API
  slug: coda-publishing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Account API
  slug: coda-account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Analytics API
  slug: coda-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
- filename: coda-openapi.json
  format: json
  label: Coda Packs SDK
  slug: coda-packs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/openapi/coda-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Adjustment
  pricingCategory: Subscription (Per Seat)
description: FOCUS-aligned FinOps profile for Coda. Coda bills primarily on a per-Doc-Maker monthly subscription basis. Editors, viewers, and the public API are free across all tiers. There is no metered API surcharge; costs scale with the count of Doc Makers and selected plan tier.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Coda Project, Inc.
  ProviderName: Coda
  PublisherName: Coda Project, Inc.
  ServiceCategory: Productivity
  ServiceName: Coda
layout: finops
meters:
- aggregation: sum
  description: Monthly subscription per active Doc Maker. Pro $12/Maker, Team $36/Maker, Enterprise contract.
  dimensions:
  - workspace
  - plan
  name: doc_maker_seats
  unit: seat
name: Coda Finops
provider_name: Coda
provider_slug: coda
publisher_name: Coda Project, Inc.
service_category: Productivity
slug: coda-finops
source_filename: coda-finops.yml
source_heading: FinOps Profile
source_url: https://coda.io/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Coda\nproviderId: coda\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Productivity\n- Docs\n- No-Code\n- Collaboration\n- Database\n- FinOps\n- Cost Management\n- FOCUS\ndescription: FOCUS-aligned FinOps profile for Coda. Coda bills primarily on a per-Doc-Maker\n  monthly subscription basis. Editors, viewers, and the public API are free across all\n  tiers. There is no metered API surcharge; costs scale with the count of Doc Makers and\n  selected plan tier.\nsources:\n- https://coda.io/pricing\n- https://coda.io/developers/apis/v1\n- https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Coda Project, Inc.\n\
  serviceCategory: Productivity\nbillingModel:\n  pricingCategory: Subscription (Per Seat)\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Coda\n  ServiceCategory: Productivity\n  ProviderName: Coda\n  PublisherName: Coda Project, Inc.\n  InvoiceIssuerName: Coda Project, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n- name: doc_maker_seats\n  description: Monthly subscription per active Doc Maker. Pro $12/Maker, Team $36/Maker,\n    Enterprise contract.\n  unit: seat\n  aggregation: sum\n  dimensions:\n  - workspace\n  - plan\nprinciples:\n- name: Visibility\n  description: Use Coda workspace billing reports to see active Doc Makers and right-size\n    seat counts.\n- name: Allocation\n  description: Allocate seats to teams/cost centers based on Doc Maker membership; editors\n    and viewers are free and need no allocation.\n- name: Optimization\n  description: Encourage editor/viewer\
  \ usage where doc-creation is not needed; consolidate\n    inactive Doc Makers; pick the lowest tier that meets feature needs.\n- name: Accountability\n  description: Assign each workspace to a budget owner; review monthly Doc Maker counts and\n    plan tier alignment.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/coda/refs/heads/main/finops/coda-finops.yml
sources:
- https://coda.io/pricing
- https://coda.io/developers/apis/v1
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Productivity
- Docs
- No-Code
- Collaboration
- Database
- FinOps
- Cost Management
- FOCUS
---
