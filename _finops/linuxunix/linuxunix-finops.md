---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Linux/Unix System API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Linux/Unix System
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Linux/Unix System
  PublisherName: Linux/Unix System
  ServiceCategory: Developer Tools / API
  ServiceName: Linux/Unix System
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
name: Linuxunix Finops
provider_name: Linux/Unix System
provider_slug: linuxunix
publisher_name: Linux/Unix System
service_category: API
slug: linuxunix-finops
source_filename: linuxunix-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Linux/Unix System\nproviderId: linuxunix\npublisherName: Linux/Unix System\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Kernel\n  - Linux\n  - Operating System\n  - System\n  - Unix\n  - POSIX\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Linux/Unix System API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Linux/Unix System\n  ServiceCategory: Developer Tools / API\n  ProviderName: Linux/Unix System\n  PublisherName: Linux/Unix System\n  InvoiceIssuerName: Linux/Unix System\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in\
  \ API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: System Calls API\n    baseURL: ''\n    tags:\n      - Kernel\n      - Low-Level\n      - Syscalls\n    serviceName: System Calls API\n    serviceCategory: API\n  - name: POSIX API\n    baseURL: ''\n    tags:\n      - POSIX\n      - Standards\n      - Portability\n    serviceName: POSIX API\n    serviceCategory: API\n  - name: D-Bus API\n    baseURL: ''\n    tags:\n      - IPC\n      - Messaging\n      - Desktop\n    serviceName: D-Bus API\n    serviceCategory: API\n  - name: Netlink API\n    baseURL: ''\n    tags:\n      - Networking\n      - Kernel\n      - Sockets\n    serviceName: Netlink API\n    serviceCategory: API\n  - name: procfs API\n    baseURL:\
  \ ''\n    tags:\n      - Filesystem\n      - Process\n      - Monitoring\n    serviceName: procfs API\n    serviceCategory: API\n  - name: sysfs API\n    baseURL: ''\n    tags:\n      - Filesystem\n      - Kernel\n      - Devices\n    serviceName: sysfs API\n    serviceCategory: API\n  - name: inotify API\n    baseURL: ''\n    tags:\n      - Filesystem\n      - Monitoring\n      - Events\n    serviceName: inotify API\n    serviceCategory: API\n  - name: epoll API\n    baseURL: ''\n    tags:\n      - I/O\n      - Events\n      - Performance\n    serviceName: epoll API\n    serviceCategory: API\n  - name: udev API\n    baseURL: ''\n    tags:\n      - Devices\n      - Hardware\n      - Hotplug\n    serviceName: udev API\n    serviceCategory: API\n  - name: systemd API\n    baseURL: ''\n    tags:\n      - Init\n      - Service Management\n      - System\n    serviceName: systemd API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests\
  \ / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/linuxunix/refs/heads/main/finops/linuxunix-finops.yml
sources: []
specification: FinOps Framework
tags:
- Kernel
- Linux
- Operating System
- System
- Unix
- POSIX
- FinOps
- Cost Management
- FOCUS
---
