---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: iis-administration-api.yml
  format: yaml
  label: IIS Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-server/refs/heads/main/openapi/iis-administration-api.yml
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
description: FinOps framework definition for the Microsoft Windows Server API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Windows Server
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Windows Server
  PublisherName: Microsoft Windows Server
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Windows Server
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
name: Microsoft Windows Server Finops
provider_name: Microsoft Windows Server
provider_slug: microsoft-windows-server
publisher_name: Microsoft Windows Server
service_category: API
slug: microsoft-windows-server-finops
source_filename: microsoft-windows-server-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Windows Server\nproviderId: microsoft-windows-server\npublisherName: Microsoft Windows Server\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Datacenter\n  - Enterprise\n  - Infrastructure\n  - Microsoft\n  - Operating System\n  - Server Management\n  - Windows Server\n  - Windows Server 2025\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Windows Server API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Windows Server\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Windows Server\n  PublisherName: Microsoft Windows Server\n  InvoiceIssuerName: Microsoft Windows Server\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n\
  \      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Windows Server Management API\n    baseURL: https://localhost\n    tags:\n      - Administration\n      - Management\n      - PowerShell\n      - WMI\n    serviceName: Windows Server Management API\n    serviceCategory: API\n  - name: Windows Remote Management (WinRM)\n    baseURL: http://localhost:5985\n    tags:\n      - PowerShell Remoting\n      - Remote Management\n      - SOAP\n      - WS-Management\n    serviceName: Windows Remote Management (WinRM)\n    serviceCategory: API\n  - name: Active Directory Domain\
  \ Services API\n    baseURL: ldap://localhost:389\n    tags:\n      - Active Directory\n      - Authentication\n      - Directory Services\n      - LDAP\n    serviceName: Active Directory Domain Services API\n    serviceCategory: API\n  - name: Hyper-V Management API\n    baseURL: https://localhost\n    tags:\n      - Hyper-V\n      - Virtual Machines\n      - Virtualization\n    serviceName: Hyper-V Management API\n    serviceCategory: API\n  - name: Windows Server Update Services (WSUS) API\n    baseURL: https://localhost:8530\n    tags:\n      - Patch Management\n      - Updates\n      - WSUS\n    serviceName: Windows Server Update Services (WSUS) API\n    serviceCategory: API\n  - name: Windows Admin Center API\n    baseURL: https://localhost:6516\n    tags:\n      - Admin Center\n      - Gateway\n      - REST API\n      - Web Management\n    serviceName: Windows Admin Center API\n    serviceCategory: API\n  - name: DNS Server Management API\n    baseURL: https://localhost\n    tags:\n\
  \      - DNS\n      - Name Resolution\n      - Networking\n    serviceName: DNS Server Management API\n    serviceCategory: API\n  - name: Windows Management Instrumentation (WMI) API\n    baseURL: https://localhost\n    tags:\n      - COM\n      - Management\n      - Monitoring\n      - Scripting\n      - WMI\n    serviceName: Windows Management Instrumentation (WMI) API\n    serviceCategory: API\n  - name: IIS Administration API\n    baseURL: https://localhost:55539\n    tags:\n      - IIS\n      - REST API\n      - Web Management\n      - Web Server\n    serviceName: IIS Administration API\n    serviceCategory: API\n  - name: Remote Desktop Services API\n    baseURL: https://localhost\n    tags:\n      - RDS\n      - Remote Access\n      - Remote Desktop\n      - Terminal Services\n    serviceName: Remote Desktop Services API\n    serviceCategory: API\n  - name: Failover Clustering API\n    baseURL: https://localhost\n    tags:\n      - Cluster Management\n      - Failover Clustering\n\
  \      - High Availability\n    serviceName: Failover Clustering API\n    serviceCategory: API\n  - name: DHCP Server Management API\n    baseURL: https://localhost\n    tags:\n      - DHCP\n      - IP Address Management\n      - Networking\n    serviceName: DHCP Server Management API\n    serviceCategory: API\n  - name: SMB File Server API\n    baseURL: https://localhost\n    tags:\n      - File Sharing\n      - Network Storage\n      - SMB\n      - Storage\n    serviceName: SMB File Server API\n    serviceCategory: API\n  - name: Windows Event Log API\n    baseURL: https://localhost\n    tags:\n      - Diagnostics\n      - Event Log\n      - Logging\n      - Monitoring\n    serviceName: Windows Event Log API\n    serviceCategory: API\n  - name: Storage Spaces Direct API\n    baseURL: https://localhost\n    tags:\n      - Hyper-Converged\n      - Software-Defined Storage\n      - Storage\n      - Storage Spaces Direct\n    serviceName: Storage Spaces Direct API\n    serviceCategory: API\n\
  \  - name: Network Policy Server (NPS) RADIUS API\n    baseURL: https://localhost\n    tags:\n      - Authentication\n      - Network Access\n      - NPS\n      - RADIUS\n      - VPN\n    serviceName: Network Policy Server (NPS) RADIUS API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-server/refs/heads/main/finops/microsoft-windows-server-finops.yml
sources: []
specification: FinOps Framework
tags:
- Datacenter
- Enterprise
- Infrastructure
- Microsoft
- Operating System
- Server Management
- Windows Server
- Windows Server 2025
- FinOps
- Cost Management
- FOCUS
---
