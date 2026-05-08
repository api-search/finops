---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: circana-liquid-data.yaml
  format: yaml
  label: Circana Liquid Data API
  slug: liquid-data-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/circana/refs/heads/main/openapi/circana-liquid-data.yaml
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
description: FinOps framework definition for the Circana API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Circana
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Circana
  PublisherName: Circana
  ServiceCategory: Developer Tools / API
  ServiceName: Circana
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
name: Circana Finops
provider_name: Circana
provider_slug: circana
publisher_name: Circana
service_category: API
slug: circana-finops
source_filename: circana-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Circana\nproviderId: circana\npublisherName: Circana\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Consumer Data\n  - Market Research\n  - Retail\n  - CPG\n  - Point Of Sale\n  - Consumer Insights\n  - Business Intelligence\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Circana API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Circana\n  ServiceCategory: Developer Tools / API\n  ProviderName: Circana\n  PublisherName: Circana\n  InvoiceIssuerName: Circana\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in\
  \ API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Circana Unify+ API\n    baseURL: ''\n    tags:\n      - Business Intelligence\n      - Data Visualization\n      - Analytics\n      - Reporting\n    serviceName: Circana Unify+ API\n    serviceCategory: API\n  - name: Circana Liquid Data API\n    baseURL: ''\n    tags:\n      - Data Platform\n      - Analytics\n      - Cloud\n      - Data Integration\n    serviceName: Circana Liquid Data API\n    serviceCategory: API\n  - name: Circana Liquid Data Go API\n    baseURL: ''\n    tags:\n      - Market Intelligence\n      - CPG\n      - Analytics\n      - Emerging Brands\n    serviceName: Circana Liquid Data Go API\n    serviceCategory: API\n  - name: Circana\
  \ Intelligence Suite API\n    baseURL: ''\n    tags:\n      - Data Integration\n      - Automation\n      - Data Harmonization\n      - Cloud\n    serviceName: Circana Intelligence Suite API\n    serviceCategory: API\n  - name: Circana Complete Market API\n    baseURL: ''\n    tags:\n      - Point Of Sale\n      - Market Measurement\n      - Retail Analytics\n    serviceName: Circana Complete Market API\n    serviceCategory: API\n  - name: Circana Complete Consumer API\n    baseURL: ''\n    tags:\n      - Consumer Panel\n      - Shopper Insights\n      - Purchase Data\n    serviceName: Circana Complete Consumer API\n    serviceCategory: API\n  - name: Circana Complete Beauty API\n    baseURL: ''\n    tags:\n      - Beauty\n      - Market Data\n      - Prestige\n      - Mass Market\n    serviceName: Circana Complete Beauty API\n    serviceCategory: API\n  - name: Circana Complete Food and Beverage API\n    baseURL: ''\n    tags:\n      - Food\n      - Beverage\n      - Foodservice\n   \
  \   - CPG\n    serviceName: Circana Complete Food and Beverage API\n    serviceCategory: API\n  - name: Circana Liquid Data Collaborate API\n    baseURL: ''\n    tags:\n      - Data Collaboration\n      - Retail Analytics\n      - AI\n    serviceName: Circana Liquid Data Collaborate API\n    serviceCategory: API\n  - name: Circana Liquid Data Engage API\n    baseURL: ''\n    tags:\n      - Retail Strategy\n      - Customer Analytics\n      - Data Precision\n    serviceName: Circana Liquid Data Engage API\n    serviceCategory: API\n  - name: Circana Liquid Activation API\n    baseURL: ''\n    tags:\n      - Audience Activation\n      - Marketing\n      - Advertising\n    serviceName: Circana Liquid Activation API\n    serviceCategory: API\n  - name: Circana Price and Promotion API\n    baseURL: ''\n    tags:\n      - Pricing\n      - Promotion\n      - Trade Optimization\n      - Forecasting\n    serviceName: Circana Price and Promotion API\n    serviceCategory: API\n  - name: Circana Retail\
  \ Media API\n    baseURL: ''\n    tags:\n      - Retail Media\n      - Advertising\n      - ROAS\n      - Media Analytics\n    serviceName: Circana Retail Media API\n    serviceCategory: API\n  - name: Circana Complete Why Analytics API\n    baseURL: ''\n    tags:\n      - AI Analytics\n      - Sales Performance\n      - Diagnostics\n    serviceName: Circana Complete Why Analytics API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/circana/refs/heads/main/finops/circana-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Consumer Data
- Market Research
- Retail
- CPG
- Point Of Sale
- Consumer Insights
- Business Intelligence
- FinOps
- Cost Management
- FOCUS
---
