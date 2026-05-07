---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: portkey-openapi.yml
  format: yaml
  label: Portkey
  slug: portkey
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/portkey/refs/heads/main/openapi/portkey-openapi.yml
- filename: portkey-openapi.yml
  format: yaml
  label: Portkey Inference API
  slug: portkey-inference-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/portkey/refs/heads/main/openapi/portkey-openapi.yml
- filename: portkey-openapi.yml
  format: yaml
  label: Portkey Admin API
  slug: portkey-admin-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/portkey/refs/heads/main/openapi/portkey-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  pricingCategory: Subscription + Usage Overage
description: 'FOCUS-aligned FinOps for Portkey: flat subscription on the Production tier ($49/month + $9 per additional 100k requests above the 100k included logs) plus contact-sales Enterprise. The primary billable meter is recorded request logs; secondary dimensions track virtual keys, workspaces, and the upstream LLM provider being proxied so that AI spend can be allocated by team and model.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Portkey AI, Inc.
  PricingUnit: 100k requests
  ProviderName: Portkey
  PublisherName: Portkey AI, Inc.
  ServiceCategory: AI Infrastructure
  ServiceName: Portkey
  ServiceSubcategory: AI Gateway
layout: finops
meters:
- aggregation: sum
  description: Request log entries persisted by the Portkey gateway and counted toward the plan cap.
  dimensions:
  - virtual_key
  - workspace
  - upstream_provider
  - model
  - environment
  name: recorded_logs
  unit: log
- aggregation: sum
  description: Recorded logs above the 100k Production-plan included quota, billed in 100k-request blocks.
  dimensions:
  - workspace
  - environment
  name: log_overage
  unit: 100k-requests
- aggregation: count
  description: Flat monthly Production subscription seat.
  dimensions:
  - plan
  name: subscription
  unit: month
- aggregation: max
  description: Stored prompt templates (capped on Developer at 3, unlimited on Production+).
  dimensions:
  - workspace
  name: prompt_templates
  unit: template
- aggregation: max
  description: Configured retention horizon (3 days on Developer, 30 on Production, custom on Enterprise).
  dimensions:
  - workspace
  name: log_retention_days
  unit: day
name: Portkey Finops
provider_name: Portkey
provider_slug: portkey
publisher_name: Portkey AI, Inc.
service_category: AI Infrastructure
slug: portkey-finops
source_filename: portkey-finops.yml
source_heading: FinOps Profile
source_url: https://portkey.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Portkey\nproviderId: portkey\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Gateways\n  - Governance\n  - Observability\n  - FinOps\n  - FOCUS\ndescription: >-\n  FOCUS-aligned FinOps for Portkey: flat subscription on the Production tier\n  ($49/month + $9 per additional 100k requests above the 100k included logs)\n  plus contact-sales Enterprise. The primary billable meter is recorded request\n  logs; secondary dimensions track virtual keys, workspaces, and the upstream\n  LLM provider being proxied so that AI spend can be allocated by team and\n  model.\nsources:\n  - https://portkey.ai/pricing\n  - https://portkey.ai/docs/product/enterprise-offering/private-cloud-deployments\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n\
  \  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Portkey AI, Inc.\nserviceCategory: AI Infrastructure\nbillingModel:\n  pricingCategory: Subscription + Usage Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Portkey\n  ServiceCategory: AI Infrastructure\n  ServiceSubcategory: AI Gateway\n  ProviderName: Portkey\n  PublisherName: Portkey AI, Inc.\n  InvoiceIssuerName: Portkey AI, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: 100k requests\nmeters:\n  - name: recorded_logs\n    description: Request log entries persisted by the Portkey gateway and counted toward the plan cap.\n    unit: log\n    aggregation: sum\n    dimensions:\n      - virtual_key\n      - workspace\n      - upstream_provider\n      - model\n      - environment\n  - name: log_overage\n    description: Recorded logs above the 100k Production-plan\
  \ included quota, billed in 100k-request blocks.\n    unit: 100k-requests\n    aggregation: sum\n    dimensions:\n      - workspace\n      - environment\n  - name: subscription\n    description: Flat monthly Production subscription seat.\n    unit: month\n    aggregation: count\n    dimensions:\n      - plan\n  - name: prompt_templates\n    description: Stored prompt templates (capped on Developer at 3, unlimited on Production+).\n    unit: template\n    aggregation: max\n    dimensions:\n      - workspace\n  - name: log_retention_days\n    description: Configured retention horizon (3 days on Developer, 30 on Production, custom on Enterprise).\n    unit: day\n    aggregation: max\n    dimensions:\n      - workspace\nprinciples:\n  - name: Visibility\n    description: Use the Portkey Logs, Traces, Metadata, and Filters surface (and the Admin API analytics endpoints) to attribute every proxied LLM call to a virtual key, workspace, and upstream model.\n  - name: Allocation\n    description:\
  \ Tag virtual keys with team, environment, and product so the recorded-logs meter can be allocated; budgets and rate limits on Enterprise can be scoped per virtual key for chargeback.\n  - name: Optimization\n    description: Use Portkey's semantic caching, fallbacks, and routing to lower upstream LLM token spend; right-size the Production overage band ($9 per 100k requests) before promoting to Enterprise contracts.\n  - name: Accountability\n    description: Assign budget owners to each workspace; configure alerts on the granular budget and rate-limit primitives so overruns surface to the responsible team.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/portkey/refs/heads/main/finops/portkey-finops.yml
sources:
- https://portkey.ai/pricing
- https://portkey.ai/docs/product/enterprise-offering/private-cloud-deployments
specification: FinOps Framework
tags:
- AI Gateways
- Governance
- Observability
- FinOps
- FOCUS
---
