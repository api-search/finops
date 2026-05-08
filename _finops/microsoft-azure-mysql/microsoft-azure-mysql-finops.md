---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-azure-mysql-openapi.yml
  format: yaml
  label: Azure Database for MySQL Flexible Servers API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-mysql/refs/heads/main/openapi/microsoft-azure-mysql-openapi.yml
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
description: FinOps framework definition for the Azure Database for MySQL API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Database for MySQL
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Database for MySQL
  PublisherName: Azure Database for MySQL
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Database for MySQL
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
name: Microsoft Azure Mysql Finops
provider_name: Azure Database for MySQL
provider_slug: microsoft-azure-mysql
publisher_name: Azure Database for MySQL
service_category: API
slug: microsoft-azure-mysql-finops
source_filename: microsoft-azure-mysql-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Database for MySQL\nproviderId: microsoft-azure-mysql\npublisherName: Azure Database for MySQL\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Database\n  - Flexible Server\n  - Managed Database\n  - MySQL\n  - Open Source\n  - Relational Database\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Database for MySQL API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n    \
  \  real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      -\
  \ Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Database for MySQL\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Database for MySQL\n  PublisherName: Azure Database for MySQL\n  InvoiceIssuerName: Azure Database for MySQL\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n  \
  \    - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Database for MySQL Flexible Servers API\n    baseURL: https://management.azure.com\n    tags:\n      - Flexible Server\n      - High Availability\n      - MySQL\n      - Server Management\n    serviceName: Azure Database for MySQL Flexible Servers API\n    serviceCategory: API\n  - name: Azure Database for MySQL Databases API\n    baseURL: https://management.azure.com\n    tags:\n      - Charset\n      - Collation\n      - Database\n      - MySQL\n    serviceName: Azure Database for MySQL Databases API\n    serviceCategory: API\n  - name:\
  \ Azure Database for MySQL Firewall Rules API\n    baseURL: https://management.azure.com\n    tags:\n      - Access Control\n      - Firewall Rules\n      - IP Allowlist\n      - Networking\n    serviceName: Azure Database for MySQL Firewall Rules API\n    serviceCategory: API\n  - name: Azure Database for MySQL Configurations API\n    baseURL: https://management.azure.com\n    tags:\n      - Configuration\n      - Parameters\n      - Server Settings\n      - Tuning\n    serviceName: Azure Database for MySQL Configurations API\n    serviceCategory: API\n  - name: Azure Database for MySQL Replicas API\n    baseURL: https://management.azure.com\n    tags:\n      - Read Replica\n      - Replication\n      - Scale-Out\n    serviceName: Azure Database for MySQL Replicas API\n    serviceCategory: API\n  - name: Azure Database for MySQL Backups API\n    baseURL: https://management.azure.com\n    tags:\n      - Backup\n      - Disaster Recovery\n      - Point-In-Time Restore\n      - Retention\n\
  \    serviceName: Azure Database for MySQL Backups API\n    serviceCategory: API\n  - name: Azure Database for MySQL Administrators API\n    baseURL: https://management.azure.com\n    tags:\n      - AAD\n      - Administrators\n      - Authentication\n      - Identity\n    serviceName: Azure Database for MySQL Administrators API\n    serviceCategory: API\n  - name: Azure Database for MySQL Check Name Availability API\n    baseURL: https://management.azure.com\n    tags:\n      - Availability\n      - Name Validation\n      - Provisioning\n    serviceName: Azure Database for MySQL Check Name Availability API\n    serviceCategory: API\n  - name: Azure Database for MySQL Operations API\n    baseURL: https://management.azure.com\n    tags:\n      - Operations\n      - Provider\n      - Resource Provider\n    serviceName: Azure Database for MySQL Operations API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target:\
  \ TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-mysql/refs/heads/main/finops/microsoft-azure-mysql-finops.yml
sources: []
specification: FinOps Framework
tags:
- Database
- Flexible Server
- Managed Database
- MySQL
- Open Source
- Relational Database
- FinOps
- Cost Management
- FOCUS
---
