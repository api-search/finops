---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: statsig-http-api-openapi.yml
  format: yaml
  label: Statsig HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statsig/refs/heads/main/openapi/statsig-http-api-openapi.yml
- filename: statsig-console-api-openapi.yml
  format: yaml
  label: Statsig Console API
  slug: console-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statsig/refs/heads/main/openapi/statsig-console-api-openapi.yml
- filename: statsig-client-sdk-api-openapi.yml
  format: yaml
  label: Statsig Client SDK API
  slug: client-sdk-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statsig/refs/heads/main/openapi/statsig-client-sdk-api-openapi.yml
- filename: statsig-server-sdk-api-openapi.yml
  format: yaml
  label: Statsig Server SDK API
  slug: server-sdk-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statsig/refs/heads/main/openapi/statsig-server-sdk-api-openapi.yml
- filename: statsig-events-api-openapi.yml
  format: yaml
  label: Statsig Events API
  slug: events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/statsig/refs/heads/main/openapi/statsig-events-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Subscription + Pay-As-You-Go Overage
description: 'FOCUS-aligned FinOps for Statsig: free tier plus a fixed Pro subscription with included event allowance and per-1K event overage, with custom event- or experiment-priced Enterprise contracts. Primary billable meters are metered events and session replays.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Statsig, Inc.
  ProviderName: Statsig
  PublisherName: Statsig, Inc.
  ServiceCategory: Feature Flags & Experimentation
  ServiceName: Statsig
layout: finops
meters:
- aggregation: sum
  description: Exposures, logged events, ingested metrics, and custom metrics that count toward the monthly event allowance and overage billing.
  dimensions:
  - project
  - event_type
  - environment
  name: metered_events
  unit: event
- aggregation: sum
  description: Recorded session replays counted against the plan's monthly replay allowance.
  dimensions:
  - project
  - environment
  name: session_replays
  unit: replay
- aggregation: sum
  description: Fixed monthly Pro subscription fee ($150/month, one project).
  dimensions:
  - project
  name: pro_subscription
  unit: month
- aggregation: sum
  description: Experiments-priced unit for Enterprise contracts that opt into experiment-based pricing.
  dimensions:
  - project
  - environment
  name: enterprise_experiments
  unit: experiment
name: Statsig Finops
provider_name: statsig
provider_slug: statsig
publisher_name: Statsig, Inc.
service_category: Feature Flags & Experimentation
slug: statsig-finops
source_filename: statsig-finops.yml
source_heading: FinOps Profile
source_url: https://www.statsig.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Statsig\nproviderId: statsig\npublisherName: Statsig, Inc.\nserviceCategory: Feature Flags & Experimentation\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Feature Flags\n  - Experimentation\n  - Session Replay\ndescription: 'FOCUS-aligned FinOps for Statsig: free tier plus a fixed Pro subscription with included\n  event allowance and per-1K event overage, with custom event- or experiment-priced Enterprise contracts.\n  Primary billable meters are metered events and session replays.'\nsources:\n  - https://www.statsig.com/pricing\n  - https://docs.statsig.com/console-api/introduction\nbillingModel:\n\
  \  pricingCategory: Subscription + Pay-As-You-Go Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Statsig\n  ServiceCategory: Feature Flags & Experimentation\n  ProviderName: Statsig\n  PublisherName: Statsig, Inc.\n  InvoiceIssuerName: Statsig, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: metered_events\n    description: Exposures, logged events, ingested metrics, and custom metrics that count toward the\n      monthly event allowance and overage billing.\n    unit: event\n    aggregation: sum\n    dimensions:\n      - project\n      - event_type\n      - environment\n  - name: session_replays\n    description: Recorded session replays counted against the plan's monthly replay allowance.\n    unit: replay\n    aggregation: sum\n    dimensions:\n      - project\n      - environment\n  - name: pro_subscription\n    description:\
  \ Fixed monthly Pro subscription fee ($150/month, one project).\n    unit: month\n    aggregation: sum\n    dimensions:\n      - project\n  - name: enterprise_experiments\n    description: Experiments-priced unit for Enterprise contracts that opt into experiment-based pricing.\n    unit: experiment\n    aggregation: sum\n    dimensions:\n      - project\n      - environment\nprinciples:\n  - name: Visibility\n    description: Use the Statsig Console (Project Settings > Usage) and the Console API to track event\n      and session-replay consumption against the plan allowance; warning notifications fire before Metric\n      Lifts stop on the free tier.\n  - name: Allocation\n    description: Tag exposures and logged events with project, environment, and stable user IDs so usage\n      can be attributed to specific products, experiments, or teams. Multi-project Enterprise customers\n      can isolate billing per project.\n  - name: Optimization\n    description: Reduce metered-event volume\
  \ by deduplicating exposure logging at the SDK layer, sampling\n      session replays, and pruning unused metrics; on Pro, watch the $0.05/1K overage meter; on Enterprise,\n      negotiate event vs experiment pricing based on whichever model fits your workload best.\n  - name: Accountability\n    description: Assign a project owner per Statsig project; route the monthly invoice and any overage\n      line items to that owner; review event growth before launching new feature gates or analytics events.\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/statsig/refs/heads/main/finops/statsig-finops.yml
sources:
- https://www.statsig.com/pricing
- https://docs.statsig.com/console-api/introduction
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Feature Flags
- Experimentation
- Session Replay
---
