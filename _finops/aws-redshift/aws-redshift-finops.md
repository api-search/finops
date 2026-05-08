---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aws-redshift-openapi.json
  format: json
  label: Amazon Redshift API
  slug: amazon-redshift-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-redshift/refs/heads/main/openapi/aws-redshift-openapi.json
- filename: aws-redshift-data-openapi.json
  format: json
  label: Amazon Redshift Data API
  slug: amazon-redshift-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aws-redshift/refs/heads/main/openapi/aws-redshift-data-openapi.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Refund
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Amazon Redshift: dual-shape billing — Serverless RPU-hour vs Provisioned per-node-hour — plus separately metered Redshift Managed Storage, Spectrum scans, concurrency scaling, and cross-region transfer. Reserved Instances and Serverless commitments provide committed-use discounts.'
focus_columns:
  BillingCurrency: USD
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  RegionId: varies
  ServiceCategory: Analytics
  ServiceName: Amazon Redshift
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - workgroup
  - namespace
  name: serverless_rpu_hours
  unit: RPU-hour
- aggregation: sum
  dimensions:
  - region
  - cluster_identifier
  - node_type
  - billing_mode
  name: provisioned_node_hours
  unit: hour
- aggregation: max
  dimensions:
  - region
  - cluster_or_namespace
  name: managed_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - cluster_identifier
  name: concurrency_scaling_seconds
  unit: second
- aggregation: sum
  dimensions:
  - region
  - schema
  name: spectrum_scanned
  unit: TB
- aggregation: max
  dimensions:
  - region
  - cluster_identifier
  name: backup_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - source_region
  - destination_region
  name: cross_region_transfer
  unit: GB
- aggregation: sum
  name: reserved_node_commitment
  unit: node-month
name: Aws Redshift Finops
provider_name: AWS Redshift
provider_slug: aws-redshift
publisher_name: Amazon Web Services, Inc.
service_category: Analytics / Data Warehouse
slug: aws-redshift-finops
source_filename: aws-redshift-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/redshift/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: AWS Redshift\nproviderId: aws-redshift\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Data Warehouse\n  - Analytics\n  - AWS\ndescription: 'FOCUS-aligned FinOps for Amazon Redshift: dual-shape billing — Serverless RPU-hour vs\n  Provisioned per-node-hour — plus separately metered Redshift Managed Storage, Spectrum scans,\n  concurrency scaling, and cross-region transfer. Reserved Instances and Serverless commitments\n  provide committed-use discounts.'\nsources:\n  - https://aws.amazon.com/redshift/pricing/\n  - https://docs.aws.amazon.com/redshift/latest/mgmt/amazon-redshift-limits.html\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Amazon Web Services, Inc.\nserviceCategory: Analytics / Data Warehouse\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Refund\n    - Credit\nfocusColumns:\n  ServiceName: Amazon Redshift\n  ServiceCategory: Analytics\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  RegionId: varies\nmeters:\n  - name: serverless_rpu_hours\n    unit: RPU-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - workgroup\n      - namespace\n  - name: provisioned_node_hours\n    unit: hour\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster_identifier\n      - node_type\n      - billing_mode\n  - name: managed_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - region\n      - cluster_or_namespace\n  - name:\
  \ concurrency_scaling_seconds\n    unit: second\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster_identifier\n  - name: spectrum_scanned\n    unit: TB\n    aggregation: sum\n    dimensions:\n      - region\n      - schema\n  - name: backup_storage\n    unit: GB-month\n    aggregation: max\n    dimensions:\n      - region\n      - cluster_identifier\n  - name: cross_region_transfer\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_region\n      - destination_region\n  - name: reserved_node_commitment\n    unit: node-month\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use SVL_ / STL_ system tables (e.g. SVL_QUERY_REPORT, STL_USAGE_CONTROL) for\n      per-query/per-user spend signal; in CUR / Cost Explorer split by UsageType (NodeUsage,\n      ServerlessUsage:RPUUsage, RMS:StorageUsage, ConcurrencyScaling:NodeUsage, RedshiftSpectrum). The\n      Redshift console also shows Serverless RPU consumption and concurrency-scaling\
  \ credits.\n  - name: Allocation\n    description: Tag clusters and Serverless namespaces with team / product cost-allocation tags. For\n      shared clusters, attribute via database / schema ownership and per-user query-cost reports.\n  - name: Optimization\n    description: 'Major levers: (1) right-size — RA3 + RMS so storage scales independently of compute;\n      (2) buy Reserved Instances for steady-state provisioned clusters (up to ~75% savings); (3) use\n      Concurrency Scaling rather than oversize the base cluster; (4) WLM tuning to keep ETL out of the\n      interactive queue; (5) Spectrum / data lake offload for rarely scanned cold data; (6) for\n      Serverless, tune base RPU floor and use query monitoring to cap runaway scans.'\n  - name: Accountability\n    description: Data platform team owns Redshift estate and reservation strategy; consuming teams are\n      accountable for query efficiency, predicate pushdown, and table design (sort/dist keys).\nmaintainers:\n  - FN:\
  \ Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aws-redshift/refs/heads/main/finops/aws-redshift-finops.yml
sources:
- https://aws.amazon.com/redshift/pricing/
- https://docs.aws.amazon.com/redshift/latest/mgmt/amazon-redshift-limits.html
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Warehouse
- Analytics
---
