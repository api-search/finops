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
description: FinOps framework definition for the Celery API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Celery
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Celery
  PublisherName: Celery
  ServiceCategory: Developer Tools / API
  ServiceName: Celery
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
name: Celery Finops
provider_name: Celery
provider_slug: celery
publisher_name: Celery
service_category: API
slug: celery-finops
source_filename: celery-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Celery\nproviderId: celery\npublisherName: Celery\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Asynchronous\n  - Distributed Systems\n  - Message Queue\n  - Open Source\n  - Python\n  - Task Queue\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Celery API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Celery\n  ServiceCategory: Developer Tools / API\n  ProviderName: Celery\n  PublisherName: Celery\n  InvoiceIssuerName: Celery\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Celery Task API\n    baseURL: ''\n    tags:\n      - Python\n      - Task Queue\n      - Tasks\n    serviceName: Celery Task API\n    serviceCategory: API\n  - name: Celery Application API\n    baseURL: ''\n    tags:\n      - Application\n      - Configuration\n    serviceName: Celery Application API\n    serviceCategory: API\n  - name: Celery Canvas API\n    baseURL: ''\n    tags:\n      - Workflows\n      - Chains\n      - Groups\n      - Chords\n    serviceName: Celery Canvas API\n    serviceCategory: API\n  - name: Celery Beat API\n    baseURL: ''\n    tags:\n      - Scheduling\n      - Periodic Tasks\n    serviceName: Celery Beat API\n    serviceCategory: API\n  - name: Celery Worker API\n\
  \    baseURL: ''\n    tags:\n      - Worker\n      - Execution\n      - Concurrency\n    serviceName: Celery Worker API\n    serviceCategory: API\n  - name: Celery Result Backend API\n    baseURL: ''\n    tags:\n      - Results\n      - State\n      - Storage\n    serviceName: Celery Result Backend API\n    serviceCategory: API\n  - name: Celery Signals API\n    baseURL: ''\n    tags:\n      - Signals\n      - Events\n      - Extensions\n    serviceName: Celery Signals API\n    serviceCategory: API\n  - name: Celery Monitoring and Events API\n    baseURL: ''\n    tags:\n      - Monitoring\n      - Events\n      - Observability\n    serviceName: Celery Monitoring and Events API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/celery/refs/heads/main/finops/celery-finops.yml
sources: []
specification: FinOps Framework
tags:
- Asynchronous
- Distributed Systems
- Message Queue
- Open Source
- Python
- Task Queue
- FinOps
- Cost Management
- FOCUS
---
