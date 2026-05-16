---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: traceable-platform-openapi.yml
  format: yaml
  label: Traceable Platform GraphQL API
  slug: traceable-platform-graphql
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traceable/refs/heads/main/openapi/traceable-platform-openapi.yml
- filename: traceable-platform-openapi.yml
  format: yaml
  label: Traceable API Security Platform
  slug: traceable-platform
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/traceable/refs/heads/main/openapi/traceable-platform-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Refund
  pricingCategory: Contracted Subscription
description: 'FinOps shape for Traceable: contracted enterprise subscription for the API security platform, typically scaled by transactions ingested, agent/sensor count, modules enabled, and retention. No public meter rates are published; this artifact captures structural meters.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Harness, Inc.
  ProviderName: Traceable
  PublisherName: Harness, Inc.
  ServiceCategory: API Security
  ServiceName: Traceable
layout: finops
meters:
- aggregation: sum
  description: Volume of API transactions captured by Traceable agents/sensors and analyzed by the platform.
  dimensions:
  - environment
  - service
  name: api_transactions_ingested
  unit: transaction
- aggregation: avg
  description: Number of in-line / out-of-band Traceable agents (sensor licenses) deployed.
  dimensions:
  - cluster
  - environment
  name: agents_deployed
  unit: agent-month
- aggregation: max
  description: Retention window contracted for transaction telemetry (e.g., 30 / 90 days).
  dimensions:
  - module
  name: data_retention
  unit: day
name: Traceable Finops
provider_name: Traceable
provider_slug: traceable
publisher_name: Harness, Inc.
service_category: API Security
slug: traceable-finops
source_filename: traceable-finops.yml
source_heading: FinOps Profile
source_url: https://www.traceable.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Traceable\nproviderId: traceable\npublisherName: Harness, Inc.\nserviceCategory: API Security\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: false\ntags:\n  - API Security\n  - API Discovery\n  - API Protection\n  - FinOps\n  - FOCUS\ndescription: 'FinOps shape for Traceable: contracted enterprise subscription for the API security platform,\n  typically scaled by transactions ingested, agent/sensor count, modules enabled, and retention. No public\n  meter rates are published; this artifact captures structural meters.'\nsources:\n  - https://www.traceable.ai/pricing\nnotes: Pricing not publicly retrievable; meters are descriptive and\
  \ unpriced. PublisherName reflects Traceable's\n  acquisition by Harness in 2025.\nbillingModel:\n  pricingCategory: Contracted Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\nfocusColumns:\n  ServiceName: Traceable\n  ServiceCategory: API Security\n  ProviderName: Traceable\n  PublisherName: Harness, Inc.\n  InvoiceIssuerName: Harness, Inc.\n  BillingCurrency: USD\nmeters:\n  - name: api_transactions_ingested\n    description: Volume of API transactions captured by Traceable agents/sensors and analyzed by the platform.\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - environment\n      - service\n  - name: agents_deployed\n    description: Number of in-line / out-of-band Traceable agents (sensor licenses) deployed.\n    unit: agent-month\n    aggregation: avg\n    dimensions:\n      - cluster\n      - environment\n  - name: data_retention\n    description: Retention\
  \ window contracted for transaction telemetry (e.g., 30 / 90 days).\n    unit: day\n    aggregation: max\n    dimensions:\n      - module\nprinciples:\n  - name: Visibility\n    description: Pull contract usage from the Traceable customer-success report (transactions ingested,\n      agent count vs. cap); reconcile against your annual subscription tier each quarter.\n  - name: Allocation\n    description: Tag agents and ingested traffic with the owning microservice / business unit so the security\n      cost is attributable to the API teams generating it.\n  - name: Optimization\n    description: Tune sampling and retention by environment (full retention for prod, reduced for non-prod);\n      retire idle agents and prune orphaned API discoveries before each renewal.\n  - name: Accountability\n    description: AppSec or Platform Security team owns the Traceable contract and policy; engineering\n      service owners are accountable for fixing the discoveries it surfaces.\nmaintainers:\n\
  \  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/traceable/refs/heads/main/finops/traceable-finops.yml
sources:
- https://www.traceable.ai/pricing
specification: FinOps Framework
tags:
- API Security
- API Discovery
- API Protection
- FinOps
- FOCUS
---
