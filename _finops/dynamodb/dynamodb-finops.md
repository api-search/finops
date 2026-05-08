---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dynamodb-openapi.yml
  format: yaml
  label: Amazon DynamoDB API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynamodb/refs/heads/main/openapi/dynamodb-openapi.yml
- filename: dynamodb-streams-asyncapi.yml
  format: yaml
  label: Amazon DynamoDB Streams API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynamodb/refs/heads/main/asyncapi/dynamodb-streams-asyncapi.yml
- filename: openapi.yaml
  format: yaml
  label: Amazon DynamoDB Accelerator (DAX) API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/dax/2017-04-19/openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Amazon DynamoDB: pay-per-request and provisioned-capacity billing with optional Reserved Capacity commitments, per AWS Region.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  PricingUnit: request-unit / capacity-unit-hour / GB-month
  ProviderName: Amazon Web Services
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Database
  ServiceName: Amazon DynamoDB
layout: finops
meters:
- aggregation: sum
  dimensions:
  - region
  - table
  - consistency
  name: read_request_units
  unit: request
- aggregation: sum
  dimensions:
  - region
  - table
  - transaction
  name: write_request_units
  unit: request
- aggregation: sum
  dimensions:
  - region
  - table
  name: provisioned_read_capacity
  unit: RCU-hour
- aggregation: sum
  dimensions:
  - region
  - table
  name: provisioned_write_capacity
  unit: WCU-hour
- aggregation: avg
  dimensions:
  - region
  - table
  - storage_class
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - table
  name: streams_reads
  unit: request
- aggregation: avg
  dimensions:
  - region
  - backup_type
  name: backup_storage
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - destination
  name: data_transfer_out
  unit: GB
name: Dynamodb Finops
provider_name: Amazon DynamoDB
provider_slug: dynamodb
publisher_name: Amazon Web Services, Inc.
service_category: Database
slug: dynamodb-finops
source_filename: dynamodb-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/dynamodb/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon DynamoDB\nproviderId: dynamodb\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Database\n  - NoSQL\ndescription: 'FOCUS-aligned FinOps for Amazon DynamoDB: pay-per-request and provisioned-capacity billing\n  with optional Reserved Capacity commitments, per AWS Region.'\nsources:\n  - https://aws.amazon.com/dynamodb/pricing/\n  - https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html\n  - https://focus.finops.org/focus-specification/v1-3/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Database\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Amazon DynamoDB\n  ServiceCategory: Database\n  ProviderName: Amazon Web Services\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\n  PricingUnit: request-unit / capacity-unit-hour / GB-month\nmeters:\n  - name: read_request_units\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - table\n      - consistency\n  - name: write_request_units\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - table\n      - transaction\n  - name: provisioned_read_capacity\n    unit: RCU-hour\n    aggregation: sum\n    dimensions:\n      - region\n      - table\n  - name: provisioned_write_capacity\n    unit: WCU-hour\n    aggregation: sum\n    dimensions:\n      - region\n      -\
  \ table\n  - name: storage_gb_month\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - table\n      - storage_class\n  - name: streams_reads\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - table\n  - name: backup_storage\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - backup_type\n  - name: data_transfer_out\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - destination\nprinciples:\n  - name: Visibility\n    description: Use AWS Cost Explorer, the Cost and Usage Report (CUR), and CloudWatch DynamoDB metrics\n      (ConsumedReadCapacityUnits, ConsumedWriteCapacityUnits, ThrottledRequests) to track consumption\n      per table and region.\n  - name: Allocation\n    description: Tag tables with cost-allocation tags (team, environment, application) and enable user-defined\n      cost allocation in the AWS Billing console for chargeback.\n  - name: Optimization\n\
  \    description: Switch idle workloads to On-Demand, apply Reserved Capacity for steady provisioned RCU/WCU,\n      use DynamoDB Standard-IA storage class for cold tables, enable auto-scaling, and adopt DAX caching\n      to lower read costs.\n  - name: Accountability\n    description: Set CloudWatch billing alarms and AWS Budgets per tag dimension; review per-table costs\n      monthly against the CUR and investigate ThrottledRequests spikes.\nmaintainers:\n  - name: Amazon Web Services\n    email: aws-dynamodb@amazon.com\n    url: https://aws.amazon.com\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dynamodb/refs/heads/main/finops/dynamodb-finops.yml
sources:
- https://aws.amazon.com/dynamodb/pricing/
- https://docs.aws.amazon.com/cur/latest/userguide/what-is-cur.html
- https://focus.finops.org/focus-specification/v1-3/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Database
- NoSQL
---
