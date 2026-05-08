---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-azure-migrate-openapi.yml
  format: yaml
  label: Azure Migrate Projects API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-migrate/refs/heads/main/openapi/microsoft-azure-migrate-openapi.yml
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
description: FinOps framework definition for the Azure Migrate API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Migrate
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Migrate
  PublisherName: Azure Migrate
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Migrate
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
name: Microsoft Azure Migrate Finops
provider_name: Azure Migrate
provider_slug: microsoft-azure-migrate
publisher_name: Azure Migrate
service_category: API
slug: microsoft-azure-migrate-finops
source_filename: microsoft-azure-migrate-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Migrate\nproviderId: microsoft-azure-migrate\npublisherName: Azure Migrate\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Assessment\n  - Cloud Migration\n  - Database Migration\n  - Discovery\n  - Migration\n  - Replication\n  - Server Migration\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Migrate API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Migrate\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Migrate\n  PublisherName: Azure Migrate\n  InvoiceIssuerName: Azure Migrate\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n   \
  \ description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Migrate Projects API\n    baseURL: https://management.azure.com\n    tags:\n      - Migrate Project\n      - Migration\n      - Project Management\n    serviceName: Azure Migrate Projects API\n    serviceCategory: API\n  - name: Azure Migrate Assessments API\n    baseURL: https://management.azure.com\n    tags:\n      - Assessment\n      - Cost Estimation\n      - Readiness\n      - Sizing\n    serviceName: Azure Migrate Assessments API\n    serviceCategory: API\n  - name: Azure Migrate Discovery API\n    baseURL: https://management.azure.com\n    tags:\n      - Agentless\n      - Discovery\n   \
  \   - Hyper-V\n      - Inventory\n      - VMware\n    serviceName: Azure Migrate Discovery API\n    serviceCategory: API\n  - name: Azure Migrate Server Migration API\n    baseURL: https://management.azure.com\n    tags:\n      - Cutover\n      - Replication\n      - Server Migration\n      - Test Migration\n    serviceName: Azure Migrate Server Migration API\n    serviceCategory: API\n  - name: Azure Database Migration Service API\n    baseURL: https://management.azure.com\n    tags:\n      - Database Migration\n      - DMS\n      - MySQL\n      - PostgreSQL\n      - SQL Server\n    serviceName: Azure Database Migration Service API\n    serviceCategory: API\n  - name: Azure Migrate Web Apps Assessment API\n    baseURL: https://management.azure.com\n    tags:\n      - App Service\n      - ASP.NET\n      - Java\n      - Web Apps\n    serviceName: Azure Migrate Web Apps Assessment API\n    serviceCategory: API\n  - name: Azure Migrate Data Box API\n    baseURL: https://management.azure.com\n\
  \    tags:\n      - Data Box\n      - Offline Transfer\n      - Storage Migration\n    serviceName: Azure Migrate Data Box API\n    serviceCategory: API\n  - name: Azure Site Recovery API\n    baseURL: https://management.azure.com\n    tags:\n      - ASR\n      - Disaster Recovery\n      - Recovery Vault\n      - Replication\n      - Site Recovery\n    serviceName: Azure Site Recovery API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-migrate/refs/heads/main/finops/microsoft-azure-migrate-finops.yml
sources: []
specification: FinOps Framework
tags:
- Assessment
- Cloud Migration
- Database Migration
- Discovery
- Migration
- Replication
- Server Migration
- FinOps
- Cost Management
- FOCUS
---
