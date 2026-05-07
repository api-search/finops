---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-neptune-management-openapi.yml
  format: yaml
  label: Amazon Neptune Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-management-openapi.yml
- filename: amazon-neptune-data-openapi.yml
  format: yaml
  label: Amazon Neptune Data API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-data-openapi.yml
- filename: amazon-neptune-gremlin-openapi.yml
  format: yaml
  label: Neptune Gremlin API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-gremlin-openapi.yml
- filename: amazon-neptune-sparql-openapi.yml
  format: yaml
  label: Neptune SPARQL API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-sparql-openapi.yml
- filename: amazon-neptune-opencypher-openapi.yml
  format: yaml
  label: Neptune openCypher API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-opencypher-openapi.yml
- filename: amazon-neptune-streams-openapi.yml
  format: yaml
  label: Neptune Streams API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-streams-openapi.yml
- filename: amazon-neptune-loader-openapi.yml
  format: yaml
  label: Neptune Loader API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-loader-openapi.yml
- filename: amazon-neptune-ml-openapi.yml
  format: yaml
  label: Neptune ML API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-ml-openapi.yml
- filename: amazon-neptune-analytics-openapi.yml
  format: yaml
  label: Neptune Analytics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/openapi/amazon-neptune-analytics-openapi.yml
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
description: 'FOCUS-aligned FinOps for Amazon Neptune: per-instance-hour plus storage/IO (Standard) or bundled (I/O-Optimized) on the provisioned model, NCU-second billing on Serverless, and separate backup storage charges.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Databases
  ServiceName: Amazon Neptune
  ServiceSubcategory: Graph Database
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - cluster
  - instance_class
  - storage_config
  name: instance_hours
  unit: instance-hour
- aggregation: sum
  dimensions:
  - region
  - cluster
  - storage_config
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: io_requests
  unit: million-requests
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: ncu_seconds
  unit: NCU-second
- aggregation: sum
  dimensions:
  - region
  - cluster
  name: backup_storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - direction
  name: data_transfer_gb
  unit: GB
name: Amazon Neptune Finops
provider_name: Amazon Neptune
provider_slug: amazon-neptune
publisher_name: Amazon Web Services, Inc.
service_category: Database / Graph
slug: amazon-neptune-finops
source_filename: amazon-neptune-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/neptune/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon Neptune\nproviderId: amazon-neptune\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Database\n  - Graph Database\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon Neptune: per-instance-hour plus storage/IO (Standard) or\n  bundled (I/O-Optimized) on the provisioned model, NCU-second billing on Serverless, and separate backup\n  storage charges.'\nsources:\n  - https://aws.amazon.com/neptune/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Database / Graph\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n\
  \  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Neptune\n  ServiceCategory: Databases\n  ServiceSubcategory: Graph Database\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: instance_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n      - instance_class\n      - storage_config\n  - name: storage_gb_month\n    unit: GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n      - storage_config\n  - name: io_requests\n    unit: million-requests\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name: ncu_seconds\n    unit: NCU-second\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name: backup_storage_gb_month\n    unit:\
  \ GB-month\n    aggregation: sum\n    dimensions:\n      - region\n      - cluster\n  - name: data_transfer_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\nprinciples:\n  - name: Visibility\n    description: Use CloudWatch Neptune metrics (CPUUtilization, GremlinRequestsPerSec, MainRequestQueuePendingRequests),\n      Performance Insights, and AWS CUR / FOCUS export.\n  - name: Allocation\n    description: Tag clusters with Application, Team, Environment; enable cost allocation tags so charges\n      flow into FOCUS columns.\n  - name: Optimization\n    description: Right-size instance class; choose Standard vs I/O-Optimized based on monthly IO; use Serverless\n      for variable workloads; pause dev/test clusters; commit to Reserved Instances at 1- or 3-year for\n      steady production.\n  - name: Accountability\n    description: Set AWS Budgets per cluster tag, alert on storage growth and IO spikes, review monthly\n      utilization for downsizing.\n\
  maintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-neptune/refs/heads/main/finops/amazon-neptune-finops.yml
sources:
- https://aws.amazon.com/neptune/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database
- Graph Database
- Cost Management
---
