---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: databricks-openapi.yml
  format: yaml
  label: Databricks Clusters API
  slug: clusters-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
- filename: databricks-openapi.yml
  format: yaml
  label: Databricks Jobs API
  slug: jobs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
- filename: databricks-openapi.yml
  format: yaml
  label: Databricks Workspace API
  slug: workspace-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/openapi/databricks-openapi.yml
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
description: FinOps framework definition for the Databricks API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Databricks
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Databricks
  PublisherName: Databricks
  ServiceCategory: Developer Tools / API
  ServiceName: Databricks
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
name: Databricks Finops
provider_name: Databricks
provider_slug: databricks
publisher_name: Databricks
service_category: API
slug: databricks-finops
source_filename: databricks-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Databricks\nproviderId: databricks\npublisherName: Databricks\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Analytics\n  - Apache Spark\n  - Big Data\n  - Clean Rooms\n  - Cloud Computing\n  - Data\n  - Data Analytics\n  - Data Engineering\n  - Data Governance\n  - Delta Lake\n  - Delta Sharing\n  - ETL\n  - Identity Management\n  - Lakehouse\n  - Machine Learning\n  - MLflow\n  - Model Serving\n  - Security\n  - SQL\n  - Unity Catalog\n  - Vector Search\n  - Visualize\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Databricks API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage\
  \ measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n\
  \      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Databricks\n  ServiceCategory: Developer Tools / API\n  ProviderName: Databricks\n  PublisherName: Databricks\n  InvoiceIssuerName: Databricks\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description:\
  \ Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Databricks\n    baseURL: ''\n    tags:\n      - Analytics\n      - Data\n      - Visualize\n    serviceName: Databricks\n    serviceCategory: API\n  - name: Databricks Clusters API\n    baseURL: ''\n    tags:\n      - Clusters\n      - Compute\n      - Infrastructure\n    serviceName: Databricks Clusters API\n    serviceCategory: API\n  - name: Databricks Jobs API\n    baseURL: ''\n    tags:\n      - Jobs\n  \
  \    - Orchestration\n      - Scheduling\n      - Workflows\n    serviceName: Databricks Jobs API\n    serviceCategory: API\n  - name: Databricks DBFS API\n    baseURL: ''\n    tags:\n      - Data\n      - Files\n      - Storage\n    serviceName: Databricks DBFS API\n    serviceCategory: API\n  - name: Databricks Workspace API\n    baseURL: ''\n    tags:\n      - Folders\n      - Notebooks\n      - Workspace\n    serviceName: Databricks Workspace API\n    serviceCategory: API\n  - name: Databricks SQL Warehouses API\n    baseURL: ''\n    tags:\n      - Analytics\n      - SQL\n      - Warehouses\n    serviceName: Databricks SQL Warehouses API\n    serviceCategory: API\n  - name: Databricks Pipelines API\n    baseURL: ''\n    tags:\n      - Delta Live Tables\n      - ETL\n      - Pipelines\n    serviceName: Databricks Pipelines API\n    serviceCategory: API\n  - name: Databricks Serving Endpoints API\n    baseURL: ''\n    tags:\n      - AI\n      - Machine Learning\n      - Model Serving\n\
  \    serviceName: Databricks Serving Endpoints API\n    serviceCategory: API\n  - name: Databricks Secrets API\n    baseURL: ''\n    tags:\n      - Credentials\n      - Secrets\n      - Security\n    serviceName: Databricks Secrets API\n    serviceCategory: API\n  - name: Databricks Instance Pools API\n    baseURL: ''\n    tags:\n      - Clusters\n      - Compute\n      - Infrastructure\n    serviceName: Databricks Instance Pools API\n    serviceCategory: API\n  - name: Databricks Token Management API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Security\n      - Tokens\n    serviceName: Databricks Token Management API\n    serviceCategory: API\n  - name: Databricks Catalogs API\n    baseURL: ''\n    tags:\n      - Data Governance\n      - Metadata\n      - Unity Catalog\n    serviceName: Databricks Catalogs API\n    serviceCategory: API\n  - name: Databricks Vector Search Indexes API\n    baseURL: ''\n    tags:\n      - AI\n      - Embeddings\n      - Vector Search\n \
  \   serviceName: Databricks Vector Search Indexes API\n    serviceCategory: API\n  - name: Databricks Model Versions API\n    baseURL: ''\n    tags:\n      - Machine Learning\n      - MLflow\n      - Model Registry\n    serviceName: Databricks Model Versions API\n    serviceCategory: API\n  - name: Databricks Permissions API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Authorization\n      - Security\n    serviceName: Databricks Permissions API\n    serviceCategory: API\n  - name: Databricks Repos API\n    baseURL: ''\n    tags:\n      - Git\n      - Repositories\n      - Version Control\n    serviceName: Databricks Repos API\n    serviceCategory: API\n  - name: Databricks Git Credentials API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Credentials\n      - Git\n    serviceName: Databricks Git Credentials API\n    serviceCategory: API\n  - name: Databricks Cluster Policies API\n    baseURL: ''\n    tags:\n      - Clusters\n      - Governance\n      - Policies\n\
  \    serviceName: Databricks Cluster Policies API\n    serviceCategory: API\n  - name: Databricks Libraries API\n    baseURL: ''\n    tags:\n      - Clusters\n      - Dependencies\n      - Libraries\n    serviceName: Databricks Libraries API\n    serviceCategory: API\n  - name: Databricks Global Init Scripts API\n    baseURL: ''\n    tags:\n      - Administration\n      - Compute\n      - Configuration\n    serviceName: Databricks Global Init Scripts API\n    serviceCategory: API\n  - name: Databricks Command Execution API\n    baseURL: ''\n    tags:\n      - Commands\n      - Compute\n      - Execution\n    serviceName: Databricks Command Execution API\n    serviceCategory: API\n  - name: Databricks Statement Execution API\n    baseURL: ''\n    tags:\n      - Queries\n      - SQL\n      - Warehouses\n    serviceName: Databricks Statement Execution API\n    serviceCategory: API\n  - name: Databricks Queries API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Queries\n      - SQL\n\
  \    serviceName: Databricks Queries API\n    serviceCategory: API\n  - name: Databricks Alerts API\n    baseURL: ''\n    tags:\n      - Alerts\n      - Monitoring\n      - SQL\n    serviceName: Databricks Alerts API\n    serviceCategory: API\n  - name: Databricks Schemas API\n    baseURL: ''\n    tags:\n      - Data Governance\n      - Schemas\n      - Unity Catalog\n    serviceName: Databricks Schemas API\n    serviceCategory: API\n  - name: Databricks Tables API\n    baseURL: ''\n    tags:\n      - Data Governance\n      - Tables\n      - Unity Catalog\n    serviceName: Databricks Tables API\n    serviceCategory: API\n  - name: Databricks Volumes API\n    baseURL: ''\n    tags:\n      - Storage\n      - Unity Catalog\n      - Volumes\n    serviceName: Databricks Volumes API\n    serviceCategory: API\n  - name: Databricks Functions API\n    baseURL: ''\n    tags:\n      - Functions\n      - SQL\n      - Unity Catalog\n    serviceName: Databricks Functions API\n    serviceCategory: API\n\
  \  - name: Databricks Grants API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Security\n      - Unity Catalog\n    serviceName: Databricks Grants API\n    serviceCategory: API\n  - name: Databricks External Locations API\n    baseURL: ''\n    tags:\n      - Cloud Storage\n      - Storage\n      - Unity Catalog\n    serviceName: Databricks External Locations API\n    serviceCategory: API\n  - name: Databricks Storage Credentials API\n    baseURL: ''\n    tags:\n      - Cloud Storage\n      - Security\n      - Unity Catalog\n    serviceName: Databricks Storage Credentials API\n    serviceCategory: API\n  - name: Databricks Metastores API\n    baseURL: ''\n    tags:\n      - Data Governance\n      - Metadata\n      - Unity Catalog\n    serviceName: Databricks Metastores API\n    serviceCategory: API\n  - name: Databricks Connections API\n    baseURL: ''\n    tags:\n      - Connections\n      - External Data\n      - Unity Catalog\n    serviceName: Databricks Connections API\n\
  \    serviceCategory: API\n  - name: Databricks Registered Models API\n    baseURL: ''\n    tags:\n      - Machine Learning\n      - MLflow\n      - Model Registry\n    serviceName: Databricks Registered Models API\n    serviceCategory: API\n  - name: Databricks Experiments API\n    baseURL: ''\n    tags:\n      - Experiments\n      - Machine Learning\n      - MLflow\n    serviceName: Databricks Experiments API\n    serviceCategory: API\n  - name: Databricks Online Tables API\n    baseURL: ''\n    tags:\n      - Feature Serving\n      - Real-Time\n      - Tables\n    serviceName: Databricks Online Tables API\n    serviceCategory: API\n  - name: Databricks Quality Monitors API\n    baseURL: ''\n    tags:\n      - Data Quality\n      - Monitoring\n      - Observability\n    serviceName: Databricks Quality Monitors API\n    serviceCategory: API\n  - name: Databricks Vector Search Endpoints API\n    baseURL: ''\n    tags:\n      - AI\n      - Compute\n      - Vector Search\n    serviceName:\
  \ Databricks Vector Search Endpoints API\n    serviceCategory: API\n  - name: Databricks Shares API\n    baseURL: ''\n    tags:\n      - Collaboration\n      - Data Sharing\n      - Delta Sharing\n    serviceName: Databricks Shares API\n    serviceCategory: API\n  - name: Databricks Recipients API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Data Sharing\n      - Delta Sharing\n    serviceName: Databricks Recipients API\n    serviceCategory: API\n  - name: Databricks Providers API\n    baseURL: ''\n    tags:\n      - Data Sharing\n      - Delta Sharing\n      - Marketplace\n    serviceName: Databricks Providers API\n    serviceCategory: API\n  - name: Databricks Clean Rooms API\n    baseURL: ''\n    tags:\n      - Clean Rooms\n      - Collaboration\n      - Privacy\n    serviceName: Databricks Clean Rooms API\n    serviceCategory: API\n  - name: Databricks Notification Destinations API\n    baseURL: ''\n    tags:\n      - Alerts\n      - Integration\n      - Notifications\n\
  \    serviceName: Databricks Notification Destinations API\n    serviceCategory: API\n  - name: Databricks Apps API\n    baseURL: ''\n    tags:\n      - Applications\n      - Deployment\n      - Development\n    serviceName: Databricks Apps API\n    serviceCategory: API\n  - name: Databricks Lakeview API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Dashboards\n      - Visualization\n    serviceName: Databricks Lakeview API\n    serviceCategory: API\n  - name: Databricks Files API\n    baseURL: ''\n    tags:\n      - Files\n      - Storage\n      - Unity Catalog\n    serviceName: Databricks Files API\n    serviceCategory: API\n  - name: Databricks Tokens API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Security\n      - Tokens\n    serviceName: Databricks Tokens API\n    serviceCategory: API\n  - name: Databricks IP Access Lists API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Networking\n      - Security\n    serviceName: Databricks IP Access\
  \ Lists API\n    serviceCategory: API\n  - name: Databricks Current User API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Identity\n      - Users\n    serviceName: Databricks Current User API\n    serviceCategory: API\n  - name: Databricks Groups API\n    baseURL: ''\n    tags:\n      - Access Control\n      - Groups\n      - Identity\n    serviceName: Databricks Groups API\n    serviceCategory: API\n  - name: Databricks Service Principals API\n    baseURL: ''\n    tags:\n      - Automation\n      - Identity\n      - Service Principals\n    serviceName: Databricks Service Principals API\n    serviceCategory: API\n  - name: Databricks Users API\n    baseURL: ''\n    tags:\n      - Administration\n      - Identity\n      - Users\n    serviceName: Databricks Users API\n    serviceCategory: API\n  - name: Databricks Dashboards API\n    baseURL: ''\n    tags:\n      - Dashboards\n      - SQL\n      - Visualization\n    serviceName: Databricks Dashboards API\n    serviceCategory:\
  \ API\n  - name: Databricks Model Registry API\n    baseURL: ''\n    tags:\n      - Machine Learning\n      - MLflow\n      - Model Registry\n    serviceName: Databricks Model Registry API\n    serviceCategory: API\n  - name: Databricks Workspace Bindings API\n    baseURL: ''\n    tags:\n      - Governance\n      - Unity Catalog\n      - Workspace\n    serviceName: Databricks Workspace Bindings API\n    serviceCategory: API\n  - name: Databricks System Schemas API\n    baseURL: ''\n    tags:\n      - Monitoring\n      - System Tables\n      - Unity Catalog\n    serviceName: Databricks System Schemas API\n    serviceCategory: API\n  - name: Databricks Table Constraints API\n    baseURL: ''\n    tags:\n      - Data Quality\n      - Tables\n      - Unity Catalog\n    serviceName: Databricks Table Constraints API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n \
  \   metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - name: Databricks\n    email: support@databricks.com\n    url: https://www.databricks.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/databricks/refs/heads/main/finops/databricks-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Analytics
- Apache Spark
- Big Data
- Clean Rooms
- Cloud Computing
- Data
- Data Analytics
- Data Engineering
- Data Governance
- Delta Lake
- Delta Sharing
- ETL
- Identity Management
- Lakehouse
- Machine Learning
- MLflow
- Model Serving
- Security
- SQL
- Unity Catalog
- Vector Search
- Visualize
- FinOps
- Cost Management
- FOCUS
---
