---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Amazon Redshift API
  slug: amazon-redshift-api
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/redshift/2012-12-01/openapi.yaml
- filename: amazon-redshift-data-api-openapi.yml
  format: yaml
  label: Amazon Redshift Data API
  slug: amazon-redshift-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-redshift/refs/heads/main/openapi/amazon-redshift-data-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Amazon Redshift: per-RPU-hour Serverless billing, per-node-hour Provisioned billing on RA3, Redshift Managed Storage at $0.024/GB-month, plus Concurrency Scaling overage, Reserved Instances, and Savings Plans.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Analytics
  ServiceName: Amazon Redshift
  ServiceSubcategory: Data Warehouse
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - workgroup
  - namespace
  name: rpu_hours
  unit: RPU-hour
- aggregation: sum
  dimensions:
  - region
  - cluster
  - node_type
  name: node_hours
  unit: node-hour
- aggregation: sum
  dimensions:
  - region
  - cluster_or_namespace
  name: managed_storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: concurrency_scaling_seconds
  unit: cs-second
- aggregation: sum
  dimensions:
  - region
  - cluster_or_namespace
  name: backup_storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - direction
  name: data_transfer_gb
  unit: GB
name: Amazon Redshift Finops
provider_name: Amazon Redshift
provider_slug: amazon-redshift
publisher_name: Amazon Web Services, Inc.
service_category: Analytics / Data Warehouse
slug: amazon-redshift-finops
source_filename: amazon-redshift-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/redshift/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon Redshift\nproviderId: amazon-redshift\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Data Warehouse\n  - Redshift\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon Redshift: per-RPU-hour Serverless billing, per-node-hour\n  Provisioned billing on RA3, Redshift Managed Storage at $0.024/GB-month, plus Concurrency Scaling overage,\n  Reserved Instances, and Savings Plans.'\nsources:\n  - https://aws.amazon.com/redshift/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Analytics / Data Warehouse\nbillingModel:\n  pricingCategory: Pay-As-You-Go +\
  \ Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Redshift\n  ServiceCategory: Analytics\n  ServiceSubcategory: Data Warehouse\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: rpu_hours\n    unit: RPU-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - workgroup\n      - namespace\n  - name: node_hours\n    unit: node-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n      - node_type\n  - name: managed_storage_gb_month\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster_or_namespace\n  - name: concurrency_scaling_seconds\n    unit: cs-second\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name:\
  \ backup_storage_gb_month\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster_or_namespace\n  - name: data_transfer_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\nprinciples:\n  - name: Visibility\n    description: Use Cost Explorer with the Redshift dimension, the Redshift console's Performance and\n      Concurrency Scaling reports, system tables (STL_QUERY, SVL_QUERY_METRICS), and CUR / FOCUS export.\n  - name: Allocation\n    description: Tag clusters/workgroups/namespaces with Environment, Team, Use Case; enable cost allocation\n      tags so charges flow into FOCUS columns.\n  - name: Optimization\n    description: Pause/scale-down Provisioned clusters, choose Serverless for spiky workloads, commit to\n      Reserved Instances for steady production, monitor RA3 storage growth, use Concurrency Scaling free-hour\n      credits before paying overage, and use Materialized Views and Auto-Vacuum to reduce\
  \ query cost.\n  - name: Accountability\n    description: Set AWS Budgets per cluster tag, alert on Concurrency Scaling overage, and review monthly\n      RPU-hour utilization for Serverless workgroup right-sizing.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-redshift/refs/heads/main/finops/amazon-redshift-finops.yml
sources:
- https://aws.amazon.com/redshift/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Data Warehouse
- Redshift
- Cost Management
---
