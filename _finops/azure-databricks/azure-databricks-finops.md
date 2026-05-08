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
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Usage-Based
description: FinOps framework definition for the Azure Databricks API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Databricks
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Databricks
  PublisherName: Azure Databricks
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Databricks
layout: finops
meters:
- aggregation: sum
  description: Count of billable API requests
  dimensions:
  - api
  - endpoint
  - tier
  - region
  - consumer
  name: api_requests
  unit: request
- aggregation: sum
  description: Bytes returned over the network in API responses
  dimensions:
  - api
  - region
  - consumer
  name: data_egress
  unit: GB
- aggregation: sum
  description: Server-side compute consumed by the request, where applicable
  dimensions:
  - api
  - endpoint
  - tier
  name: compute_seconds
  unit: second
name: Azure Databricks Finops
provider_name: Azure Databricks
provider_slug: azure-databricks
publisher_name: Azure Databricks
service_category: API
slug: azure-databricks-finops
source_filename: azure-databricks-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Databricks\nproviderId: azure-databricks\npublisherName: Azure Databricks\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Apache Spark\n  - Big Data\n  - Data Engineering\n  - Machine Learning\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Databricks API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Databricks\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Databricks\n  PublisherName: Azure Databricks\n  InvoiceIssuerName: Azure Databricks\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Databricks REST API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api\n    tags:\n      - Clusters\n      - Jobs\n      - Notebooks\n      - Workspace\n    serviceName: Azure Databricks REST API\n    serviceCategory: API\n  - name: Clusters API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/clusters\n    tags:\n      - Clusters\n      - Compute\n    serviceName: Clusters API\n    serviceCategory: API\n  - name: Jobs API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/jobs\n    tags:\n      - Automation\n      - Jobs\n      - Scheduling\n    serviceName: Jobs API\n\
  \    serviceCategory: API\n  - name: Workspace API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/workspace\n    tags:\n      - Folders\n      - Notebooks\n      - Workspace\n    serviceName: Workspace API\n    serviceCategory: API\n  - name: DBFS API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/dbfs\n    tags:\n      - Files\n      - Storage\n    serviceName: DBFS API\n    serviceCategory: API\n  - name: Libraries API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/libraries\n    tags:\n      - Dependencies\n      - Libraries\n    serviceName: Libraries API\n    serviceCategory: API\n  - name: Secrets API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/secrets\n    tags:\n      - Credentials\n      - Secrets\n      - Security\n    serviceName: Secrets API\n    serviceCategory: API\n  - name: Token Management API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/token\n\
  \    tags:\n      - Authentication\n      - Security\n      - Tokens\n    serviceName: Token Management API\n    serviceCategory: API\n  - name: SQL Analytics API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/sql\n    tags:\n      - Analytics\n      - Queries\n      - Sql\n      - Warehouses\n    serviceName: SQL Analytics API\n    serviceCategory: API\n  - name: MLflow API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/mlflow\n    tags:\n      - Experiments\n      - Machine Learning\n      - Mlops\n      - Model Tracking\n    serviceName: MLflow API\n    serviceCategory: API\n  - name: Instance Pools API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/instance-pools\n    tags:\n      - Clusters\n      - Compute\n      - Instance Pools\n    serviceName: Instance Pools API\n    serviceCategory: API\n  - name: Cluster Policies API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/policies/clusters\n\
  \    tags:\n      - Clusters\n      - Governance\n      - Policies\n    serviceName: Cluster Policies API\n    serviceCategory: API\n  - name: Repos API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/repos\n    tags:\n      - Git\n      - Repositories\n      - Version Control\n    serviceName: Repos API\n    serviceCategory: API\n  - name: Git Credentials API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/git-credentials\n    tags:\n      - Authentication\n      - Credentials\n      - Git\n    serviceName: Git Credentials API\n    serviceCategory: API\n  - name: Pipelines API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/pipelines\n    tags:\n      - Data Engineering\n      - Delta Live Tables\n      - ETL\n      - Pipelines\n    serviceName: Pipelines API\n    serviceCategory: API\n  - name: Permissions API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/permissions\n    tags:\n      -\
  \ Access Control\n      - Permissions\n      - Security\n    serviceName: Permissions API\n    serviceCategory: API\n  - name: Unity Catalog - Catalogs API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/catalogs\n    tags:\n      - Catalogs\n      - Data Governance\n      - Unity Catalog\n    serviceName: Unity Catalog - Catalogs API\n    serviceCategory: API\n  - name: Unity Catalog - Schemas API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/schemas\n    tags:\n      - Data Governance\n      - Schemas\n      - Unity Catalog\n    serviceName: Unity Catalog - Schemas API\n    serviceCategory: API\n  - name: Unity Catalog - Tables API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/tables\n    tags:\n      - Data Governance\n      - Tables\n      - Unity Catalog\n    serviceName: Unity Catalog - Tables API\n    serviceCategory: API\n  - name: Unity Catalog - Volumes API\n\
  \    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/volumes\n    tags:\n      - Storage\n      - Unity Catalog\n      - Volumes\n    serviceName: Unity Catalog - Volumes API\n    serviceCategory: API\n  - name: Unity Catalog - Grants API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/permissions\n    tags:\n      - Data Governance\n      - Permissions\n      - Unity Catalog\n    serviceName: Unity Catalog - Grants API\n    serviceCategory: API\n  - name: Unity Catalog - External Locations API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/external-locations\n    tags:\n      - External Locations\n      - Storage\n      - Unity Catalog\n    serviceName: Unity Catalog - External Locations API\n    serviceCategory: API\n  - name: Unity Catalog - Storage Credentials API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/storage-credentials\n   \
  \ tags:\n      - Credentials\n      - Security\n      - Storage\n      - Unity Catalog\n    serviceName: Unity Catalog - Storage Credentials API\n    serviceCategory: API\n  - name: Unity Catalog - Metastores API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/metastores\n    tags:\n      - Data Governance\n      - Metastores\n      - Unity Catalog\n    serviceName: Unity Catalog - Metastores API\n    serviceCategory: API\n  - name: Model Serving Endpoints API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/serving-endpoints\n    tags:\n      - Deployment\n      - Inference\n      - Machine Learning\n      - Model Serving\n    serviceName: Model Serving Endpoints API\n    serviceCategory: API\n  - name: Model Registry API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/mlflow/databricks\n    tags:\n      - Machine Learning\n      - Mlops\n      - Model Registry\n    serviceName: Model Registry API\n \
  \   serviceCategory: API\n  - name: Registered Models API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.1/unity-catalog/models\n    tags:\n      - Machine Learning\n      - Model Registry\n      - Unity Catalog\n    serviceName: Registered Models API\n    serviceCategory: API\n  - name: Global Init Scripts API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/global-init-scripts\n    tags:\n      - Administration\n      - Clusters\n      - Initialization\n    serviceName: Global Init Scripts API\n    serviceCategory: API\n  - name: IP Access Lists API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/ip-access-lists\n    tags:\n      - Access Control\n      - Networking\n      - Security\n    serviceName: IP Access Lists API\n    serviceCategory: API\n  - name: Statement Execution API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/sql/statements\n    tags:\n      - Query Execution\n      - Sql\n\
  \      - Warehouses\n    serviceName: Statement Execution API\n    serviceCategory: API\n  - name: Command Execution API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/1.2\n    tags:\n      - Clusters\n      - Commands\n      - Execution\n    serviceName: Command Execution API\n    serviceCategory: API\n  - name: Files API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/fs/files\n    tags:\n      - Files\n      - Storage\n      - Unity Catalog\n    serviceName: Files API\n    serviceCategory: API\n  - name: Apps API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/apps\n    tags:\n      - Applications\n      - Deployment\n    serviceName: Apps API\n    serviceCategory: API\n  - name: Lakeview API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/lakeview\n    tags:\n      - Dashboards\n      - Lakeview\n      - Visualization\n    serviceName: Lakeview API\n    serviceCategory: API\n  - name: Online\
  \ Tables API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/online-tables\n    tags:\n      - Feature Serving\n      - Machine Learning\n      - Online Tables\n    serviceName: Online Tables API\n    serviceCategory: API\n  - name: Vector Search Indexes API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/vector-search/indexes\n    tags:\n      - AI\n      - RAG\n      - Similarity Search\n      - Vector Search\n    serviceName: Vector Search Indexes API\n    serviceCategory: API\n  - name: Vector Search Endpoints API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/vector-search/endpoints\n    tags:\n      - AI\n      - Endpoints\n      - Vector Search\n    serviceName: Vector Search Endpoints API\n    serviceCategory: API\n  - name: Query History API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/sql/history/queries\n    tags:\n      - Monitoring\n      - Query History\n      - Sql\n    serviceName:\
  \ Query History API\n    serviceCategory: API\n  - name: Account SCIM API\n    baseURL: https://<databricks-instance>.azuredatabricks.net/api/2.0/account/scim/v2\n    tags:\n      - Groups\n      - Identity Management\n      - SCIM\n      - Users\n    serviceName: Account SCIM API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/azure-databricks/refs/heads/main/finops/azure-databricks-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Apache Spark
- Big Data
- Data Engineering
- Machine Learning
- FinOps
- Cost Management
- FOCUS
---
