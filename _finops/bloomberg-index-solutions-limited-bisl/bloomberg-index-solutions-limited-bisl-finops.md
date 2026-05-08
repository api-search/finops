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
description: FinOps framework definition for the Bloomberg Index Solutions Limited (BISL) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Bloomberg Index Solutions Limited (BISL)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Bloomberg Index Solutions Limited (BISL)
  PublisherName: Bloomberg Index Solutions Limited (BISL)
  ServiceCategory: Developer Tools / API
  ServiceName: Bloomberg Index Solutions Limited (BISL)
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
name: Bloomberg Index Solutions Limited Bisl Finops
provider_name: Bloomberg Index Solutions Limited (BISL)
provider_slug: bloomberg-index-solutions-limited-bisl
publisher_name: Bloomberg Index Solutions Limited (BISL)
service_category: API
slug: bloomberg-index-solutions-limited-bisl-finops
source_filename: bloomberg-index-solutions-limited-bisl-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Bloomberg Index Solutions Limited (BISL)\nproviderId: bloomberg-index-solutions-limited-bisl\npublisherName: Bloomberg Index Solutions Limited (BISL)\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Index\n  - Fixed Income\n  - Benchmark\n  - Multi-Asset\n  - Index Administration\n  - Bloomberg\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Bloomberg Index Solutions Limited (BISL) API surface.\n  Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting\n  across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible\
  \ to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Bloomberg Index Solutions Limited (BISL)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Bloomberg Index Solutions Limited (BISL)\n  PublisherName: Bloomberg Index Solutions Limited (BISL)\n  InvoiceIssuerName: Bloomberg Index Solutions Limited (BISL)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API\
  \ requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Bloomberg Index Data API\n    baseURL: blpapi://localhost:8194\n    tags:\n      - Index Data\n      - Fixed Income\n      - Returns\n      - Constituents\n    serviceName: Bloomberg Index Data API\n    serviceCategory: API\n  - name: Bloomberg Index Licensing\n    baseURL: https://indices.bloomberg.com\n    tags:\n      - Index Licensing\n      - ETF\n      - Benchmark Regulation\n      - BMR\n    serviceName: Bloomberg Index Licensing\n\
  \    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kinlane@gmail.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/bloomberg-index-solutions-limited-bisl/refs/heads/main/finops/bloomberg-index-solutions-limited-bisl-finops.yml
sources: []
specification: FinOps Framework
tags:
- Index
- Fixed Income
- Benchmark
- Multi-Asset
- Index Administration
- Bloomberg
- FinOps
- Cost Management
- FOCUS
---
