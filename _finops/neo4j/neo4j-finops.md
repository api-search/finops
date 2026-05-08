---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: neo4j-http-api-openapi.yml
  format: yaml
  label: Neo4j HTTP API
  slug: http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/openapi/neo4j-http-api-openapi.yml
- filename: neo4j-query-api-openapi.yml
  format: yaml
  label: Neo4j Query API
  slug: query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/openapi/neo4j-query-api-openapi.yml
- filename: neo4j-aura-api-openapi.yml
  format: yaml
  label: Neo4j Aura API
  slug: aura-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/openapi/neo4j-aura-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Subscription
description: 'FOCUS-aligned FinOps for Neo4j: AuraDB billed per GB-RAM-month with size scaling memory + CPU + storage together; Aura Graph Analytics billed per GB-hour; self-managed Enterprise via annual contract.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Neo4j, Inc.
  PricingCategory: Pay-As-You-Go
  PricingUnit: GB-month
  ProviderName: Neo4j
  PublisherName: Neo4j, Inc.
  ServiceCategory: Database
  ServiceName: Neo4j
  ServiceSubcategory: Graph Database
layout: finops
meters:
- aggregation: avg
  description: AuraDB Professional capacity at $65 per GB RAM per month (min 1 GB).
  dimensions:
  - region
  - instance
  - cloud
  name: auradb_professional_gb_month
  unit: GB-month
- aggregation: avg
  description: AuraDB Business Critical capacity at $146 per GB RAM per month (min 2 GB).
  dimensions:
  - region
  - instance
  - cloud
  name: auradb_business_critical_gb_month
  unit: GB-month
- aggregation: sum
  description: Aura Graph Analytics consumption at $0.40 per GB-hour.
  dimensions:
  - region
  - workspace
  name: graph_analytics_gb_hours
  unit: GB-hour
- aggregation: avg
  description: AuraDB Virtual Dedicated Cloud custom-contracted instances.
  dimensions:
  - region
  - tenant
  name: virtual_dedicated_cloud
  unit: instance-month
- aggregation: avg
  description: Persistent storage co-scaled with selected instance size.
  dimensions:
  - instance
  name: storage_gb_month
  unit: GB-month
- aggregation: avg
  description: Backup retention storage (7/30/60 days depending on tier).
  dimensions:
  - instance
  - tier
  name: backups_gb_month
  unit: GB-month
- aggregation: sum
  description: Self-managed Neo4j Enterprise / Infinigraph subscription seats.
  dimensions:
  - edition
  - tenant
  name: enterprise_subscription
  unit: month
name: Neo4J Finops
provider_name: Neo4j
provider_slug: neo4j
publisher_name: Neo4j, Inc.
service_category: Database
slug: neo4j-finops
source_filename: neo4j-finops.yml
source_heading: FinOps Profile
source_url: https://neo4j.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Neo4j\nproviderId: neo4j\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Graph Database\n  - AuraDB\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Neo4j: AuraDB billed per GB-RAM-month with size scaling memory\n  + CPU + storage together; Aura Graph Analytics billed per GB-hour; self-managed Enterprise via annual\n  contract.'\nsources:\n  - https://neo4j.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Neo4j, Inc.\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n\
  \    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Neo4j\n  ServiceCategory: Database\n  ServiceSubcategory: Graph Database\n  ProviderName: Neo4j\n  PublisherName: Neo4j, Inc.\n  InvoiceIssuerName: Neo4j, Inc.\n  BillingCurrency: USD\n  PricingCategory: Pay-As-You-Go\n  PricingUnit: GB-month\nmeters:\n  - name: auradb_professional_gb_month\n    description: AuraDB Professional capacity at $65 per GB RAM per month (min 1 GB).\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - instance\n      - cloud\n  - name: auradb_business_critical_gb_month\n    description: AuraDB Business Critical capacity at $146 per GB RAM per month (min 2 GB).\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - instance\n      - cloud\n  - name: graph_analytics_gb_hours\n    description: Aura Graph Analytics consumption at $0.40 per GB-hour.\n    unit: GB-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - workspace\n\
  \  - name: virtual_dedicated_cloud\n    description: AuraDB Virtual Dedicated Cloud custom-contracted instances.\n    unit: instance-month\n    aggregation: avg\n    dimensions:\n      - region\n      - tenant\n  - name: storage_gb_month\n    description: Persistent storage co-scaled with selected instance size.\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - instance\n  - name: backups_gb_month\n    description: Backup retention storage (7/30/60 days depending on tier).\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - instance\n      - tier\n  - name: enterprise_subscription\n    description: Self-managed Neo4j Enterprise / Infinigraph subscription seats.\n    unit: month\n    aggregation: sum\n    dimensions:\n      - edition\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Use the Aura Console billing dashboard for per-instance GB-RAM-month and GB-hour usage;\n      export billing CSV for chargeback. Self-managed customers track\
  \ license metrics via Neo4j Operations\n      Manager.\n  - name: Allocation\n    description: Tag AuraDB instances with project / team labels in the Aura Console; map workspaces in\n      Aura Graph Analytics to cost centers; use separate projects per environment (dev/stage/prod).\n  - name: Optimization\n    description: Right-size AuraDB instances based on p95 query latency, not peak; pause non-prod instances\n      during off-hours (Aura supports pausing); choose Aura Graph Analytics on-demand for batch workloads\n      vs. always-on AuraDB; consolidate small graphs into one instance where governance allows.\n  - name: Accountability\n    description: Set per-project Aura spend ceilings; alert on instance-size upgrades; review backup\n      retention against compliance requirements; review Graph Analytics GB-hour spikes monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/neo4j/refs/heads/main/finops/neo4j-finops.yml
sources:
- https://neo4j.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Graph Database
- AuraDB
- Cost Management
---
