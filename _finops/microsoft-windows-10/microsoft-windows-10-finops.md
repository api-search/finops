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
  slug: windows-runtime-winrt-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-winrt-openapi.yml
- filename: microsoft-windows-10-win32-openapi.yml
  format: yaml
  label: Win32 API
  slug: win32-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-win32-openapi.yml
- filename: microsoft-windows-10-notifications-openapi.yml
  format: yaml
  label: Windows Notifications API
  slug: windows-notifications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-notifications-openapi.yml
- filename: microsoft-windows-10-ml-openapi.yml
  format: yaml
  label: Windows ML API
  slug: windows-ml-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-ml-openapi.yml
- filename: microsoft-windows-10-storage-openapi.yml
  format: yaml
  label: Windows Storage API
  slug: windows-storage-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-storage-openapi.yml
- filename: microsoft-windows-10-cortana-openapi.yml
  format: yaml
  label: Windows Cortana API
  slug: windows-cortana-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-cortana-openapi.yml
- filename: microsoft-windows-10-ink-openapi.yml
  format: yaml
  label: Windows Ink API
  slug: windows-ink-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-ink-openapi.yml
- filename: microsoft-windows-10-composition-openapi.yml
  format: yaml
  label: Windows Composition API
  slug: windows-composition-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-composition-openapi.yml
- filename: microsoft-windows-10-directx-openapi.yml
  format: yaml
  label: DirectX Graphics API
  slug: directx-graphics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-directx-openapi.yml
- filename: microsoft-windows-10-media-capture-openapi.yml
  format: yaml
  label: Windows Media Capture API
  slug: windows-media-capture-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-media-capture-openapi.yml
- filename: microsoft-windows-10-networking-openapi.yml
  format: yaml
  label: Windows Networking API
  slug: windows-networking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-networking-openapi.yml
- filename: microsoft-windows-10-bluetooth-openapi.yml
  format: yaml
  label: Windows Bluetooth API
  slug: windows-bluetooth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-bluetooth-openapi.yml
- filename: microsoft-windows-10-geolocation-openapi.yml
  format: yaml
  label: Windows Geolocation API
  slug: windows-geolocation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-geolocation-openapi.yml
- filename: microsoft-windows-10-sensors-openapi.yml
  format: yaml
  label: Windows Sensors API
  slug: windows-sensors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-sensors-openapi.yml
- filename: microsoft-windows-10-hello-openapi.yml
  format: yaml
  label: Windows Hello Authentication API
  slug: windows-hello-authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-hello-openapi.yml
- filename: microsoft-windows-10-winui-openapi.yml
  format: yaml
  label: WinUI API
  slug: winui-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-winui-openapi.yml
- filename: microsoft-windows-10-background-tasks-openapi.yml
  format: yaml
  label: Windows Background Tasks API
  slug: windows-background-tasks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/openapi/microsoft-windows-10-background-tasks-openapi.yml
billing_model:
  billingCurrency: USD
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription
description: 'FOCUS-aligned FinOps for Windows 10: post-EOS the primary spend lever is per-device, per-year Extended Security Updates (ESU) under Volume Licensing, with cumulative pricing that doubles each year (Year 1 $61, Year 2 $122, Year 3 $244). Windows 10 VMs running on Microsoft cloud services receive ESU at no additional charge.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  PricingUnit: device-year
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Operating System
  ServiceName: Microsoft Windows 10
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - device
  name: esu_year_1_devices
  unit: device-year
- aggregation: sum
  dimensions:
  - tenant
  - device
  name: esu_year_2_devices
  unit: device-year
- aggregation: sum
  dimensions:
  - tenant
  - device
  name: esu_year_3_devices
  unit: device-year
- aggregation: sum
  dimensions:
  - cloud_service
  - tenant
  name: esu_cloud_entitled_devices
  unit: device-year
name: Microsoft Windows 10 Finops
provider_name: Microsoft Windows 10
provider_slug: microsoft-windows-10
publisher_name: Microsoft Corporation
service_category: Operating System / Endpoint
slug: microsoft-windows-10-finops
source_filename: microsoft-windows-10-finops.yml
source_heading: FinOps Profile
source_url: https://learn.microsoft.com/en-us/windows/whats-new/extended-security-updates
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Windows 10\nproviderId: microsoft-windows-10\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Microsoft\n  - Operating System\ndescription: 'FOCUS-aligned FinOps for Windows 10: post-EOS the primary spend lever is per-device,\n  per-year Extended Security Updates (ESU) under Volume Licensing, with cumulative pricing that doubles\n  each year (Year 1 $61, Year 2 $122, Year 3 $244). Windows 10 VMs running on Microsoft cloud services\n  receive ESU at no additional charge.'\nsources:\n  - https://learn.microsoft.com/en-us/windows/whats-new/extended-security-updates\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName:\
  \ Microsoft Corporation\nserviceCategory: Operating System / Endpoint\nbillingModel:\n  pricingCategory: Subscription\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Windows 10\n  ServiceCategory: Operating System\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  PricingUnit: device-year\n  ChargeCategory: Purchase\nmeters:\n  - name: esu_year_1_devices\n    unit: device-year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - device\n  - name: esu_year_2_devices\n    unit: device-year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - device\n  - name: esu_year_3_devices\n    unit: device-year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - device\n  - name: esu_cloud_entitled_devices\n    unit: device-year\n    aggregation: sum\n    dimensions:\n\
  \      - cloud_service\n      - tenant\nprinciples:\n  - name: Visibility\n    description: Pull ESU enrollment counts from Microsoft 365 admin center Volume Licensing Product\n      Details; cross-reference with Intune device inventory to identify devices still on Windows 10\n      22H2.\n  - name: Allocation\n    description: Tag ESU charges by business unit / OU; allocate cloud-entitled (no-cost) ESU separately\n      from Volume Licensing ESU so the migration value is visible.\n  - name: Optimization\n    description: Migrate eligible devices to Windows 11 to avoid the year-2 ($122) and year-3 ($244)\n      ESU price escalations; move stragglers to Windows 365 / Azure Virtual Desktop where ESU is free;\n      decommission Windows 10 devices on hardware ineligible for Windows 11.\n  - name: Accountability\n    description: Assign an ESU budget owner per business unit; review remaining Windows 10 inventory\n      monthly; require approval for new ESU year purchases.\nmaintainers:\n \
  \ - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-10/refs/heads/main/finops/microsoft-windows-10-finops.yml
sources:
- https://learn.microsoft.com/en-us/windows/whats-new/extended-security-updates
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Microsoft
- Operating System
---
