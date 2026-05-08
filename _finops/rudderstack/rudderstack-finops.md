---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rudderstack-gateway-openapi.yml
  format: yaml
  label: RudderStack HTTP Tracking API
  slug: rudderstack-http-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/rudderstack/refs/heads/main/openapi/rudderstack-gateway-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  billingTerm: Monthly or Annual
  chargeCategories:
  - Subscription
  - Usage
  - Adjustment
  - Tax
  commitmentDiscount: Annual prepay discount on Starter; committed-volume discount on Growth and Enterprise contracts.
  pricingCategory: Tier-Based Subscription with Event Quota
description: RudderStack's billing surface is a tier-based monthly subscription metered primarily on monthly tracked events. Free (250K events) is gratis; Starter is a flat $220/month including 1M events; Growth and Enterprise are custom-quoted committed-volume contracts. Reverse ETL connections, Profiles, and Python Transformations gate higher tiers. Hidden adjacent costs include the customer-owned data warehouse compute used by Profiles and Reverse ETL, and the egress traffic to downstream SaaS destinations.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Subscription
  InvoiceIssuerName: RudderStack
  PricingCategory: Standard Pricing
  ProviderName: RudderStack
  PublisherName: RudderStack
  ServiceCategory: Customer Data Platform
  ServiceName: RudderStack
layout: finops
meters:
- aggregation: sum
  description: Events ingested via Event Stream (identify, track, page, screen, group, alias) and counted toward the plan's monthly quota.
  dimensions:
  - workspace
  - source
  - event_type
  name: tracked_events
  unit: event
- aggregation: sum
  description: Rows synced through Reverse ETL pipelines.
  dimensions:
  - workspace
  - source
  - destination
  - model
  name: reverse_etl_rows
  unit: row
- aggregation: sum
  description: Profiles model executions (identity stitching, feature compute, audience materialization).
  dimensions:
  - workspace
  - project
  - model
  name: profiles_runs
  unit: run
- aggregation: sum
  description: Transformation function invocations (JS or Python) on the streaming pipeline.
  dimensions:
  - workspace
  - destination
  - language
  name: transformation_invocations
  unit: invocation
- aggregation: max
  description: Active source-to-destination connections (caps vary by tier).
  dimensions:
  - workspace
  - source
  - destination
  name: connections_active
  unit: connection-month
name: Rudderstack Finops
provider_name: RudderStack
provider_slug: rudderstack
publisher_name: RudderStack
service_category: Customer Data Platform
slug: rudderstack-finops
source_filename: rudderstack-finops.yml
source_heading: FinOps Profile
source_url: https://www.rudderstack.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: RudderStack\nproviderId: rudderstack\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n  - Customer Data Platform\n  - CDP\n  - Data Pipeline\n  - Event Streaming\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: >-\n  RudderStack's billing surface is a tier-based monthly subscription metered primarily on monthly tracked events. Free (250K events) is gratis; Starter is a flat $220/month including 1M events; Growth and Enterprise are custom-quoted committed-volume contracts. Reverse ETL connections, Profiles, and Python Transformations gate higher tiers. Hidden adjacent costs include the customer-owned data warehouse compute used by Profiles and Reverse ETL, and the egress traffic to downstream SaaS destinations.\nnotes: >-\n  Reconciled against published RudderStack pricing on 2026-05-08. RudderStack does not currently expose a public\
  \ FOCUS-formatted billing feed; usage and invoice data is available through the Dashboard, monthly invoices, and (for Enterprise) custom usage exports. Self-hosted (open-source) deployments do not generate RudderStack invoices but do incur infrastructure cost in the operator's cloud.\nsources:\n  - https://www.rudderstack.com/pricing/\n  - https://www.rudderstack.com/docs/data-pipelines/event-stream/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: RudderStack\nserviceCategory: Customer Data Platform\nbillingModel:\n  pricingCategory: Tier-Based Subscription with Event Quota\n  billingFrequency: Monthly\n  billingTerm: Monthly or Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Subscription\n    - Usage\n    - Adjustment\n    - Tax\n  commitmentDiscount:\
  \ Annual prepay discount on Starter; committed-volume discount on Growth and Enterprise contracts.\nfocusColumns:\n  ServiceName: RudderStack\n  ServiceCategory: Customer Data Platform\n  ProviderName: RudderStack\n  PublisherName: RudderStack\n  InvoiceIssuerName: RudderStack\n  BillingCurrency: USD\n  ChargeCategory: Subscription\n  PricingCategory: Standard Pricing\nmeters:\n  - name: tracked_events\n    description: Events ingested via Event Stream (identify, track, page, screen, group, alias) and counted toward the plan's monthly quota.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - workspace\n      - source\n      - event_type\n  - name: reverse_etl_rows\n    description: Rows synced through Reverse ETL pipelines.\n    unit: row\n    aggregation: sum\n    dimensions:\n      - workspace\n      - source\n      - destination\n      - model\n  - name: profiles_runs\n    description: Profiles model executions (identity stitching, feature compute, audience materialization).\n\
  \    unit: run\n    aggregation: sum\n    dimensions:\n      - workspace\n      - project\n      - model\n  - name: transformation_invocations\n    description: Transformation function invocations (JS or Python) on the streaming pipeline.\n    unit: invocation\n    aggregation: sum\n    dimensions:\n      - workspace\n      - destination\n      - language\n  - name: connections_active\n    description: Active source-to-destination connections (caps vary by tier).\n    unit: connection-month\n    aggregation: max\n    dimensions:\n      - workspace\n      - source\n      - destination\nprinciples:\n  - name: Visibility\n    description: >-\n      Pull the monthly invoice and Dashboard usage report. Track event-volume burn-down vs plan quota; on Enterprise, request a scheduled usage export feeding your cost-allocation pipeline. Account for warehouse compute consumed by Profiles and Reverse ETL inside your warehouse provider's bill, not the RudderStack invoice.\n  - name: Allocation\n   \
  \ description: >-\n      Use one workspace per business unit (or use source-level tagging) to attribute event volume back to product surfaces. Allocate Reverse ETL rows by destination owner.\n  - name: Optimization\n    description: >-\n      Suppress noisy events at the SDK and via Tracking Plan validation; right-size Reverse ETL sync frequency; archive rarely used connections; consolidate shadow workspaces; renegotiate at renewal once stable volume is known.\n  - name: Accountability\n    description: >-\n      Assign a workspace owner; alert on month-to-date events at 70/85/95% of plan; review forecast monthly with the contract owner ahead of renewal.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/rudderstack/refs/heads/main/finops/rudderstack-finops.yml
sources:
- https://www.rudderstack.com/pricing/
- https://www.rudderstack.com/docs/data-pipelines/event-stream/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Customer Data Platform
- CDP
- Data Pipeline
- Event Streaming
- FinOps
- Cost Management
- FOCUS
---
