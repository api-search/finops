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
description: FinOps framework definition for the UNIX System Call API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: UNIX System Call
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: UNIX System Call
  PublisherName: UNIX System Call
  ServiceCategory: Developer Tools / API
  ServiceName: UNIX System Call
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
name: Unix Finops
provider_name: UNIX System Call
provider_slug: unix
publisher_name: UNIX System Call
service_category: API
slug: unix-finops
source_filename: unix-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: UNIX System Call\nproviderId: unix\npublisherName: UNIX System Call\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - C-Api\n  - Ieee-1003\n  - Kernel\n  - Open-Group\n  - Operating-System\n  - Posix\n  - System-Calls\n  - Unix\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the UNIX System Call API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: UNIX System Call\n  ServiceCategory: Developer Tools / API\n  ProviderName: UNIX System Call\n  PublisherName: UNIX System Call\n  InvoiceIssuerName: UNIX System Call\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: File System Operations API\n    baseURL: system://unix/fs\n    tags:\n      - Directories\n      - Files\n      - Filesystem\n      - Io\n    serviceName: File System Operations API\n    serviceCategory: API\n  - name: Process Management API\n    baseURL: system://unix/process\n    tags:\n      - Execution\n      - Processes\n      - Scheduling\n    serviceName: Process Management API\n    serviceCategory: API\n  - name: Interprocess Communication API\n    baseURL: system://unix/ipc\n    tags:\n      - Ipc\n      - Pipes\n      - Shared-Memory\n      - Signals\n      - Sockets\n    serviceName: Interprocess Communication\
  \ API\n    serviceCategory: API\n  - name: Memory Management API\n    baseURL: system://unix/memory\n    tags:\n      - Allocation\n      - Memory\n      - Mmap\n      - Virtual-Memory\n    serviceName: Memory Management API\n    serviceCategory: API\n  - name: System Information API\n    baseURL: system://unix/sysinfo\n    tags:\n      - Configuration\n      - Groups\n      - Information\n      - System\n      - Users\n    serviceName: System Information API\n    serviceCategory: API\n  - name: POSIX Threads API\n    baseURL: system://unix/pthreads\n    tags:\n      - Concurrency\n      - Mutexes\n      - Pthreads\n      - Synchronization\n      - Threads\n    serviceName: POSIX Threads API\n    serviceCategory: API\n  - name: I/O Multiplexing API\n    baseURL: system://unix/io-multiplex\n    tags:\n      - Event-Driven\n      - Io\n      - Multiplexing\n      - Non-Blocking\n      - Poll\n      - Select\n    serviceName: I/O Multiplexing API\n    serviceCategory: API\n  - name: POSIX\
  \ Semaphores API\n    baseURL: system://unix/semaphores\n    tags:\n      - Concurrency\n      - Ipc\n      - Semaphores\n      - Synchronization\n    serviceName: POSIX Semaphores API\n    serviceCategory: API\n  - name: POSIX Message Queues API\n    baseURL: system://unix/mqueue\n    tags:\n      - Asynchronous\n      - Ipc\n      - Message-Queues\n      - Messaging\n    serviceName: POSIX Message Queues API\n    serviceCategory: API\n  - name: Terminal and Device I/O API\n    baseURL: system://unix/terminal\n    tags:\n      - Device-Io\n      - Serial\n      - Terminal\n      - Termios\n      - Tty\n    serviceName: Terminal and Device I/O API\n    serviceCategory: API\n  - name: File Locking API\n    baseURL: system://unix/file-locking\n    tags:\n      - Advisory-Locking\n      - Concurrency\n      - Fcntl\n      - File-Locking\n    serviceName: File Locking API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n\
  \    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/unix/refs/heads/main/finops/unix-finops.yml
sources: []
specification: FinOps Framework
tags:
- C-Api
- Ieee-1003
- Kernel
- Open-Group
- Operating-System
- Posix
- System-Calls
- Unix
- FinOps
- Cost Management
- FOCUS
---
