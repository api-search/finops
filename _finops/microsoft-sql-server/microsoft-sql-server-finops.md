---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: SQL Server Database Engine API
  slug: sql-server-database-engine-api
  spec_type: OpenAPI
  url: https://docs.microsoft.com/sql/connect/
- filename: sql
  format: yaml
  label: Azure SQL Database REST API
  slug: azure-sql-database-rest-api
  spec_type: OpenAPI
  url: https://github.com/Azure/azure-rest-api-specs/tree/main/specification/sql
- filename: '2.0'
  format: yaml
  label: SQL Server Reporting Services (SSRS) API
  slug: sql-server-reporting-services-ssrs-api
  spec_type: OpenAPI
  url: https://app.swaggerhub.com/apis/microsoft-rs/SSRS/2.0
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
description: FinOps framework definition for the Microsoft SQL Server API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft SQL Server
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft SQL Server
  PublisherName: Microsoft SQL Server
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft SQL Server
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
name: Microsoft Sql Server Finops
provider_name: Microsoft SQL Server
provider_slug: microsoft-sql-server
publisher_name: Microsoft SQL Server
service_category: API
slug: microsoft-sql-server-finops
source_filename: microsoft-sql-server-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft SQL Server\nproviderId: microsoft-sql-server\npublisherName: Microsoft SQL Server\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Cloud\n  - Data Management\n  - Database\n  - Enterprise\n  - Relational Database\n  - SQL\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft SQL Server API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft SQL Server\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft SQL Server\n  PublisherName: Microsoft SQL Server\n  InvoiceIssuerName: Microsoft SQL Server\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SQL Server Database Engine API\n    baseURL: https://your-server.database.windows.net\n    tags:\n      - Database\n      - Query\n      - Transact-SQL\n    serviceName: SQL Server Database Engine API\n    serviceCategory: API\n  - name: SQL Server Management Objects (SMO) API\n    baseURL: https://api.example.com/smo\n    tags:\n      - .NET\n      - Administration\n      - Management\n    serviceName: SQL Server Management Objects (SMO) API\n    serviceCategory: API\n  - name: Azure SQL Database REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud\n      - Database\
  \ Management\n      - REST API\n    serviceName: Azure SQL Database REST API\n    serviceCategory: API\n  - name: SQL Server Reporting Services (SSRS) API\n    baseURL: https://your-server/reports/api/v2.0\n    tags:\n      - Business Intelligence\n      - Reporting\n      - REST API\n    serviceName: SQL Server Reporting Services (SSRS) API\n    serviceCategory: API\n  - name: SQL Server Integration Services (SSIS) Catalog API\n    baseURL: https://your-server/SSISDB\n    tags:\n      - Data Pipeline\n      - ETL\n      - Integration\n    serviceName: SQL Server Integration Services (SSIS) Catalog API\n    serviceCategory: API\n  - name: Azure SQL Managed Instance REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Azure\n      - Cloud\n      - Database Management\n      - Managed Instance\n      - REST API\n    serviceName: Azure SQL Managed Instance REST API\n    serviceCategory: API\n  - name: Data API Builder\n    baseURL: https://localhost:5000/api\n    tags:\n\
  \      - CRUD\n      - Data Access\n      - GraphQL\n      - Open Source\n      - REST API\n    serviceName: Data API Builder\n    serviceCategory: API\n  - name: Azure Analysis Services REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Analysis Services\n      - Azure\n      - Business Intelligence\n      - REST API\n      - Tabular Models\n    serviceName: Azure Analysis Services REST API\n    serviceCategory: API\n  - name: Microsoft SqlClient Data Provider (ADO.NET)\n    baseURL: ''\n    tags:\n      - .NET\n      - ADO.NET\n      - Data Provider\n      - SqlClient\n    serviceName: Microsoft SqlClient Data Provider (ADO.NET)\n    serviceCategory: API\n  - name: Microsoft JDBC Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Cross-Platform\n      - Driver\n      - Java\n      - JDBC\n    serviceName: Microsoft JDBC Driver for SQL Server\n    serviceCategory: API\n  - name: Microsoft ODBC Driver for SQL Server\n    baseURL: ''\n    tags:\n      - Cross-Platform\n\
  \      - Driver\n      - Native Code\n      - ODBC\n    serviceName: Microsoft ODBC Driver for SQL Server\n    serviceCategory: API\n  - name: Microsoft OLE DB Driver for SQL Server\n    baseURL: ''\n    tags:\n      - COM\n      - Driver\n      - OLE DB\n      - Windows\n    serviceName: Microsoft OLE DB Driver for SQL Server\n    serviceCategory: API\n  - name: Microsoft Python Driver for SQL Server (mssql-python)\n    baseURL: ''\n    tags:\n      - Cross-Platform\n      - DB-API\n      - Driver\n      - Python\n    serviceName: Microsoft Python Driver for SQL Server (mssql-python)\n    serviceCategory: API\n  - name: Node.js Driver for SQL Server (tedious)\n    baseURL: ''\n    tags:\n      - Cross-Platform\n      - Driver\n      - JavaScript\n      - Node.js\n      - TDS\n    serviceName: Node.js Driver for SQL Server (tedious)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost\
  \ per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-sql-server/refs/heads/main/finops/microsoft-sql-server-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- Data Management
- Database
- Enterprise
- Relational Database
- SQL
- FinOps
- Cost Management
- FOCUS
---
