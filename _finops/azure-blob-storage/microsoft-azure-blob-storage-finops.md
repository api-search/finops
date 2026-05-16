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
  label: Azure Blob Storage REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/storage/data-plane/Microsoft.BlobStorage/stable/2021-12-02/blob.json
- filename: storage.json
  format: json
  label: Azure Storage Resource Provider REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/storage/resource-manager/Microsoft.Storage/stable/2023-05-01/storage.json
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
description: 'FOCUS-aligned FinOps for Azure Blob Storage: per-GB-month capacity by access tier, per-10,000-transaction fees, retrieval and egress charges, with reserved-capacity commitments available.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Storage
  ServiceName: Azure Blob Storage
layout: finops
meters:
- aggregation: avg
  dimensions:
  - access_tier
  - redundancy
  - region
  - account
  name: capacity_gb_month
  unit: GB-month
- aggregation: sum
  dimensions:
  - access_tier
  - region
  - account
  name: write_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - access_tier
  - region
  - account
  name: read_transactions
  unit: transaction
- aggregation: sum
  dimensions:
  - access_tier
  - region
  name: data_retrieval
  unit: GB
- aggregation: sum
  dimensions:
  - region
  - direction
  name: data_egress
  unit: GB
- aggregation: sum
  dimensions:
  - access_tier
  name: early_deletion
  unit: GB
name: Microsoft Azure Blob Storage Finops
provider_name: Azure Blob Storage
provider_slug: azure-blob-storage
publisher_name: Microsoft Corporation
service_category: Storage / Object Storage
slug: microsoft-azure-blob-storage-finops
source_filename: microsoft-azure-blob-storage-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/storage/blobs/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Blob Storage\nproviderId: microsoft-azure-blob-storage\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Storage\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure Blob Storage: per-GB-month capacity by access tier, per-10,000-transaction\n  fees, retrieval and egress charges, with reserved-capacity commitments available.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/storage/blobs/\n  - https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Storage / Object Storage\nbillingModel:\n\
  \  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure Blob Storage\n  ServiceCategory: Storage\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: capacity_gb_month\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - access_tier\n      - redundancy\n      - region\n      - account\n  - name: write_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - access_tier\n      - region\n      - account\n  - name: read_transactions\n    unit: transaction\n    aggregation: sum\n    dimensions:\n      - access_tier\n      - region\n      - account\n  - name: data_retrieval\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - access_tier\n  \
  \    - region\n  - name: data_egress\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - region\n      - direction\n  - name: early_deletion\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - access_tier\nprinciples:\n  - name: Visibility\n    description: Use Azure Cost Management with grouping by Meter Subcategory (Hot/Cool/Cold/Archive)\n      and the Storage Account blob inventory report to attribute capacity and transactions per container.\n  - name: Allocation\n    description: Tag storage accounts and use container-level inventory reports keyed to tags or\n      naming conventions for chargeback to applications and teams.\n  - name: Optimization\n    description: Apply Lifecycle Management policies to tier blobs from Hot to Cool, Cold, then Archive;\n      use reserved capacity for stable footprints; consolidate redundancy (LRS vs GRS) to actual durability\n      need; avoid early-deletion charges by aligning retention to tier minimums.\n  - name: Accountability\n\
  \    description: Assign per-container cost owners; alert on capacity growth and transaction-rate\n      anomalies; review tier mix quarterly against access-pattern telemetry.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-blob-storage/refs/heads/main/finops/microsoft-azure-blob-storage-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/storage/blobs/
- https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Storage
- Microsoft Azure
---
