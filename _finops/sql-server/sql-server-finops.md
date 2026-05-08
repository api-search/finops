---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sql.json
  format: json
  label: SQL Server REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/sql/resource-manager/Microsoft.Sql/stable/2021-11-01/sql.json
- filename: databases.json
  format: json
  label: Azure SQL Database REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/sql/resource-manager/Microsoft.Sql/stable/2021-11-01/databases.json
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
description: FinOps framework definition for the Microsoft SQL Server APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft SQL Server APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft SQL Server APIs
  PublisherName: Microsoft SQL Server APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft SQL Server APIs
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
name: Sql Server Finops
provider_name: Microsoft SQL Server APIs
provider_slug: sql-server
publisher_name: Microsoft SQL Server APIs
service_category: API
slug: sql-server-finops
source_filename: sql-server-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft SQL Server APIs\nproviderId: sql-server\npublisherName: Microsoft SQL Server APIs\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Azure SQL\n  - Cloud Database\n  - Data Management\n  - Database\n  - Microsoft\n  - Relational Database\n  - SQL\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft SQL Server APIs API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n   \
  \   real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      -\
  \ Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft SQL Server APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft SQL Server APIs\n  PublisherName: Microsoft SQL Server APIs\n  InvoiceIssuerName: Microsoft SQL Server APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SQL Server Database Engine API\n    baseURL: ''\n    tags:\n      - Database Engine\n      - Query Execution\n      - T-SQL\n    serviceName: SQL Server Database Engine API\n    serviceCategory: API\n  - name: SQL Server REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud\n      - Management\n      - REST\n    serviceName: SQL Server REST API\n    serviceCategory: API\n  - name: SQL Server Management Objects (SMO)\n    baseURL: ''\n    tags:\n      - .NET\n      - Automation\n      - Management\n      -\
  \ SMO\n    serviceName: SQL Server Management Objects (SMO)\n    serviceCategory: API\n  - name: SQL Server Reporting Services (SSRS) API\n    baseURL: http://localhost/reports/api/v2.0\n    tags:\n      - Business Intelligence\n      - Reporting\n      - REST\n      - SSRS\n    serviceName: SQL Server Reporting Services (SSRS) API\n    serviceCategory: API\n  - name: ODBC Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Cross-Platform\n      - Driver\n      - ODBC\n    serviceName: ODBC Driver for SQL Server\n    serviceCategory: API\n  - name: JDBC Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - Java\n      - JDBC\n    serviceName: JDBC Driver for SQL Server\n    serviceCategory: API\n  - name: SQL Server Analysis Services (SSAS) API\n    baseURL: ''\n    tags:\n      - Analysis\n      - Business Intelligence\n      - OLAP\n      - SSAS\n    serviceName: SQL Server Analysis Services (SSAS) API\n    serviceCategory:\
  \ API\n  - name: Azure SQL Database REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud\n      - PaaS\n      - REST\n    serviceName: Azure SQL Database REST API\n    serviceCategory: API\n  - name: Azure SQL Managed Instance REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud\n      - Managed Instance\n      - PaaS\n      - REST\n    serviceName: Azure SQL Managed Instance REST API\n    serviceCategory: API\n  - name: SQL Server External REST Endpoint Invocation\n    baseURL: ''\n    tags:\n      - External Endpoints\n      - Integration\n      - REST\n      - SQL Server 2025\n      - T-SQL\n    serviceName: SQL Server External REST Endpoint Invocation\n    serviceCategory: API\n  - name: Data API Builder for SQL Server\n    baseURL: ''\n    tags:\n      - Azure\n      - Data API\n      - GraphQL\n      - Open Source\n      - REST\n    serviceName: Data API Builder for SQL Server\n    serviceCategory: API\n\
  \  - name: ADO.NET Provider for SQL Server (Microsoft.Data.SqlClient)\n    baseURL: ''\n    tags:\n      - .NET\n      - ADO.NET\n      - Connectivity\n      - Driver\n      - SqlClient\n    serviceName: ADO.NET Provider for SQL Server (Microsoft.Data.SqlClient)\n    serviceCategory: API\n  - name: OLE DB Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - OLE DB\n      - Windows\n    serviceName: OLE DB Driver for SQL Server\n    serviceCategory: API\n  - name: SQL Server Integration Services (SSIS) API\n    baseURL: ''\n    tags:\n      - Automation\n      - Data Integration\n      - ETL\n      - SSIS\n    serviceName: SQL Server Integration Services (SSIS) API\n    serviceCategory: API\n  - name: Node.js Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - JavaScript\n      - Node.js\n      - Npm\n    serviceName: Node.js Driver for SQL Server\n    serviceCategory: API\n  - name: Python Drivers\
  \ for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - Pymssql\n      - Pyodbc\n      - Python\n    serviceName: Python Drivers for SQL Server\n    serviceCategory: API\n  - name: Go Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - Go\n      - Golang\n    serviceName: Go Driver for SQL Server\n    serviceCategory: API\n  - name: PHP Drivers for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - PDO\n      - PHP\n      - SQLSRV\n    serviceName: PHP Drivers for SQL Server\n    serviceCategory: API\n  - name: Ruby Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Driver\n      - Ruby\n      - TinyTDS\n    serviceName: Ruby Driver for SQL Server\n    serviceCategory: API\n  - name: Entity Framework Core SQL Server Provider\n    baseURL: ''\n    tags:\n      - .NET\n      - Driver\n      - Entity Framework\n      - ORM\n    serviceName: Entity\
  \ Framework Core SQL Server Provider\n    serviceCategory: API\n  - name: SQL Server PowerShell Module\n    baseURL: ''\n    tags:\n      - Automation\n      - CLI\n      - Management\n      - PowerShell\n    serviceName: SQL Server PowerShell Module\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sql-server/refs/heads/main/finops/sql-server-finops.yml
sources: []
specification: FinOps Framework
tags:
- Azure SQL
- Cloud Database
- Data Management
- Database
- Microsoft
- Relational Database
- SQL
- FinOps
- Cost Management
- FOCUS
---
