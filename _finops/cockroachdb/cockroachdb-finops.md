---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cockroachdb-cloud-api-openapi.yml
  format: yaml
  label: CockroachDB Cloud API
  slug: cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/openapi/cockroachdb-cloud-api-openapi.yml
- filename: cockroachdb-cluster-api-openapi.yml
  format: yaml
  label: CockroachDB Cluster API
  slug: cluster-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/openapi/cockroachdb-cluster-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  pricingCategory: Resource-Based
description: FOCUS-aligned FinOps for CockroachDB.
focus_columns:
  BillingCurrency: USD
  ProviderName: CockroachDB
  PublisherName: CockroachDB
  ServiceCategory: Distributed SQL Database
  ServiceName: CockroachDB
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - region
  - cloud
  name: vcpu_hours
  unit: vcpu-hour
- aggregation: sum
  name: request_units
  unit: RU
- aggregation: max
  name: storage
  unit: GiB-month
- aggregation: sum
  name: data_transfer
  unit: GB
- aggregation: max
  name: backup_storage
  unit: GiB-month
name: Cockroachdb Finops
provider_name: CockroachDB
provider_slug: cockroachdb
publisher_name: CockroachDB
service_category: Distributed SQL Database
slug: cockroachdb-finops
source_filename: cockroachdb-finops.yml
source_heading: FinOps Profile
source_url: https://www.cockroachlabs.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: CockroachDB\nproviderId: cockroachdb\ncreated: '2026-05-04'\nmodified: '2026-05-04'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Distributed SQL Database\ndescription: FOCUS-aligned FinOps for CockroachDB.\nsources:\n  - https://www.cockroachlabs.com/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: CockroachDB\nserviceCategory: Distributed SQL Database\nbillingModel:\n  pricingCategory: Resource-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\nfocusColumns:\n  ServiceName: CockroachDB\n  ServiceCategory: Distributed SQL Database\n  ProviderName: CockroachDB\n  PublisherName: CockroachDB\n  BillingCurrency: USD\nmeters:\n  - name: vcpu_hours\n    unit:\
  \ vcpu-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - region\n      - cloud\n  - name: request_units\n    unit: RU\n    aggregation: sum\n  - name: storage\n    unit: GiB-month\n    aggregation: max\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n  - name: backup_storage\n    unit: GiB-month\n    aggregation: max\nprinciples:\n  - name: Visibility\n    description: Track CockroachDB consumption monthly.\n  - name: Allocation\n    description: Tag usage to teams/cost centers.\n  - name: Optimization\n    description: Right-size; reclaim unused entitlements.\n  - name: Accountability\n    description: Set spend alerts; quarterly review.\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cockroachdb/refs/heads/main/finops/cockroachdb-finops.yml
sources:
- https://www.cockroachlabs.com/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Distributed SQL Database
---
