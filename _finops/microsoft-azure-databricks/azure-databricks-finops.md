---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Azure Databricks REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Clusters API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Jobs API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Workspace API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Usage
  - Purchase
  - Tax
  - Adjustment
  pricingCategory: Pay-As-You-Go + Committed Use
description: 'FOCUS-aligned FinOps for Azure Databricks: dual-meter pricing where DBUs (Databricks Units) are billed by Databricks via Azure Marketplace and the underlying Azure VM, storage, and network are billed by Azure. Reserved DBUs (DBCU) and Azure Reservations stack for committed-use savings.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  PricingCategory: Pay-As-You-Go
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Data Analytics
  ServiceName: Azure Databricks
layout: finops
meters:
- aggregation: sum
  description: Databricks Unit consumption (per second) by workload type
  dimensions:
  - workload_type
  - tier
  - region
  - workspace
  - photon
  name: dbu_consumption
  unit: DBU
- aggregation: sum
  description: Underlying Azure VM time (billed separately by Azure)
  dimensions:
  - vm_sku
  - region
  - workspace
  name: vm_compute_hours
  unit: instance-hour
- aggregation: sum
  description: Serverless SQL / Model Serving / Jobs compute charged as DBUs without separate VM line
  dimensions:
  - service
  - region
  name: serverless_compute
  unit: DBU
- aggregation: avg
  description: Underlying ADLS Gen2 / managed storage
  dimensions:
  - region
  name: storage_capacity
  unit: GB-month
- aggregation: sum
  description: Inference queries against Model Serving endpoints
  dimensions:
  - endpoint
  name: model_serving_queries
  unit: query
- aggregation: sum
  description: Vector Search endpoint storage and throughput units
  name: vector_search_capacity
  unit: endpoint-hour
name: Azure Databricks Finops
provider_name: Azure Databricks
provider_slug: microsoft-azure-databricks
publisher_name: Microsoft Corporation
service_category: Data Analytics
slug: azure-databricks-finops
source_filename: azure-databricks-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/databricks/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Databricks\nproviderId: azure-databricks\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - Analytics\n  - Lakehouse\n  - Spark\n  - FinOps\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps for Azure Databricks: dual-meter pricing where DBUs (Databricks Units)\n  are billed by Databricks via Azure Marketplace and the underlying Azure VM, storage, and network are\n  billed by Azure. Reserved DBUs (DBCU) and Azure Reservations stack for committed-use savings.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/databricks/\n  - https://learn.microsoft.com/en-us/azure/databricks/admin/account-settings/usage\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\n\
  publisherName: Microsoft Corporation\nserviceCategory: Data Analytics\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\nfocusColumns:\n  ServiceName: Azure Databricks\n  ServiceCategory: Data Analytics\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  PricingCategory: Pay-As-You-Go\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: dbu_consumption\n    description: Databricks Unit consumption (per second) by workload type\n    unit: DBU\n    aggregation: sum\n    dimensions:\n      - workload_type\n      - tier\n      - region\n      - workspace\n      - photon\n  - name: vm_compute_hours\n    description: Underlying Azure VM time (billed separately by Azure)\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - vm_sku\n      - region\n    \
  \  - workspace\n  - name: serverless_compute\n    description: Serverless SQL / Model Serving / Jobs compute charged as DBUs without separate VM line\n    unit: DBU\n    aggregation: sum\n    dimensions:\n      - service\n      - region\n  - name: storage_capacity\n    description: Underlying ADLS Gen2 / managed storage\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - region\n  - name: model_serving_queries\n    description: Inference queries against Model Serving endpoints\n    unit: query\n    aggregation: sum\n    dimensions:\n      - endpoint\n  - name: vector_search_capacity\n    description: Vector Search endpoint storage and throughput units\n    unit: endpoint-hour\n    aggregation: sum\nprinciples:\n  - name: Visibility\n    description: Use the Azure Databricks usage page (system tables) and Azure Cost Management to view\n      DBU consumption by workspace, cluster, job, and tag; integrate with FOCUS exports.\n  - name: Allocation\n    description: Apply cluster\
  \ tags and pool tags propagated to Azure VM cost; cross-reference with system.billing.usage\n      for chargeback by job, user, or workspace.\n  - name: Optimization\n    description: Use Photon for SQL/ETL; choose Jobs Compute over All-Purpose for production workloads;\n      enable autoscaling and auto-termination; right-size VM SKUs; commit DBCUs and Azure Reservations\n      for predictable usage.\n  - name: Accountability\n    description: Set workspace-level budgets in Azure Cost Management; assign workspace admins as owners;\n      review high-cost queries and idle clusters in monthly FinOps reviews.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-databricks/refs/heads/main/finops/azure-databricks-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/databricks/
- https://learn.microsoft.com/en-us/azure/databricks/admin/account-settings/usage
specification: FinOps Framework
tags:
- Analytics
- Lakehouse
- Spark
- FinOps
- FOCUS
---
