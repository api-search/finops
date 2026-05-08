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
  label: Temenos Transact Core Banking API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/transact/openapi.json
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
description: FinOps framework definition for the Temenos Transact API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Temenos Transact
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Temenos Transact
  PublisherName: Temenos Transact
  ServiceCategory: Developer Tools / API
  ServiceName: Temenos Transact
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
name: Temenos Transact Finops
provider_name: Temenos Transact
provider_slug: temenos-transact
publisher_name: Temenos Transact
service_category: API
slug: temenos-transact-finops
source_filename: temenos-transact-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Temenos Transact\nproviderId: temenos-transact\npublisherName: Temenos Transact\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Core Banking\n  - Digital Banking\n  - Enterprise\n  - Financial Services\n  - Fintech\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Temenos Transact API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Temenos Transact\n  ServiceCategory: Developer Tools / API\n  ProviderName: Temenos Transact\n  PublisherName: Temenos Transact\n  InvoiceIssuerName: Temenos Transact\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Temenos Transact Core Banking API\n    baseURL: https://api.temenos.com/transact/v1\n    tags:\n      - Accounts\n      - Banking\n      - Core Banking\n      - Customers\n      - Payments\n      - Transactions\n    serviceName: Temenos Transact Core Banking API\n    serviceCategory: API\n  - name: Temenos Transact Microservices APIs\n    baseURL: https://api.temenos.com/transact/v1\n    tags:\n      - Configuration\n      - Entitlements\n      - Microservices\n      - Orchestration\n    serviceName: Temenos Transact Microservices APIs\n    serviceCategory: API\n  - name: Temenos Transact Data Hub APIs\n    baseURL:\
  \ https://api.temenos.com/transact/v1\n    tags:\n      - Analytics\n      - Data Hub\n      - Data Store\n      - Reporting\n    serviceName: Temenos Transact Data Hub APIs\n    serviceCategory: API\n  - name: Temenos Operational Data Store APIs\n    baseURL: https://api.temenos.com/transact/v1\n    tags:\n      - Data Streams\n      - ETL\n      - Operational Data\n      - Real-Time\n    serviceName: Temenos Operational Data Store APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/temenos-transact/refs/heads/main/finops/temenos-transact-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Core Banking
- Digital Banking
- Enterprise
- Financial Services
- Fintech
- FinOps
- Cost Management
- FOCUS
---
