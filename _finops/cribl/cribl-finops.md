---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cribl-cloud-api-openapi.yml
  format: yaml
  label: Cribl Cloud API
  slug: cribl-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/openapi/cribl-cloud-api-openapi.yml
- filename: cribl-stream-api-openapi.yml
  format: yaml
  label: Cribl Stream API
  slug: cribl-stream-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/openapi/cribl-stream-api-openapi.yml
- filename: cribl-edge-api-openapi.yml
  format: yaml
  label: Cribl Edge API
  slug: cribl-edge-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/openapi/cribl-edge-api-openapi.yml
- filename: cribl-search-api-openapi.yml
  format: yaml
  label: Cribl Search API
  slug: cribl-search-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/openapi/cribl-search-api-openapi.yml
- filename: cribl-lake-api-openapi.yml
  format: yaml
  label: Cribl Lake API
  slug: cribl-lake-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/openapi/cribl-lake-api-openapi.yml
- filename: cribl-as-code-api-openapi.yml
  format: yaml
  label: Cribl As Code API
  slug: cribl-as-code-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/openapi/cribl-as-code-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  chargeFrequency: Recurring
  pricingCategory: Consumption-Based + Subscription
description: FOCUS-aligned FinOps for Cribl - consumption-based licensing on processed-data volume (TB/day) plus tier-bound capacity (worker groups, worker processes, edge nodes, Lake capacity, search executors). Free tier covers 1 TB/day; Standard and Enterprise are negotiated commercially.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cribl, Inc.
  PricingCategory: Usage-Based
  ProviderName: Cribl
  PublisherName: Cribl, Inc.
  ServiceCategory: Observability Pipeline
  ServiceName: Cribl
layout: finops
meters:
- aggregation: sum
  description: Volume of telemetry data processed through Cribl Stream / Edge per day
  dimensions:
  - source
  - destination
  - pipeline
  - worker_group
  - environment
  name: data_processed
  unit: TB
- aggregation: max
  description: Worker process count concurrently running across worker groups
  dimensions:
  - worker_group
  - environment
  name: worker_processes
  unit: worker_process
- aggregation: max
  description: Cribl Edge agents deployed across the fleet
  dimensions:
  - fleet
  - environment
  name: edge_nodes
  unit: edge_node
- aggregation: avg
  description: Cribl Lake storage consumed
  dimensions:
  - dataset
  - retention_class
  name: lake_storage
  unit: GB-month
- aggregation: max
  description: Concurrent Cribl Search executors
  dimensions:
  - workspace
  - environment
  name: search_executors
  unit: executor
- aggregation: max
  description: Annual / monthly subscription baseline tied to the platform tier
  dimensions:
  - tier
  - workspace
  name: subscription_fee
  unit: month
name: Cribl Finops
provider_name: Cribl
provider_slug: cribl
publisher_name: Cribl, Inc.
service_category: Observability Pipeline
slug: cribl-finops
source_filename: cribl-finops.yml
source_heading: FinOps Profile
source_url: https://cribl.io/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cribl\nproviderId: cribl\npublisherName: Cribl, Inc.\nserviceCategory: Observability Pipeline\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Configuration\n  - Data Lake\n  - Data Pipelines\n  - Data Routing\n  - Edge Computing\n  - Observability\n  - Search\n  - Security Data\n  - Stream Processing\n  - Telemetry\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FOCUS-aligned FinOps for Cribl - consumption-based licensing on processed-data volume\n  (TB/day) plus tier-bound capacity (worker groups, worker processes, edge nodes, Lake capacity, search\n  executors). Free tier covers 1 TB/day; Standard and Enterprise\
  \ are negotiated commercially.\nsources:\n  - https://cribl.io/pricing/\n  - https://docs.cribl.io/api-reference/\n  - https://focus.finops.org/focus-specification/v1-3/\nbillingModel:\n  pricingCategory: Consumption-Based + Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cribl\n  ServiceCategory: Observability Pipeline\n  ProviderName: Cribl\n  PublisherName: Cribl, Inc.\n  InvoiceIssuerName: Cribl, Inc.\n  PricingCategory: Usage-Based\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: data_processed\n    description: Volume of telemetry data processed through Cribl Stream / Edge per day\n    unit: TB\n    aggregation: sum\n    dimensions:\n      - source\n      - destination\n      - pipeline\n      - worker_group\n      - environment\n  - name: worker_processes\n    description: Worker\
  \ process count concurrently running across worker groups\n    unit: worker_process\n    aggregation: max\n    dimensions:\n      - worker_group\n      - environment\n  - name: edge_nodes\n    description: Cribl Edge agents deployed across the fleet\n    unit: edge_node\n    aggregation: max\n    dimensions:\n      - fleet\n      - environment\n  - name: lake_storage\n    description: Cribl Lake storage consumed\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - dataset\n      - retention_class\n  - name: search_executors\n    description: Concurrent Cribl Search executors\n    unit: executor\n    aggregation: max\n    dimensions:\n      - workspace\n      - environment\n  - name: subscription_fee\n    description: Annual / monthly subscription baseline tied to the platform tier\n    unit: month\n    aggregation: max\n    dimensions:\n      - tier\n      - workspace\nprinciples:\n  - name: Visibility\n    description: Use the Cribl Cloud dashboard, Cribl Search, and per-pipeline\
  \ metrics to track TB/day\n      processed by source, destination, pipeline, and worker group. Export usage telemetry into the\n      same observability stack you bill for.\n  - name: Allocation\n    description: Allocate cost by source system (security, infra, app), destination (SIEM, lake, archive),\n      and team. Cribl's pipeline-level metrics make per-team chargeback feasible for shared deployments.\n  - name: Optimization\n    description: Cribl's core ROI is volume reduction - use Reduce, Suppress, Sample, and Drop functions\n      in pipelines to shrink data before downstream-tool ingest cost; route low-value telemetry to\n      Cribl Lake instead of premium SIEM ingest; right-size worker process count to match TB/day; use\n      Cribl As Code (Terraform / SDK) to enforce the optimization patterns across environments.\n  - name: Accountability\n    description: Assign each pipeline an owner; alert on TB/day burn-rate at the worker-group level\n      so over-budget telemetry sources\
  \ are caught before a renewal cycle. Tie Cribl ROI metrics (pre-\n      vs post-Cribl downstream cost) into FinOps reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cribl/refs/heads/main/finops/cribl-finops.yml
sources:
- https://cribl.io/pricing/
- https://docs.cribl.io/api-reference/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Configuration
- Data Lake
- Data Pipelines
- Data Routing
- Edge Computing
- Observability
- Search
- Security Data
- Stream Processing
- Telemetry
- FinOps
- Cost Management
- FOCUS
---
