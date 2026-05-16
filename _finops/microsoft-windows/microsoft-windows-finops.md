---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Windows Runtime (WinRT) API
  slug: windows-runtime-winrt-api
  spec_type: OpenAPI
  url: https://api.windows.com/openapi.json
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
description: FinOps framework definition for the Microsoft Windows API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Windows
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Windows
  PublisherName: Microsoft Windows
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Windows
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
name: Microsoft Windows Finops
provider_name: Microsoft Windows
provider_slug: microsoft-windows
publisher_name: Microsoft Windows
service_category: API
slug: microsoft-windows-finops
source_filename: microsoft-windows-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Windows\nproviderId: microsoft-windows\npublisherName: Microsoft Windows\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Desktop\n  - Development\n  - Microsoft\n  - Operating System\n  - Windows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Windows API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Windows\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Windows\n  PublisherName: Microsoft Windows\n  InvoiceIssuerName: Microsoft Windows\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Windows Runtime (WinRT) API\n    baseURL: ''\n    tags:\n      - Applications\n      - UWP\n      - Windows\n      - WinRT\n    serviceName: Windows Runtime (WinRT) API\n    serviceCategory: API\n  - name: Win32 API\n    baseURL: ''\n    tags:\n      - C++\n      - Native\n      - Win32\n      - Windows\n    serviceName: Win32 API\n    serviceCategory: API\n  - name: Windows Management Instrumentation (WMI)\n    baseURL: ''\n    tags:\n      - Management\n      - System Administration\n      - Windows\n      - WMI\n    serviceName: Windows Management Instrumentation (WMI)\n    serviceCategory: API\n  - name: Windows PowerShell API\n \
  \   baseURL: ''\n    tags:\n      - Automation\n      - PowerShell\n      - Scripting\n      - Windows\n    serviceName: Windows PowerShell API\n    serviceCategory: API\n  - name: Windows Registry API\n    baseURL: ''\n    tags:\n      - Configuration\n      - Registry\n      - System\n      - Windows\n    serviceName: Windows Registry API\n    serviceCategory: API\n  - name: Windows Shell API\n    baseURL: ''\n    tags:\n      - Explorer\n      - Shell\n      - UI\n      - Windows\n    serviceName: Windows Shell API\n    serviceCategory: API\n  - name: DirectX Graphics API\n    baseURL: ''\n    tags:\n      - DirectX\n      - Gaming\n      - Graphics\n      - Windows\n    serviceName: DirectX Graphics API\n    serviceCategory: API\n  - name: Windows Notification API\n    baseURL: ''\n    tags:\n      - Notifications\n      - Toast\n      - User Interface\n      - Windows\n    serviceName: Windows Notification API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n\
  \    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows/refs/heads/main/finops/microsoft-windows-finops.yml
sources: []
specification: FinOps Framework
tags:
- Desktop
- Development
- Microsoft
- Operating System
- Windows
- FinOps
- Cost Management
- FOCUS
---
