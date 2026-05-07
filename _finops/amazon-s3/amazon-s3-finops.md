---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-s3-rest-api-openapi.yml
  format: yaml
  label: Amazon S3 REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-s3/refs/heads/main/openapi/amazon-s3-rest-api-openapi.yml
- filename: amazon-s3-control-api-openapi.yml
  format: yaml
  label: Amazon S3 Control API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-s3/refs/heads/main/openapi/amazon-s3-control-api-openapi.yml
- filename: amazon-s3-tables-api-openapi.yml
  format: yaml
  label: Amazon S3 Tables API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-s3/refs/heads/main/openapi/amazon-s3-tables-api-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Credit
  - Adjustment
  pricingCategory: Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Amazon S3: per-GB-month storage by class, per-1,000-request charges by verb and class, tiered egress with a 100 GB/month free pool, plus separately metered features (replication, inventory, retrieval, lifecycle transitions, S3 Tables).'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Web Services, Inc.
  ProviderName: AWS
  PublisherName: Amazon Web Services, Inc.
  ServiceCategory: Storage
  ServiceName: Amazon Simple Storage Service
  ServiceSubcategory: Object Storage
layout: finops
meters:
- aggregation: avg
  dimensions:
  - region
  - bucket
  - storage_class
  name: storage_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - region
  - bucket
  - operation
  - storage_class
  name: requests
  unit: request
- aggregation: sum
  dimensions:
  - region
  - direction
  - destination
  name: data_transfer_gb
  unit: GB
- aggregation: sum
  dimensions:
  - source_region
  - destination_region
  name: cross_region_replication_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - bucket
  - source_class
  - destination_class
  name: lifecycle_transitions
  unit: object
- aggregation: sum
  dimensions:
  - region
  - bucket
  - retrieval_tier
  name: glacier_retrieval_gb
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - bucket
  name: inventory_objects
  unit: object
name: Amazon S3 Finops
provider_name: Amazon S3
provider_slug: amazon-s3
publisher_name: Amazon Web Services, Inc.
service_category: Storage / Object Storage
slug: amazon-s3-finops
source_filename: amazon-s3-finops.yml
source_heading: FinOps Profile
source_url: https://aws.amazon.com/s3/pricing/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Amazon S3\nproviderId: amazon-s3\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - AWS\n  - Object Storage\n  - S3\n  - Cost Management\ndescription: 'FOCUS-aligned FinOps for Amazon S3: per-GB-month storage by class, per-1,000-request charges\n  by verb and class, tiered egress with a 100 GB/month free pool, plus separately metered features (replication,\n  inventory, retrieval, lifecycle transitions, S3 Tables).'\nsources:\n  - https://aws.amazon.com/s3/pricing/\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Amazon Web Services, Inc.\nserviceCategory: Storage / Object Storage\nbillingModel:\n  pricingCategory: Pay-As-You-Go\n\
  \  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\nfocusColumns:\n  ServiceName: Amazon Simple Storage Service\n  ServiceCategory: Storage\n  ServiceSubcategory: Object Storage\n  ProviderName: AWS\n  PublisherName: Amazon Web Services, Inc.\n  InvoiceIssuerName: Amazon Web Services, Inc.\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: storage_gb_month\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n      - bucket\n      - storage_class\n  - name: requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - region\n      - bucket\n      - operation\n      - storage_class\n  - name: data_transfer_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\n      - destination\n  - name: cross_region_replication_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_region\n      - destination_region\n\
  \  - name: lifecycle_transitions\n    unit: object\n    aggregation: sum\n    dimensions:\n      - region\n      - bucket\n      - source_class\n      - destination_class\n  - name: glacier_retrieval_gb\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - bucket\n      - retrieval_tier\n  - name: inventory_objects\n    unit: object\n    aggregation: sum\n    dimensions:\n      - region\n      - bucket\nprinciples:\n  - name: Visibility\n    description: Use S3 Storage Lens (free metrics, advanced metrics paid), Cost Explorer with the S3 dimension,\n      bucket-level CloudWatch metrics, and CUR / FOCUS export for object-level cost.\n  - name: Allocation\n    description: Tag buckets with Application, Team, Environment; use cost allocation tags so charges flow\n      through FOCUS columns; use S3 Storage Lens groups for grouping prefixes.\n  - name: Optimization\n    description: Use S3 Intelligent-Tiering for unknown access patterns, lifecycle policies to transition\n\
  \      cold data to Glacier classes, S3 Storage Lens recommendations to find inefficient prefixes, multi-part\n      upload cleanup, and CloudFront in front of public buckets to reduce egress.\n  - name: Accountability\n    description: Set AWS Budgets per bucket tag, configure anomaly detection on data transfer, and review\n      Storage Lens dashboards monthly with bucket owners.\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n  - name: Amazon Web Services\n    email: support@aws.amazon.com\n    url: https://aws.amazon.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-s3/refs/heads/main/finops/amazon-s3-finops.yml
sources:
- https://aws.amazon.com/s3/pricing/
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Object Storage
- S3
- Cost Management
---
