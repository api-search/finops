---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: virtualMachines.json
  format: json
  label: Azure Virtual Machines REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/compute/resource-manager/Microsoft.Compute/ComputeRP/stable/2023-09-01/virtualMachines.json
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
description: FinOps framework definition for the Azure Virtual Machines API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure Virtual Machines
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure Virtual Machines
  PublisherName: Azure Virtual Machines
  ServiceCategory: Developer Tools / API
  ServiceName: Azure Virtual Machines
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
name: Microsoft Azure Virtual Machines Finops
provider_name: Azure Virtual Machines
provider_slug: microsoft-azure-virtual-machines
publisher_name: Azure Virtual Machines
service_category: API
slug: microsoft-azure-virtual-machines-finops
source_filename: microsoft-azure-virtual-machines-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure Virtual Machines\nproviderId: microsoft-azure-virtual-machines\npublisherName: Azure Virtual Machines\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Computing\n  - Compute\n  - IaaS\n  - Infrastructure\n  - Virtual Machines\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure Virtual Machines API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure Virtual Machines\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure Virtual Machines\n  PublisherName: Azure Virtual Machines\n  InvoiceIssuerName: Azure Virtual Machines\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure Virtual Machines REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Compute\n      - REST API\n      - Virtual Machines\n    serviceName: Azure Virtual Machines REST API\n    serviceCategory: API\n  - name: Azure Virtual Machine Scale Sets REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Autoscaling\n      - Load Balancing\n      - Virtual Machine Scale Sets\n    serviceName: Azure Virtual Machine Scale Sets REST API\n    serviceCategory: API\n  - name: Azure Virtual Machine Extensions REST API\n    baseURL: https://management.azure.com\n\
  \    tags:\n      - Automation\n      - Configuration\n      - Extensions\n    serviceName: Azure Virtual Machine Extensions REST API\n    serviceCategory: API\n  - name: Azure Virtual Machine Images REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Images\n      - Marketplace\n      - VM Images\n    serviceName: Azure Virtual Machine Images REST API\n    serviceCategory: API\n  - name: Azure Virtual Machine Sizes REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Capacity\n      - SKUs\n      - VM Sizes\n    serviceName: Azure Virtual Machine Sizes REST API\n    serviceCategory: API\n  - name: Azure Virtual Machine Run Commands REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Diagnostics\n      - Run Commands\n      - Scripting\n    serviceName: Azure Virtual Machine Run Commands REST API\n    serviceCategory: API\n  - name: Azure Availability Sets REST API\n    baseURL: https://management.azure.com\n    tags:\n      -\
  \ Availability Sets\n      - Fault Domains\n      - High Availability\n    serviceName: Azure Availability Sets REST API\n    serviceCategory: API\n  - name: Azure Proximity Placement Groups REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Co-Location\n      - Low Latency\n      - Proximity Placement Groups\n    serviceName: Azure Proximity Placement Groups REST API\n    serviceCategory: API\n  - name: Azure Dedicated Hosts REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Compliance\n      - Dedicated Hosts\n      - Isolation\n    serviceName: Azure Dedicated Hosts REST API\n    serviceCategory: API\n  - name: Azure Capacity Reservations REST API\n    baseURL: https://management.azure.com\n    tags:\n      - Capacity Reservations\n      - Planning\n      - Reserved Capacity\n    serviceName: Azure Capacity Reservations REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests\
  \ / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-virtual-machines/refs/heads/main/finops/microsoft-azure-virtual-machines-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Computing
- Compute
- IaaS
- Infrastructure
- Virtual Machines
- FinOps
- Cost Management
- FOCUS
---
