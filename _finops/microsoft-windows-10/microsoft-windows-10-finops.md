---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: microsoft-windows-10-winrt-openapi.yml
  format: yaml
  label: Windows Runtime (WinRT) API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-winrt-openapi.yml
- filename: microsoft-windows-10-win32-openapi.yml
  format: yaml
  label: Win32 API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-win32-openapi.yml
- filename: microsoft-windows-10-notifications-openapi.yml
  format: yaml
  label: Windows Notifications API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-notifications-openapi.yml
- filename: microsoft-windows-10-ml-openapi.yml
  format: yaml
  label: Windows ML API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-ml-openapi.yml
- filename: microsoft-windows-10-storage-openapi.yml
  format: yaml
  label: Windows Storage API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-storage-openapi.yml
- filename: microsoft-windows-10-cortana-openapi.yml
  format: yaml
  label: Windows Cortana API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-cortana-openapi.yml
- filename: microsoft-windows-10-ink-openapi.yml
  format: yaml
  label: Windows Ink API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-ink-openapi.yml
- filename: microsoft-windows-10-composition-openapi.yml
  format: yaml
  label: Windows Composition API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-composition-openapi.yml
- filename: microsoft-windows-10-directx-openapi.yml
  format: yaml
  label: DirectX Graphics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-directx-openapi.yml
- filename: microsoft-windows-10-media-capture-openapi.yml
  format: yaml
  label: Windows Media Capture API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-media-capture-openapi.yml
- filename: microsoft-windows-10-networking-openapi.yml
  format: yaml
  label: Windows Networking API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-networking-openapi.yml
- filename: microsoft-windows-10-bluetooth-openapi.yml
  format: yaml
  label: Windows Bluetooth API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-bluetooth-openapi.yml
- filename: microsoft-windows-10-geolocation-openapi.yml
  format: yaml
  label: Windows Geolocation API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-geolocation-openapi.yml
- filename: microsoft-windows-10-sensors-openapi.yml
  format: yaml
  label: Windows Sensors API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-sensors-openapi.yml
- filename: microsoft-windows-10-hello-openapi.yml
  format: yaml
  label: Windows Hello Authentication API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-hello-openapi.yml
- filename: microsoft-windows-10-winui-openapi.yml
  format: yaml
  label: WinUI API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-winui-openapi.yml
- filename: microsoft-windows-10-background-tasks-openapi.yml
  format: yaml
  label: Windows Background Tasks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-background-tasks-openapi.yml
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
description: FinOps framework definition for the Microsoft Windows 10 API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Microsoft Windows 10
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Microsoft Windows 10
  PublisherName: Microsoft Windows 10
  ServiceCategory: Developer Tools / API
  ServiceName: Microsoft Windows 10
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
name: Microsoft Windows 10 Finops
provider_name: Microsoft Windows 10
provider_slug: microsoft-windows-10
publisher_name: Microsoft Windows 10
service_category: API
slug: microsoft-windows-10-finops
source_filename: microsoft-windows-10-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Microsoft Windows 10\nproviderId: microsoft-windows-10\npublisherName: Microsoft Windows 10\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Desktop\n  - Operating System\n  - UWP\n  - Win32\n  - Windows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Microsoft Windows 10 API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Microsoft Windows 10\n  ServiceCategory: Developer Tools / API\n  ProviderName: Microsoft Windows 10\n  PublisherName: Microsoft Windows 10\n  InvoiceIssuerName: Microsoft Windows 10\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes\
  \ returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Windows Runtime (WinRT) API\n    baseURL: https://api.windows.com\n    tags:\n      - Universal Apps\n      - UWP\n      - Windows Runtime\n      - WinRT\n    serviceName: Windows Runtime (WinRT) API\n    serviceCategory: API\n  - name: Win32 API\n    baseURL: https://api.windows.com\n    tags:\n      - Desktop\n      - Native\n      - System Programming\n      - Win32\n    serviceName: Win32 API\n    serviceCategory: API\n  - name: Windows Notifications API\n    baseURL: https://api.windows.com\n    tags:\n      - Notifications\n      - Tiles\n      - Toast\n      - User Interface\n    serviceName: Windows Notifications\
  \ API\n    serviceCategory: API\n  - name: Windows ML API\n    baseURL: https://api.windows.com\n    tags:\n      - Artificial Intelligence\n      - Inference\n      - Machine Learning\n      - ONNX\n    serviceName: Windows ML API\n    serviceCategory: API\n  - name: Windows Storage API\n    baseURL: https://api.windows.com\n    tags:\n      - Data Management\n      - File System\n      - Files\n      - Storage\n    serviceName: Windows Storage API\n    serviceCategory: API\n  - name: Windows Cortana API\n    baseURL: https://api.windows.com\n    tags:\n      - Cortana\n      - Digital Assistant\n      - Voice\n      - Voice Commands\n    serviceName: Windows Cortana API\n    serviceCategory: API\n  - name: Windows Ink API\n    baseURL: https://api.windows.com\n    tags:\n      - Ink\n      - Input\n      - Pen\n      - Stylus\n    serviceName: Windows Ink API\n    serviceCategory: API\n  - name: Windows Composition API\n    baseURL: https://api.windows.com\n    tags:\n      - Animations\n\
  \      - Composition\n      - Graphics\n      - Visual Layer\n    serviceName: Windows Composition API\n    serviceCategory: API\n  - name: DirectX Graphics API\n    baseURL: https://api.windows.com\n    tags:\n      - DirectX\n      - Gaming\n      - Graphics\n      - Rendering\n    serviceName: DirectX Graphics API\n    serviceCategory: API\n  - name: Windows Media Capture API\n    baseURL: https://api.windows.com\n    tags:\n      - Audio\n      - Camera\n      - Media\n      - Video Capture\n    serviceName: Windows Media Capture API\n    serviceCategory: API\n  - name: Windows Networking API\n    baseURL: https://api.windows.com\n    tags:\n      - HTTP\n      - Networking\n      - Sockets\n      - WebSockets\n    serviceName: Windows Networking API\n    serviceCategory: API\n  - name: Windows Bluetooth API\n    baseURL: https://api.windows.com\n    tags:\n      - Bluetooth\n      - Devices\n      - IoT\n      - Wireless\n    serviceName: Windows Bluetooth API\n    serviceCategory:\
  \ API\n  - name: Windows Geolocation API\n    baseURL: https://api.windows.com\n    tags:\n      - Geolocation\n      - GPS\n      - Location\n      - Maps\n    serviceName: Windows Geolocation API\n    serviceCategory: API\n  - name: Windows Sensors API\n    baseURL: https://api.windows.com\n    tags:\n      - Devices\n      - Hardware\n      - IoT\n      - Sensors\n    serviceName: Windows Sensors API\n    serviceCategory: API\n  - name: Windows Hello Authentication API\n    baseURL: https://api.windows.com\n    tags:\n      - Authentication\n      - Biometrics\n      - Identity\n      - Security\n    serviceName: Windows Hello Authentication API\n    serviceCategory: API\n  - name: WinUI API\n    baseURL: https://api.windows.com\n    tags:\n      - Controls\n      - Fluent Design\n      - User Interface\n      - XAML\n    serviceName: WinUI API\n    serviceCategory: API\n  - name: Windows Background Tasks API\n    baseURL: https://api.windows.com\n    tags:\n      - App Lifecycle\n\
  \      - Background Tasks\n      - Scheduling\n    serviceName: Windows Background Tasks API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/finops/microsoft-windows-10-finops.yml
sources: []
specification: FinOps Framework
tags:
- Desktop
- Operating System
- UWP
- Win32
- Windows
- FinOps
- Cost Management
- FOCUS
---
