---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: solarwinds-orion-openapi.yml
  format: yaml
  label: SolarWinds Orion API
  slug: solarwinds-orion-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-orion-openapi.yml
- filename: solarwinds-service-desk-openapi.yml
  format: yaml
  label: SolarWinds Service Desk API
  slug: solarwinds-service-desk-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-service-desk-openapi.yml
- filename: openapi.json
  format: json
  label: SolarWinds Observability API
  slug: solarwinds-observability-api
  spec_type: OpenAPI
  url: https://api.na-01.cloud.solarwinds.com/v1/openapi.json
- filename: solarwinds-pingdom-openapi.yml
  format: yaml
  label: SolarWinds Pingdom API
  slug: solarwinds-pingdom-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-pingdom-openapi.yml
- filename: solarwinds-loggly-openapi.yml
  format: yaml
  label: SolarWinds Loggly API
  slug: solarwinds-loggly-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-loggly-openapi.yml
- filename: solarwinds-papertrail-openapi.yml
  format: yaml
  label: SolarWinds Papertrail API
  slug: solarwinds-papertrail-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-papertrail-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  pricingCategory: Subscription + Perpetual License (Contact Sales)
description: FOCUS-aligned FinOps placeholder for SolarWinds. The portfolio mixes perpetual licenses (Orion-based products) and SaaS subscriptions (Observability, Service Desk, Pingdom, Loggly, Papertrail); meters reflect the consumption shape customers should track per product.
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: SolarWinds Worldwide, LLC
  ProviderName: SolarWinds
  PublisherName: SolarWinds Worldwide, LLC
  ServiceCategory: IT Management and Observability
  ServiceName: SolarWinds
layout: finops
meters:
- aggregation: max
  dimensions:
  - product
  - environment
  name: monitored_elements
  unit: element
- aggregation: sum
  dimensions:
  - product
  - source
  name: ingested_log_volume
  unit: GB
- aggregation: max
  dimensions:
  - dbms
  name: monitored_database_instances
  unit: instance
- aggregation: count
  dimensions:
  - region
  - check_type
  name: synthetic_checks
  unit: check
- aggregation: max
  dimensions:
  - tier
  name: service_desk_agents
  unit: agent
name: Solarwinds Finops
provider_name: SolarWinds
provider_slug: solarwinds
publisher_name: SolarWinds Worldwide, LLC
service_category: IT Management and Observability
slug: solarwinds-finops
source_filename: solarwinds-finops.yml
source_heading: FinOps Profile
source_url: https://www.solarwinds.com/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: SolarWinds\nproviderId: solarwinds\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - Observability\n  - IT Management\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps placeholder for SolarWinds. The portfolio mixes perpetual licenses\n  (Orion-based products) and SaaS subscriptions (Observability, Service Desk, Pingdom, Loggly, Papertrail);\n  meters reflect the consumption shape customers should track per product.'\nsources:\n  - https://www.solarwinds.com/\nnotes: SolarWinds publishes per-product pricing only via Contact Sales / quote-based channels and online\n  pricing pages were not retrievable. FOCUS unit prices cannot be reconciled here; meters describe consumption\n  shape per major product (monitored elements, ingested log volume, monitored database instances, synthetic\n  checks).\nalignedWith:\n  framework: FinOps\
  \ Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: SolarWinds Worldwide, LLC\nserviceCategory: IT Management and Observability\nbillingModel:\n  pricingCategory: Subscription + Perpetual License (Contact Sales)\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\nfocusColumns:\n  ServiceName: SolarWinds\n  ServiceCategory: IT Management and Observability\n  ProviderName: SolarWinds\n  PublisherName: SolarWinds Worldwide, LLC\n  InvoiceIssuerName: SolarWinds Worldwide, LLC\n  BillingCurrency: USD\nmeters:\n  - name: monitored_elements\n    unit: element\n    aggregation: max\n    dimensions:\n      - product\n      - environment\n  - name: ingested_log_volume\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - product\n      - source\n  - name: monitored_database_instances\n    unit:\
  \ instance\n    aggregation: max\n    dimensions:\n      - dbms\n  - name: synthetic_checks\n    unit: check\n    aggregation: count\n    dimensions:\n      - region\n      - check_type\n  - name: service_desk_agents\n    unit: agent\n    aggregation: max\n    dimensions:\n      - tier\nprinciples:\n  - name: Visibility\n    description: Use SolarWinds Observability dashboards plus per-product reporting (DPA, Service Desk\n      analytics, Pingdom reports, Loggly/Papertrail volume views) to surface consumption per product family.\n  - name: Allocation\n    description: Tag monitored elements, log sources, and Service Desk requesters to business units; allocate\n      Orion node licenses to the systems they monitor.\n  - name: Optimization\n    description: Retire stale monitors, archive cold log streams off Loggly/Papertrail, right-size Pingdom\n      check frequency, and consolidate Orion modules where the same hosts are monitored by multiple SKUs.\n  - name: Accountability\n    description:\
  \ Platform owner reconciles per-product entitlement (node count, log GB, agent count) against\n      SolarWinds invoices and renewal quotes each cycle.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/finops/solarwinds-finops.yml
sources:
- https://www.solarwinds.com/
specification: FinOps Framework
tags:
- Observability
- IT Management
- FinOps
- FOCUS
---
