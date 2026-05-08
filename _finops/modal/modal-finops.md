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
description: FinOps framework definition for the Modal API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Modal
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Modal
  PublisherName: Modal
  ServiceCategory: Developer Tools / API
  ServiceName: Modal
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
name: Modal Finops
provider_name: Modal
provider_slug: modal
publisher_name: Modal
service_category: API
slug: modal-finops
source_filename: modal-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Modal\nproviderId: modal\npublisherName: Modal\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Serverless\n  - Compute\n  - Python\n  - Inference\n  - GPU\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Modal API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Modal\n  ServiceCategory: Developer Tools / API\n  ProviderName: Modal\n  PublisherName: Modal\n  InvoiceIssuerName: Modal\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Modal Functions API\n    baseURL: https://api.modal.com\n    tags:\n      - Functions\n      - Serverless\n      - Python\n    serviceName: Modal Functions API\n    serviceCategory: API\n  - name: Modal Apps API\n    baseURL: https://api.modal.com\n    tags:\n      - Apps\n      - Deployments\n    serviceName: Modal Apps API\n    serviceCategory: API\n  - name: Modal Sandboxes API\n    baseURL: https://api.modal.com\n    tags:\n      - Sandboxes\n      - Code Execution\n      - Agents\n    serviceName: Modal Sandboxes API\n    serviceCategory: API\n  - name: Modal Images API\n    baseURL: https://api.modal.com\n    tags:\n      - Images\n      - Containers\n      - Build\n    serviceName: Modal Images API\n    serviceCategory: API\n  - name: Modal\
  \ Volumes API\n    baseURL: https://api.modal.com\n    tags:\n      - Volumes\n      - Storage\n      - Persistent\n    serviceName: Modal Volumes API\n    serviceCategory: API\n  - name: Modal Network File Systems API\n    baseURL: https://api.modal.com\n    tags:\n      - File System\n      - NFS\n      - Storage\n    serviceName: Modal Network File Systems API\n    serviceCategory: API\n  - name: Modal Secrets API\n    baseURL: https://api.modal.com\n    tags:\n      - Secrets\n      - Configuration\n    serviceName: Modal Secrets API\n    serviceCategory: API\n  - name: Modal Web Endpoints API\n    baseURL: https://api.modal.com\n    tags:\n      - HTTP\n      - Web\n      - WSGI\n      - ASGI\n    serviceName: Modal Web Endpoints API\n    serviceCategory: API\n  - name: Modal Cron API\n    baseURL: https://api.modal.com\n    tags:\n      - Cron\n      - Schedules\n    serviceName: Modal Cron API\n    serviceCategory: API\n  - name: Modal Queues API\n    baseURL: https://api.modal.com\n\
  \    tags:\n      - Queues\n      - Messaging\n    serviceName: Modal Queues API\n    serviceCategory: API\n  - name: Modal Dicts API\n    baseURL: https://api.modal.com\n    tags:\n      - Dicts\n      - Key-Value Store\n    serviceName: Modal Dicts API\n    serviceCategory: API\n  - name: Modal Tunnels API\n    baseURL: https://api.modal.com\n    tags:\n      - Tunnels\n      - Networking\n    serviceName: Modal Tunnels API\n    serviceCategory: API\n  - name: Modal Environments API\n    baseURL: https://api.modal.com\n    tags:\n      - Environments\n      - Workspaces\n    serviceName: Modal Environments API\n    serviceCategory: API\n  - name: Modal Token / Workspace API\n    baseURL: https://api.modal.com\n    tags:\n      - Workspace\n      - Tokens\n      - Auth\n    serviceName: Modal Token / Workspace API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n\
  \    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/modal/refs/heads/main/finops/modal-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Serverless
- Compute
- Python
- Inference
- GPU
- FinOps
- Cost Management
- FOCUS
---
