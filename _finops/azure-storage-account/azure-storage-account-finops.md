---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: blob.json
  format: json
  label: Azure Blob Storage API
  slug: azure-blob-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/storage/data-plane/Microsoft.BlobStorage/stable/2021-12-02/blob.json
- filename: azure-storage-account-management-openapi.yaml
  format: yaml
  label: Azure Queue Storage API
  slug: azure-queue-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-storage-account/refs/heads/main/openapi/azure-storage-account-management-openapi.yaml
- filename: azure-storage-account-management-openapi.yaml
  format: yaml
  label: Azure Table Storage API
  slug: azure-table-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-storage-account/refs/heads/main/openapi/azure-storage-account-management-openapi.yaml
- filename: azure-storage-account-management-openapi.yaml
  format: yaml
  label: Azure File Storage API
  slug: azure-file-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-storage-account/refs/heads/main/openapi/azure-storage-account-management-openapi.yaml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure Storage: per-GB-month capacity, per-10K-transaction operations, per-GB egress, and tier-based pricing (Hot/Cool/Cold/Archive on Blob; Standard/Premium on Files). Reserved Capacity covers Block Blob and Azure Files for committed workloads.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Pay-As-You-Go
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Storage
  ServiceName: Azure Storage
layout: finops
meters:
- aggregation: avg
  description: Block / page / append blob storage by access tier
  dimensions:
  - access_tier
  - redundancy
  - region
  - account
  name: blob_capacity
  unit: GB-month
- aggregation: sum
  description: Read / write / list / scan operations on blob storage
  dimensions:
  - operation_type
  - access_tier
  - region
  name: blob_transactions
  unit: operation
- aggregation: avg
  description: Azure Files capacity
  dimensions:
  - tier
  - redundancy
  - region
  name: file_capacity
  unit: GB-month
- aggregation: sum
  description: Azure Files SMB/NFS operations
  dimensions:
  - operation_type
  - region
  name: file_transactions
  unit: operation
- aggregation: sum
  description: Queue and Table operations
  dimensions:
  - service
  - region
  name: queue_table_transactions
  unit: operation
- aggregation: sum
  description: Cold / Archive retrieval throughput charges
  dimensions:
  - tier
  name: data_retrieval
  unit: GB
- aggregation: sum
  description: Cross-region / internet egress
  dimensions:
  - source_region
  - destination
  name: egress_bandwidth
  unit: GB
name: Azure Storage Account Finops
provider_name: Azure Storage Account
provider_slug: azure-storage-account
publisher_name: Microsoft Corporation
service_category: Storage
slug: azure-storage-account-finops
source_filename: azure-storage-account-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/storage/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Storage Account\nproviderId: azure-storage-account\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Storage\n  - Blob\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Azure Storage: per-GB-month capacity, per-10K-transaction operations,\n  per-GB egress, and tier-based pricing (Hot/Cool/Cold/Archive on Blob; Standard/Premium on Files). Reserved\n  Capacity covers Block Blob and Azure Files for committed workloads.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/storage/\n  - https://learn.microsoft.com/en-us/azure/storage/common/scalability-targets-standard-account\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Microsoft Corporation\nserviceCategory: Storage\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Azure Storage\n  ServiceCategory: Storage\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Pay-As-You-Go\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: blob_capacity\n    description: Block / page / append blob storage by access tier\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - access_tier\n      - redundancy\n      - region\n      - account\n  - name: blob_transactions\n    description: Read / write / list / scan operations on blob storage\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - operation_type\n      - access_tier\n      - region\n  - name: file_capacity\n  \
  \  description: Azure Files capacity\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - tier\n      - redundancy\n      - region\n  - name: file_transactions\n    description: Azure Files SMB/NFS operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - operation_type\n      - region\n  - name: queue_table_transactions\n    description: Queue and Table operations\n    unit: operation\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n  - name: data_retrieval\n    description: Cold / Archive retrieval throughput charges\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - tier\n  - name: egress_bandwidth\n    description: Cross-region / internet egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - source_region\n      - destination\nprinciples:\n  - name: Visibility\n    description: Use Storage Insights, Storage Analytics metrics, and Azure Cost Management cost-per-account\n      breakdowns to view capacity,\
  \ transaction, and egress costs.\n  - name: Allocation\n    description: Apply tags to storage accounts; use one account per workload; map costs by tag/container/blob\n      prefix using Storage Inventory and cost-allocation rules.\n  - name: Optimization\n    description: Use lifecycle management to tier blobs Hot -> Cool -> Cold -> Archive automatically;\n      enable blob versioning carefully (cost grows with versions); right-size redundancy (LRS vs GRS);\n      buy Reserved Capacity for steady-state; use private endpoints to avoid egress.\n  - name: Accountability\n    description: Set per-account alerts on capacity and transaction growth; assign account owners; review\n      lifecycle policies and orphan blobs/snapshots monthly.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-storage-account/refs/heads/main/finops/azure-storage-account-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/storage/
- https://learn.microsoft.com/en-us/azure/storage/common/scalability-targets-standard-account
specification: FinOps Framework
tags:
- Storage
- Blob
- FinOps
- FOCUS
---
