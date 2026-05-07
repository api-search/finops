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
  billingFrequency: Annual
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Adjustment
  - Credit
  pricingCategory: Subscription + Pay-As-You-Go
description: 'FOCUS-aligned FinOps for Windows Server: perpetual core-based licenses (Standard $1,176, Datacenter $6,771 per 16-core pack) plus mandatory CALs, with optional Azure-Arc-billed pay-as-you-go ($33.58/core/month or $0.046/core/hour) for elastic workloads.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Purchase
  InvoiceIssuerName: Microsoft Corporation
  ProviderName: Microsoft
  PublisherName: Microsoft Corporation
  ServiceCategory: Compute
  ServiceName: Microsoft Windows Server
  ServiceSubcategory: Operating System
layout: finops
meters:
- aggregation: sum
  dimensions:
  - tenant
  - server
  name: standard_core_licenses
  unit: core-license
- aggregation: sum
  dimensions:
  - tenant
  - server
  name: datacenter_core_licenses
  unit: core-license
- aggregation: sum
  dimensions:
  - tenant
  - cal_type
  name: cals
  unit: seat-year
- aggregation: sum
  dimensions:
  - server
  - region
  name: payg_core_hours
  unit: core-hour
- aggregation: sum
  dimensions:
  - server
  - region
  name: payg_core_months
  unit: core-month
name: Microsoft Windows Server Finops
provider_name: Microsoft Windows Server
provider_slug: microsoft-windows-server
publisher_name: Microsoft Corporation
service_category: Operating System / Server
slug: microsoft-windows-server-finops
source_filename: microsoft-windows-server-finops.yml
source_heading: FinOps Profile
source_url: https://www.microsoft.com/en-us/windows-server/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nschema: https://www.finops.org/framework/\nprovider: Microsoft Windows Server\nproviderId: microsoft-windows-server\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - FinOps\n  - FOCUS\n  - Cost Management\n  - Microsoft\n  - Server\n  - Operating System\ndescription: 'FOCUS-aligned FinOps for Windows Server: perpetual core-based licenses (Standard $1,176,\n  Datacenter $6,771 per 16-core pack) plus mandatory CALs, with optional Azure-Arc-billed pay-as-you-go\n  ($33.58/core/month or $0.046/core/hour) for elastic workloads.'\nsources:\n  - https://www.microsoft.com/en-us/windows-server/pricing\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\npublisherName: Microsoft Corporation\nserviceCategory: Operating System / Server\n\
  billingModel:\n  pricingCategory: Subscription + Pay-As-You-Go\n  billingFrequency: Annual\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Adjustment\n    - Credit\nfocusColumns:\n  ServiceName: Microsoft Windows Server\n  ServiceCategory: Compute\n  ServiceSubcategory: Operating System\n  ProviderName: Microsoft\n  PublisherName: Microsoft Corporation\n  InvoiceIssuerName: Microsoft Corporation\n  BillingCurrency: USD\n  ChargeCategory: Purchase\nmeters:\n  - name: standard_core_licenses\n    unit: core-license\n    aggregation: sum\n    dimensions:\n      - tenant\n      - server\n  - name: datacenter_core_licenses\n    unit: core-license\n    aggregation: sum\n    dimensions:\n      - tenant\n      - server\n  - name: cals\n    unit: seat-year\n    aggregation: sum\n    dimensions:\n      - tenant\n      - cal_type\n  - name: payg_core_hours\n    unit: core-hour\n    aggregation: sum\n    dimensions:\n      - server\n      - region\n  - name:\
  \ payg_core_months\n    unit: core-month\n    aggregation: sum\n    dimensions:\n      - server\n      - region\nprinciples:\n  - name: Visibility\n    description: Use Volume Licensing Service Center exports for perpetual core/CAL counts; pull Azure\n      Cost Management for Arc-billed pay-as-you-go core-hours; tag servers with workload owner via\n      Azure Arc machine tags.\n  - name: Allocation\n    description: Allocate Datacenter packs to virtualization clusters and Standard packs to physical\n      hosts; charge CALs back per business unit; Arc-billed PAYG can be tagged at the server level for\n      direct chargeback.\n  - name: Optimization\n    description: Consolidate VM density to fewer Datacenter-licensed hosts; right-size cores (avoid\n      over-licensing 8-core servers with 16-core packs); use Azure Hybrid Benefit for cloud workloads;\n      switch bursty / dev workloads to PAYG instead of perpetual.\n  - name: Accountability\n    description: Assign a license owner per\
  \ cluster; review CAL consumption against headcount quarterly;\n      reconcile PAYG core-hours against forecast.\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-windows-server/refs/heads/main/finops/microsoft-windows-server-finops.yml
sources:
- https://www.microsoft.com/en-us/windows-server/pricing
specification: FinOps Framework
tags:
- FinOps
- FOCUS
- Cost Management
- Microsoft
- Server
- Operating System
---
