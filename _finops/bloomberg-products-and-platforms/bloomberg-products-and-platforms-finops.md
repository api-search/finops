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
description: FinOps framework definition for the Bloomberg Products and Platforms API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bloomberg Products and Platforms
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bloomberg Products and Platforms
  PublisherName: Bloomberg Products and Platforms
  ServiceCategory: Developer Tools / API
  ServiceName: Bloomberg Products and Platforms
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
name: Bloomberg Products And Platforms Finops
provider_name: Bloomberg Products and Platforms
provider_slug: bloomberg-products-and-platforms
publisher_name: Bloomberg Products and Platforms
service_category: API
slug: bloomberg-products-and-platforms-finops
source_filename: bloomberg-products-and-platforms-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bloomberg Products and Platforms\nproviderId: bloomberg-products-and-platforms\npublisherName: Bloomberg Products and Platforms\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Products\n  - Platforms\n  - Terminal\n  - Enterprise\n  - Financial Data\n  - Analytics\n  - Bloomberg\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bloomberg Products and Platforms API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product,\
  \ and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n     \
  \ - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bloomberg Products and Platforms\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bloomberg Products and Platforms\n  PublisherName: Bloomberg Products and Platforms\n  InvoiceIssuerName: Bloomberg Products and Platforms\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bloomberg Open API (BLPAPI)\n    baseURL: blpapi://localhost:8194\n    tags:\n      - Core API\n      - Cross-Platform\n      - Market Data\n    serviceName: Bloomberg Open API (BLPAPI)\n    serviceCategory: API\n  - name: Bloomberg B-PIPE\n    baseURL: blpapi://bpipe-server:8194\n    tags:\n      - B-PIPE\n      - Enterprise\n      - Data Distribution\n    serviceName: Bloomberg B-PIPE\n    serviceCategory: API\n  - name: Bloomberg EMSX (Electronic Order Management)\n    baseURL: blpapi://localhost:8194\n\
  \    tags:\n      - EMSX\n      - Order Management\n      - FIX\n      - Electronic Trading\n    serviceName: Bloomberg EMSX (Electronic Order Management)\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-products-and-platforms/refs/heads/main/finops/bloomberg-products-and-platforms-finops.yml
sources: []
specification: FinOps Framework
tags:
- Products
- Platforms
- Terminal
- Enterprise
- Financial Data
- Analytics
- Bloomberg
- FinOps
- Cost Management
- FOCUS
---
