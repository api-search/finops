---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-endpoint-configuration-management-configmgr-rest-api-openapi.yml
  format: yaml
  label: Configuration Manager REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-configmgr-rest-api-openapi.yml
- filename: microsoft-endpoint-configuration-management-intune-graph-api-openapi.yml
  format: yaml
  label: Microsoft Intune Graph API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-intune-graph-api-openapi.yml
- filename: microsoft-endpoint-configuration-management-intune-data-warehouse-api-openapi.yml
  format: yaml
  label: Intune Data Warehouse API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-intune-data-warehouse-api-openapi.yml
- filename: microsoft-endpoint-configuration-management-intune-reporting-export-api-openapi.yml
  format: yaml
  label: Intune Reporting Export API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/openapi/microsoft-endpoint-configuration-management-intune-reporting-export-api-openapi.yml
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
description: FinOps framework definition for the Microsoft Endpoint Configuration Management API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Endpoint Configuration Management
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Endpoint Configuration Management
  PublisherName: Microsoft Endpoint Configuration Management
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Endpoint Configuration Management
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
name: Microsoft Endpoint Configuration Management Finops
provider_name: Microsoft Endpoint Configuration Management
provider_slug: microsoft-endpoint-configuration-management
publisher_name: Microsoft Endpoint Configuration Management
service_category: API
slug: microsoft-endpoint-configuration-management-finops
source_filename: microsoft-endpoint-configuration-management-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Endpoint Configuration Management\nproviderId: microsoft-endpoint-configuration-management\npublisherName: Microsoft Endpoint Configuration Management\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Compliance\n  - Configuration Management\n  - Device Management\n  - Endpoint Management\n  - Mobile Device Management\n  - Patch Management\n  - Software Deployment\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Endpoint Configuration Management API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n  across the provider's APIs.\n\
  principles:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n\
  \      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Endpoint Configuration Management\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Endpoint Configuration Management\n  PublisherName: Microsoft Endpoint Configuration Management\n  InvoiceIssuerName: Microsoft Endpoint Configuration Management\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory:\
  \ Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Configuration Manager REST API\n    baseURL: https://{siteserver}/AdminService\n    tags:\n      - Admin Service\n      - Configuration Manager\n      - REST API\n    serviceName: Configuration Manager REST API\n    serviceCategory: API\n  - name: Configuration Manager PowerShell Cmdlets\n    baseURL: ''\n    tags:\n      - Automation\n      - Configuration\
  \ Manager\n      - PowerShell\n      - Scripting\n    serviceName: Configuration Manager PowerShell Cmdlets\n    serviceCategory: API\n  - name: Configuration Manager SDK\n    baseURL: ''\n    tags:\n      - Configuration Manager\n      - Development\n      - SDK\n      - WMI\n    serviceName: Configuration Manager SDK\n    serviceCategory: API\n  - name: Microsoft Intune Graph API\n    baseURL: https://graph.microsoft.com/v1.0\n    tags:\n      - Compliance\n      - Device Management\n      - Intune\n      - Microsoft Graph\n    serviceName: Microsoft Intune Graph API\n    serviceCategory: API\n  - name: Intune Data Warehouse API\n    baseURL: https://fef.{location}.manage.microsoft.com/ReportingService/DataWarehouseFEService\n    tags:\n      - Data Warehouse\n      - Intune\n      - OData\n      - Reporting\n    serviceName: Intune Data Warehouse API\n    serviceCategory: API\n  - name: Intune App SDK\n    baseURL: ''\n    tags:\n      - App Protection\n      - Intune\n      - Mobile\
  \ Apps\n      - SDK\n    serviceName: Intune App SDK\n    serviceCategory: API\n  - name: Intune Reporting Export API\n    baseURL: https://graph.microsoft.com/v1.0/deviceManagement/reports\n    tags:\n      - Export\n      - Intune\n      - Microsoft Graph\n      - Reporting\n    serviceName: Intune Reporting Export API\n    serviceCategory: API\n  - name: Intune App Wrapping Tool\n    baseURL: ''\n    tags:\n      - Android\n      - App Protection\n      - Intune\n      - iOS\n      - Mobile Apps\n    serviceName: Intune App Wrapping Tool\n    serviceCategory: API\n  - name: Intune PowerShell SDK\n    baseURL: ''\n    tags:\n      - Automation\n      - Intune\n      - PowerShell\n      - SDK\n    serviceName: Intune PowerShell SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN:\
  \ Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-endpoint-configuration-management/refs/heads/main/finops/microsoft-endpoint-configuration-management-finops.yml
sources: []
specification: FinOps Framework
tags:
- Compliance
- Configuration Management
- Device Management
- Endpoint Management
- Mobile Device Management
- Patch Management
- Software Deployment
- FinOps
- Cost Management
- FOCUS
---
