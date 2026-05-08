---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: appdynamics-controller-rest-api-openapi.yml
  format: yaml
  label: AppDynamics Controller REST API
  slug: controller-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-controller-rest-api-openapi.yml
- filename: appdynamics-metric-and-snapshot-api-openapi.yml
  format: yaml
  label: AppDynamics Metric and Snapshot API
  slug: metric-and-snapshot-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-metric-and-snapshot-api-openapi.yml
- filename: appdynamics-alert-and-respond-api-openapi.yml
  format: yaml
  label: AppDynamics Alert and Respond API
  slug: alert-and-respond-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-alert-and-respond-api-openapi.yml
- filename: appdynamics-configuration-api-openapi.yml
  format: yaml
  label: AppDynamics Configuration API
  slug: configuration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-configuration-api-openapi.yml
- filename: appdynamics-analytics-events-api-openapi.yml
  format: yaml
  label: AppDynamics Analytics Events API
  slug: analytics-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-analytics-events-api-openapi.yml
- filename: appdynamics-database-agent-api-openapi.yml
  format: yaml
  label: AppDynamics Database Agent API
  slug: database-agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-database-agent-api-openapi.yml
- filename: appdynamics-machine-agent-api-openapi.yml
  format: yaml
  label: AppDynamics Machine Agent API
  slug: machine-agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-machine-agent-api-openapi.yml
- filename: appdynamics-cloud-observability-api-openapi.yml
  format: yaml
  label: Cisco Cloud Observability API
  slug: cloud-observability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-cloud-observability-api-openapi.yml
- filename: appdynamics-authentication-api-openapi.yml
  format: yaml
  label: AppDynamics OAuth Authentication API
  slug: authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-authentication-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Adjustment
  pricingCategory: Subscription + Usage-Based
description: 'FOCUS-aligned FinOps view for AppDynamics: per-vCPU annual subscriptions across three editions (Infrastructure $6, Premium $33, Enterprise $50 per vCPU/month) with usage-priced add-ons for RUM (per 1,000 tokens) and Browser Synthetics (per test location). Allocation should track instrumented vCPUs per business unit and edition mix, with RUM token volume governed at the front-end build pipeline.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Cisco Systems, Inc.
  PricingCategory: Subscription
  ProviderName: Cisco AppDynamics
  PublisherName: Cisco Systems, Inc.
  ServiceCategory: Observability / APM
  ServiceName: AppDynamics
layout: finops
meters:
- aggregation: sum
  description: Instrumented vCPUs covered by the subscription, per month
  dimensions:
  - edition
  - business_unit
  - environment
  name: vcpu_months
  unit: vcpu-month
- aggregation: sum
  description: Real User Monitoring tokens consumed (browser + mobile)
  dimensions:
  - app
  - platform
  name: rum_tokens
  unit: token
- aggregation: max
  description: Active synthetic test locations per month
  dimensions:
  - app
  name: synthetic_locations
  unit: location
- aggregation: sum
  description: CPU cores covered by the Secure Application add-on
  dimensions:
  - app
  name: secure_app_cpu_cores
  unit: cpu-core
- aggregation: sum
  description: Analytics events ingested into the AppDynamics Events Service
  dimensions:
  - source
  name: events_ingest
  unit: event
name: Appdynamics Finops
provider_name: AppDynamics
provider_slug: appdynamics
publisher_name: Cisco Systems, Inc.
service_category: Observability / APM
slug: appdynamics-finops
source_filename: appdynamics-finops.yml
source_heading: FinOps Profile
source_url: https://www.splunk.com/en_us/products/pricing/observability.html
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AppDynamics\nproviderId: appdynamics\npublisherName: Cisco Systems, Inc.\nserviceCategory: Observability / APM\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - APM\n  - Observability\n  - Cisco\ndescription: 'FOCUS-aligned FinOps view for AppDynamics: per-vCPU annual subscriptions across three editions\n  (Infrastructure $6, Premium $33, Enterprise $50 per vCPU/month) with usage-priced add-ons for RUM (per\n  1,000 tokens) and Browser Synthetics (per test location). Allocation should track instrumented vCPUs\n  per business unit and edition mix, with RUM token volume governed at the front-end build\
  \ pipeline.'\nsources:\n  - https://www.splunk.com/en_us/products/pricing/observability.html\nbillingModel:\n  pricingCategory: Subscription + Usage-Based\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Adjustment\nfocusColumns:\n  ServiceName: AppDynamics\n  ServiceCategory: Observability / APM\n  ProviderName: Cisco AppDynamics\n  PublisherName: Cisco Systems, Inc.\n  InvoiceIssuerName: Cisco Systems, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Purchase\n  PricingCategory: Subscription\nmeters:\n  - name: vcpu_months\n    description: Instrumented vCPUs covered by the subscription, per month\n    unit: vcpu-month\n    aggregation: sum\n    dimensions:\n      - edition\n      - business_unit\n      - environment\n  - name: rum_tokens\n    description: Real User Monitoring tokens consumed (browser + mobile)\n    unit: token\n    aggregation: sum\n    dimensions:\n      - app\n      - platform\n  - name: synthetic_locations\n\
  \    description: Active synthetic test locations per month\n    unit: location\n    aggregation: max\n    dimensions:\n      - app\n  - name: secure_app_cpu_cores\n    description: CPU cores covered by the Secure Application add-on\n    unit: cpu-core\n    aggregation: sum\n    dimensions:\n      - app\n  - name: events_ingest\n    description: Analytics events ingested into the AppDynamics Events Service\n    unit: event\n    aggregation: sum\n    dimensions:\n      - source\nprinciples:\n  - name: Visibility\n    description: Use the AppDynamics Controller's License Usage and Account Management views and Cisco\n      EA reporting to track vCPUs by app and edition; export to BigQuery/Snowflake for showback.\n  - name: Allocation\n    description: Tag instrumented hosts/agents with business-unit and environment labels; allocate vCPU\n      consumption back to the consuming team.\n  - name: Optimization\n    description: Right-size editions per environment (Infrastructure for non-prod,\
  \ Premium/Enterprise\n      where APM is required); decommission unused agents; throttle RUM token sampling on high-traffic\n      endpoints.\n  - name: Accountability\n    description: Platform/SRE owns the AppDynamics contract; service owners accountable for vCPU footprint\n      and RUM token volume.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/finops/appdynamics-finops.yml
sources:
- https://www.splunk.com/en_us/products/pricing/observability.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- APM
- Observability
- Cisco
---
