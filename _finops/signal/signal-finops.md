---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: signal-server-openapi.yml
  format: yaml
  label: Signal Server
  slug: signal-server
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/signal/refs/heads/main/openapi/signal-server-openapi.yml
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
description: FinOps framework definition for the Signal API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Signal
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Signal
  PublisherName: Signal
  ServiceCategory: Developer Tools / API
  ServiceName: Signal
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
name: Signal Finops
provider_name: Signal
provider_slug: signal
publisher_name: Signal
service_category: API
slug: signal-finops
source_filename: signal-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Signal\nproviderId: signal\npublisherName: Signal\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Encryption\n  - Messaging\n  - Security\n  - Cryptography\n  - Open Source\n  - Privacy\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Signal API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Signal\n  ServiceCategory: Developer Tools / API\n  ProviderName: Signal\n  PublisherName: Signal\n  InvoiceIssuerName: Signal\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Signal Protocol Specifications\n    baseURL: ''\n    tags:\n      - Encryption\n      - Messaging\n      - Cryptography\n      - Security\n      - Protocols\n    serviceName: Signal Protocol Specifications\n    serviceCategory: API\n  - name: Signal libsignal SDK\n    baseURL: ''\n    tags:\n      - SDK\n      - Encryption\n      - Cryptography\n      - Java\n      - Swift\n      - TypeScript\n      - Rust\n    serviceName: Signal libsignal SDK\n    serviceCategory: API\n  - name: Signal Server\n    baseURL: https://chat.signal.org\n    tags:\n      - Messaging\n      - Server\n      - Backend\n      - Encryption\n      - Open Source\n    serviceName: Signal Server\n    serviceCategory: API\n  - name: Signal Android\
  \ SDK\n    baseURL: ''\n    tags:\n      - Android\n      - Mobile\n      - Messaging\n      - Encryption\n      - Open Source\n    serviceName: Signal Android SDK\n    serviceCategory: API\n  - name: Signal iOS SDK\n    baseURL: ''\n    tags:\n      - iOS\n      - Mobile\n      - Messaging\n      - Encryption\n      - Open Source\n    serviceName: Signal iOS SDK\n    serviceCategory: API\n  - name: Signal Desktop SDK\n    baseURL: ''\n    tags:\n      - Desktop\n      - Electron\n      - Messaging\n      - Encryption\n      - Open Source\n    serviceName: Signal Desktop SDK\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/signal/refs/heads/main/finops/signal-finops.yml
sources: []
specification: FinOps Framework
tags:
- Encryption
- Messaging
- Security
- Cryptography
- Open Source
- Privacy
- FinOps
- Cost Management
- FOCUS
---
