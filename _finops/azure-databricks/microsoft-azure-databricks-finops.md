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
  url: https://raw.githubusercontent.com/api-evangelist/azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Clusters API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Jobs API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
- filename: azure-databricks-openapi.yml
  format: yaml
  label: Workspace API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/azure-databricks/refs/heads/main/openapi/azure-databricks-openapi.yml
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
description: 'FOCUS-aligned FinOps for Azure Databricks: per-DBU consumption metered by workload type (Jobs, All-Purpose, SQL Serverless, Model Serving) on top of Azure VM and storage cost, with optional 1- or 3-year DBCU pre-purchase commitments.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Analytics
  ServiceName: Azure Databricks
layout: finops
meters:
- aggregation: sum
  dimensions:
  - workspace
  - cluster
  - sku
  - region
  name: jobs_dbu
  unit: DBU
- aggregation: sum
  dimensions:
  - workspace
  - cluster
  - sku
  - region
  name: all_purpose_dbu
  unit: DBU
- aggregation: sum
  dimensions:
  - workspace
  - warehouse
  - region
  name: sql_serverless_dbu
  unit: DBU
- aggregation: sum
  dimensions:
  - workspace
  - endpoint
  name: model_serving_dbu
  unit: DBU
- aggregation: sum
  dimensions:
  - workspace
  - vm_sku
  - region
  name: vm_compute_hours
  unit: instance-hour
- aggregation: avg
  dimensions:
  - workspace
  name: managed_storage
  unit: GB-month
name: Microsoft Azure Databricks Finops
provider_name: Azure Databricks
provider_slug: azure-databricks
publisher_name: Microsoft Corporation
service_category: Analytics / Data + AI Platform
slug: microsoft-azure-databricks-finops
source_filename: microsoft-azure-databricks-finops.yml
source_heading: FinOps Profile
source_url: https://azure.microsoft.com/en-us/pricing/details/databricks/
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Azure Databricks\nproviderId: microsoft-azure-databricks\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Analytics\n  - Microsoft Azure\ndescription: 'FOCUS-aligned FinOps for Azure Databricks: per-DBU consumption metered by workload type\n  (Jobs, All-Purpose, SQL Serverless, Model Serving) on top of Azure VM and storage cost, with optional\n  1- or 3-year DBCU pre-purchase commitments.'\nsources:\n  - https://azure.microsoft.com/en-us/pricing/details/databricks/\n  - https://learn.microsoft.com/en-us/azure/databricks/admin/account-settings/usage\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory:\
  \ Analytics / Data + AI Platform\nbillingModel:\n  pricingCategory: Pay-As-You-Go + Committed Use\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Azure Databricks\n  ServiceCategory: Analytics\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: jobs_dbu\n    unit: DBU\n    aggregation: sum\n    dimensions:\n      - workspace\n      - cluster\n      - sku\n      - region\n  - name: all_purpose_dbu\n    unit: DBU\n    aggregation: sum\n    dimensions:\n      - workspace\n      - cluster\n      - sku\n      - region\n  - name: sql_serverless_dbu\n    unit: DBU\n    aggregation: sum\n    dimensions:\n      - workspace\n      - warehouse\n      - region\n  - name: model_serving_dbu\n    unit: DBU\n    aggregation: sum\n    dimensions:\n \
  \     - workspace\n      - endpoint\n  - name: vm_compute_hours\n    unit: instance-hour\n    aggregation: sum\n    dimensions:\n      - workspace\n      - vm_sku\n      - region\n  - name: managed_storage\n    unit: GB-month\n    aggregation: avg\n    dimensions:\n      - workspace\nprinciples:\n  - name: Visibility\n    description: Use the Databricks Usage UI / system tables (system.billing.usage) and Azure Cost\n      Management to correlate DBUs with VM and storage line items per workspace and cluster.\n  - name: Allocation\n    description: Tag clusters and SQL warehouses with cost-center and project tags that propagate\n      to billing usage records; use Unity Catalog for per-team workspace and catalog scoping.\n  - name: Optimization\n    description: Move scheduled work from All-Purpose to Jobs Compute; right-size cluster autoscaling;\n      use Photon and serverless where break-even; pre-purchase DBCUs for steady baseline; auto-terminate\n      idle clusters.\n  - name: Accountability\n\
  \    description: Assign workspace owners as cost owners; alert on DBU burn rate vs commitment; review\n      Standard-to-Premium migration timing before October 1, 2026 retirement.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-databricks/refs/heads/main/finops/microsoft-azure-databricks-finops.yml
sources:
- https://azure.microsoft.com/en-us/pricing/details/databricks/
- https://learn.microsoft.com/en-us/azure/databricks/admin/account-settings/usage
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Analytics
- Microsoft Azure
---
