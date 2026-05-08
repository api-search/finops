---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: tidb-cloud-api-openapi.yml
  format: yaml
  label: TiDB Cloud API
  slug: tidb-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tidb/refs/heads/main/openapi/tidb-cloud-api-openapi.yml
- filename: tidb-cloud-data-service-openapi.yml
  format: yaml
  label: TiDB Cloud Data Service API
  slug: tidb-cloud-data-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tidb/refs/heads/main/openapi/tidb-cloud-data-service-openapi.yml
- filename: tidb-cloud-chat2query-openapi.yml
  format: yaml
  label: TiDB Cloud Chat2Query API
  slug: tidb-cloud-chat2query-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tidb/refs/heads/main/openapi/tidb-cloud-chat2query-openapi.yml
- filename: tidb-http-api-openapi.yml
  format: yaml
  label: TiDB HTTP API
  slug: tidb-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/tidb/refs/heads/main/openapi/tidb-http-api-openapi.yml
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
description: 'FOCUS-aligned FinOps for TiDB Cloud: Request-Unit and storage metering on Starter/Essential/Premium, hourly instance billing on Dedicated, and contract-based licensing on Self-Managed.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: PingCAP, Inc.
  ProviderName: PingCAP
  PublisherName: PingCAP, Inc.
  ServiceCategory: Database
  ServiceName: TiDB Cloud
layout: finops
meters:
- aggregation: sum
  dimensions:
  - cluster
  - region
  - tier
  name: request_units
  unit: request-unit
- aggregation: max
  dimensions:
  - cluster
  - region
  name: row_storage
  unit: GB-month
- aggregation: max
  dimensions:
  - cluster
  - region
  name: column_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - cluster
  - node_type
  - cloud_provider
  - region
  name: dedicated_node_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - cluster
  - region
  name: data_transfer
  unit: GB
name: Tidb Finops
provider_name: tidb
provider_slug: tidb
publisher_name: PingCAP, Inc.
service_category: Database
slug: tidb-finops
source_filename: tidb-finops.yml
source_heading: FinOps Profile
source_url: https://www.pingcap.com/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: tidb\nproviderId: tidb\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Database\n  - Cloud\n  - HTAP\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for TiDB Cloud: Request-Unit and storage metering on Starter/Essential/Premium,\n  hourly instance billing on Dedicated, and contract-based licensing on Self-Managed.'\nsources:\n  - https://www.pingcap.com/pricing/\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: PingCAP, Inc.\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Subscription\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n\
  \    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: TiDB Cloud\n  ServiceCategory: Database\n  ProviderName: PingCAP\n  PublisherName: PingCAP, Inc.\n  InvoiceIssuerName: PingCAP, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: request_units\n    unit: request-unit\n    aggregation: sum\n    dimensions:\n      - cluster\n      - region\n      - tier\n  - name: row_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - cluster\n      - region\n  - name: column_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - cluster\n      - region\n  - name: dedicated_node_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - cluster\n      - node_type\n      - cloud_provider\n      - region\n  - name: data_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - cluster\n      - region\nprinciples:\n  - name: Visibility\n    description: Use\
  \ the TiDB Cloud console billing dashboard and exported invoices to see RU consumption,\n      storage growth, and Dedicated node-hours per cluster.\n  - name: Allocation\n    description: Allocate cost by cluster name and project tags; tag clusters with the owning team and\n      environment so RU and storage spend roll up cleanly.\n  - name: Optimization\n    description: For Starter, tune queries to reduce RU consumption and use spend limits; for Dedicated,\n      right-size vCPU node counts (4–32 vCPU options) and consolidate underutilized clusters.\n  - name: Accountability\n    description: Assign a database platform owner accountable for the PingCAP account, free-tier headroom,\n      and quarterly true-up against RU and node-hour burn.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tidb/refs/heads/main/finops/tidb-finops.yml
sources:
- https://www.pingcap.com/pricing/
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- Database
- Cloud
- HTAP
- FinOps
- FOCUS
---
