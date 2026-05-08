---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: timescaledb-openapi.yml
  format: yaml
  label: Tiger Cloud REST API
  slug: tiger-cloud-rest
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/timescaledb/refs/heads/main/openapi/timescaledb-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly (in arrears)
  chargeCategories:
  - Usage
  - Purchase
  - Adjustment
  pricingCategory: Usage
description: FOCUS-aligned FinOps profile for Tiger Cloud (the managed TimescaleDB service). Compute is metered hourly per service-hour at a tier-specific rate that varies by region. Storage is metered as average GB-hour, priced uniformly across regions. Billed monthly in arrears in USD.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tiger Data
  PricingUnit: service-hour
  ProviderName: Tiger Data
  PublisherName: Tiger Data
  ServiceCategory: Database
  ServiceName: Tiger Cloud
layout: finops
meters:
- aggregation: sum
  description: Hourly metering of running database services at tier-specific rates.
  dimensions:
  - service_id
  - tier
  - region
  name: compute_service_hours
  unit: service-hour
- aggregation: avg
  description: Average GB-hours of high-performance storage attached to services.
  dimensions:
  - service_id
  name: storage_gb_hour_high_perf
  unit: GB-hour
- aggregation: avg
  description: Average GB-hours of tiered/object storage (cold).
  dimensions:
  - service_id
  name: storage_gb_hour_tiered
  unit: GB-hour
- aggregation: sum
  description: Egress bandwidth out of Tiger Cloud services where applicable.
  dimensions:
  - service_id
  - region
  name: data_transfer
  unit: GB
- aggregation: sum
  description: Read-replica service-hours billed in addition to primary.
  dimensions:
  - service_id
  - replica_id
  name: replicas
  unit: service-hour
name: Timescaledb Finops
provider_name: TimescaleDB / Tiger Data
provider_slug: timescaledb
publisher_name: Tiger Data
service_category: Database (Time-Series)
slug: timescaledb-finops
source_filename: timescaledb-finops.yml
source_heading: FinOps Profile
source_url: https://www.tigerdata.com/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: TimescaleDB / Tiger Data\nproviderId: timescaledb\ncreated: '2026-05-08'\nmodified: '2026-05-08'\nreconciled: true\ntags:\n- Database\n- Time-Series\n- PostgreSQL\n- Open Source\n- Cloud\n- FinOps\n- Cost Management\n- FOCUS\ndescription: >-\n  FOCUS-aligned FinOps profile for Tiger Cloud (the managed TimescaleDB\n  service). Compute is metered hourly per service-hour at a tier-specific rate\n  that varies by region. Storage is metered as average GB-hour, priced\n  uniformly across regions. Billed monthly in arrears in USD.\nnotes: >-\n  Cost Explorer in the Tiger Console exposes per-service breakdown; storage\n  tiering between high-perf and object/tiered storage is a primary\n  optimisation lever for time-series workloads.\nsources:\n- https://www.tigerdata.com/pricing\n- https://www.tigerdata.com/docs/use-timescale/billing\n- https://focus.finops.org/focus-specification/v1-3/\n\
  alignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Tiger Data\nserviceCategory: Database (Time-Series)\nbillingModel:\n  pricingCategory: Usage\n  billingFrequency: Monthly (in arrears)\n  billingCurrency: USD\n  chargeCategories:\n  - Usage\n  - Purchase\n  - Adjustment\nfocusColumns:\n  ServiceName: Tiger Cloud\n  ServiceCategory: Database\n  ProviderName: Tiger Data\n  PublisherName: Tiger Data\n  InvoiceIssuerName: Tiger Data\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: service-hour\nmeters:\n- name: compute_service_hours\n  description: Hourly metering of running database services at tier-specific rates.\n  unit: service-hour\n  aggregation: sum\n  dimensions:\n  - service_id\n  - tier\n  - region\n- name: storage_gb_hour_high_perf\n  description: Average GB-hours of high-performance\
  \ storage attached to services.\n  unit: GB-hour\n  aggregation: avg\n  dimensions:\n  - service_id\n- name: storage_gb_hour_tiered\n  description: Average GB-hours of tiered/object storage (cold).\n  unit: GB-hour\n  aggregation: avg\n  dimensions:\n  - service_id\n- name: data_transfer\n  description: Egress bandwidth out of Tiger Cloud services where applicable.\n  unit: GB\n  aggregation: sum\n  dimensions:\n  - service_id\n  - region\n- name: replicas\n  description: Read-replica service-hours billed in addition to primary.\n  unit: service-hour\n  aggregation: sum\n  dimensions:\n  - service_id\n  - replica_id\nprinciples:\n- name: Visibility\n  description: Use Tiger Console Cost Explorer + invoice CSV for monthly spend; tag services with project/team metadata.\n- name: Allocation\n  description: One-service-per-team or labelled service names to map to FOCUS BillingAccountId / ResourceTag.\n- name: Optimization\n  description: Right-size tier; enable Hypercore (columnstore) compression\
  \ on cold partitions; move historical chunks to tiered storage.\n- name: Accountability\n  description: Assign service owners; alert on monthly spend > budget via Tiger Console notifications.\nmaintainers:\n- FN: Kin Lane\n  email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/timescaledb/refs/heads/main/finops/timescaledb-finops.yml
sources:
- https://www.tigerdata.com/pricing
- https://www.tigerdata.com/docs/use-timescale/billing
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Database
- Time-Series
- PostgreSQL
- Open Source
- Cloud
- FinOps
- Cost Management
- FOCUS
---
