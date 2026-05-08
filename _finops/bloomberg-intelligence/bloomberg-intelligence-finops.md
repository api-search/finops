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
description: FinOps framework definition for the Bloomberg Intelligence API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bloomberg Intelligence
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bloomberg Intelligence
  PublisherName: Bloomberg Intelligence
  ServiceCategory: Developer Tools / API
  ServiceName: Bloomberg Intelligence
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
name: Bloomberg Intelligence Finops
provider_name: Bloomberg Intelligence
provider_slug: bloomberg-intelligence
publisher_name: Bloomberg Intelligence
service_category: API
slug: bloomberg-intelligence-finops
source_filename: bloomberg-intelligence-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bloomberg Intelligence\nproviderId: bloomberg-intelligence\npublisherName: Bloomberg Intelligence\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Company Analysis\n  - Credit Research\n  - ESG Data\n  - Financial Data\n  - Financial Research\n  - Market Data\n  - Market Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bloomberg Intelligence API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bloomberg Intelligence\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bloomberg Intelligence\n  PublisherName: Bloomberg Intelligence\n  InvoiceIssuerName: Bloomberg Intelligence\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bloomberg Open API (BLPAPI)\n    baseURL: blpapi://localhost:8194\n    tags:\n      - Core API\n      - Market Data\n      - Real-Time Data\n      - Reference Data\n    serviceName: Bloomberg Open API (BLPAPI)\n    serviceCategory: API\n  - name: Bloomberg Query Language (BQL)\n    baseURL: bql://bloomberg.com\n    tags:\n      - Analytics\n      - Data Query\n      - Query Language\n    serviceName: Bloomberg Query Language (BQL)\n    serviceCategory: API\n  - name: Bloomberg Data License API\n    baseURL: https://dlws.bloomberg.com\n\
  \    tags:\n      - Bulk Data\n      - Data License\n      - Enterprise\n      - SFTP\n      - SOAP\n    serviceName: Bloomberg Data License API\n    serviceCategory: API\n  - name: Bloomberg Server API (SAPI)\n    baseURL: blpapi://server:8194\n    tags:\n      - B-PIPE\n      - Enterprise\n      - High Performance\n      - Server API\n    serviceName: Bloomberg Server API (SAPI)\n    serviceCategory: API\n  - name: Bloomberg Intelligence Research API\n    baseURL: https://api.bloomberg.com/intelligence\n    tags:\n      - Analysis\n      - ESG\n      - Industry Research\n      - Reports\n      - Research\n    serviceName: Bloomberg Intelligence Research API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-intelligence/refs/heads/main/finops/bloomberg-intelligence-finops.yml
sources: []
specification: FinOps Framework
tags:
- Company Analysis
- Credit Research
- ESG Data
- Financial Data
- Financial Research
- Market Data
- Market Intelligence
- FinOps
- Cost Management
- FOCUS
---
