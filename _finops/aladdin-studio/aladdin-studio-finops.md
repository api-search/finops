---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: aladdin-studio-graph-openapi.yaml
  format: yaml
  label: Aladdin Graph API
  slug: graph-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-graph-openapi.yaml
- filename: aladdin-studio-data-cloud-openapi.yaml
  format: yaml
  label: Aladdin Data Cloud API
  slug: data-cloud-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-data-cloud-openapi.yaml
- filename: aladdin-studio-trading-openapi.yaml
  format: yaml
  label: Aladdin Trading API
  slug: trading-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-trading-openapi.yaml
- filename: aladdin-studio-investment-research-openapi.yaml
  format: yaml
  label: Aladdin Investment Research API
  slug: investment-research-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/openapi/aladdin-studio-investment-research-openapi.yaml
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
description: FinOps framework definition for the Aladdin Studio API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Aladdin Studio
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Aladdin Studio
  PublisherName: Aladdin Studio
  ServiceCategory: Developer Tools / API
  ServiceName: Aladdin Studio
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
name: Aladdin Studio Finops
provider_name: Aladdin Studio
provider_slug: aladdin-studio
publisher_name: Aladdin Studio
service_category: API
slug: aladdin-studio-finops
source_filename: aladdin-studio-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Aladdin Studio\nproviderId: aladdin-studio\npublisherName: Aladdin Studio\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Financial\n  - Investment Management\n  - Portfolio Analytics\n  - Risk Management\n  - Asset Management\n  - BlackRock\n  - Data Cloud\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Aladdin Studio API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Aladdin Studio\n  ServiceCategory: Developer Tools / API\n  ProviderName: Aladdin Studio\n  PublisherName: Aladdin Studio\n  InvoiceIssuerName: Aladdin Studio\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n\
  \    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Aladdin Graph API\n    baseURL: https://api.blackrock.com/v1\n    tags:\n      - Portfolio Data\n      - Investment Management\n      - REST\n    serviceName: Aladdin Graph API\n    serviceCategory: API\n  - name: Aladdin Data Cloud API\n    baseURL: https://api.blackrock.com/adc/v1\n    tags:\n      - Data Cloud\n      - Snowflake\n      - Analytics\n    serviceName: Aladdin Data Cloud API\n    serviceCategory: API\n  - name: Aladdin Trading API\n    baseURL: https://api.blackrock.com/trading/v1\n    tags:\n      - Trading\n      - Order Management\n      - Financial\n    serviceName: Aladdin Trading\
  \ API\n    serviceCategory: API\n  - name: Aladdin Investment Research API\n    baseURL: https://api.blackrock.com/research/v1\n    tags:\n      - Investment Research\n      - Analytics\n      - Portfolio\n    serviceName: Aladdin Investment Research API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/aladdin-studio/refs/heads/main/finops/aladdin-studio-finops.yml
sources: []
specification: FinOps Framework
tags:
- Financial
- Investment Management
- Portfolio Analytics
- Risk Management
- Asset Management
- BlackRock
- Data Cloud
- FinOps
- Cost Management
- FOCUS
---
