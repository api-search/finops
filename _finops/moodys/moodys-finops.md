---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: moodys-data-buffet-api-openapi.yml
  format: yaml
  label: Moody's Data Buffet API
  slug: data-buffet-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/moodys/refs/heads/main/openapi/moodys-data-buffet-api-openapi.yml
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
description: FinOps framework definition for the Moody's API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Moody's
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Moody's
  PublisherName: Moody's
  ServiceCategory: Developer Tools / API
  ServiceName: Moody's
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
name: Moodys Finops
provider_name: Moody's
provider_slug: moodys
publisher_name: Moody's
service_category: API
slug: moodys-finops
source_filename: moodys-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Moody's\nproviderId: moodys\npublisherName: Moody's\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Climate Risk\n  - Compliance\n  - Credit Risk\n  - Economic Data\n  - Entity Verification\n  - Financial Analytics\n  - Insurance\n  - KYC\n  - Risk\n  - Screening\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Moody's API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Moody's\n  ServiceCategory: Developer Tools / API\n  ProviderName: Moody's\n  PublisherName: Moody's\n  InvoiceIssuerName: Moody's\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Moody's KYC API\n    baseURL: ''\n    tags:\n      - Anti-Money Laundering\n      - Compliance\n      - Entity Verification\n      - KYC\n      - Risk\n      - Screening\n    serviceName: Moody's KYC API\n    serviceCategory: API\n  - name: Moody's Data Buffet API\n    baseURL: https://api.economy.com\n    tags:\n      - Demographics\n      - Economic Data\n      - Forecasts\n      - Time Series\n    serviceName: Moody's Data Buffet API\n    serviceCategory: API\n  - name: Moody's Scenario Studio API\n    baseURL: https://api.economy.com\n    tags:\n      - Economic Models\n      - Forecasting\n      - Macroeconomic\n      - Scenarios\n\
  \    serviceName: Moody's Scenario Studio API\n    serviceCategory: API\n  - name: Moody's AutoCycle API\n    baseURL: https://api.economy.com\n    tags:\n      - Automotive\n      - Forecasts\n      - Residual Value\n      - Vehicle Pricing\n    serviceName: Moody's AutoCycle API\n    serviceCategory: API\n  - name: Moody's Consumer Credit Loss Forecasts API\n    baseURL: https://api.economy.com\n    tags:\n      - Consumer Credit\n      - Credit Loss\n      - Forecasts\n      - Risk\n    serviceName: Moody's Consumer Credit Loss Forecasts API\n    serviceCategory: API\n  - name: Moody's Municipal Probability of Default API\n    baseURL: https://api.economy.com\n    tags:\n      - Credit Risk\n      - Forecasts\n      - Municipal\n      - Probability of Default\n    serviceName: Moody's Municipal Probability of Default API\n    serviceCategory: API\n  - name: Moody's EDF-X API\n    baseURL: https://hub.moodysanalytics.com\n    tags:\n      - Credit Risk\n      - Expected Default Frequency\n\
  \      - Probability of Default\n      - Risk Assessment\n    serviceName: Moody's EDF-X API\n    serviceCategory: API\n  - name: Moody's NewsEdge API\n    baseURL: https://hub.moodysanalytics.com\n    tags:\n      - Media\n      - News\n      - Real-Time Data\n      - Social Media\n    serviceName: Moody's NewsEdge API\n    serviceCategory: API\n  - name: Moody's QUIQSpread API\n    baseURL: https://hub.moodysanalytics.com\n    tags:\n      - Automation\n      - Banking\n      - Financial Spreading\n      - Financial Statements\n    serviceName: Moody's QUIQSpread API\n    serviceCategory: API\n  - name: Moody's Capital Risk Analyzer API\n    baseURL: https://hub.moodysanalytics.com\n    tags:\n      - Banking\n      - Capital Planning\n      - Risk\n      - Stress Testing\n    serviceName: Moody's Capital Risk Analyzer API\n    serviceCategory: API\n  - name: Moody's Climate on Demand API\n    baseURL: https://developer.rms.com\n    tags:\n      - Climate Risk\n      - Environmental\n\
  \      - Insurance\n      - Physical Risk\n    serviceName: Moody's Climate on Demand API\n    serviceCategory: API\n  - name: Moody's Location Intelligence API\n    baseURL: https://developer.rms.com\n    tags:\n      - Geospatial\n      - Insurance\n      - Location\n      - Risk Data\n    serviceName: Moody's Location Intelligence API\n    serviceCategory: API\n  - name: Moody's Risk Modeler API\n    baseURL: https://developer.rms.com\n    tags:\n      - Catastrophe Modeling\n      - Insurance\n      - Risk\n      - Underwriting\n    serviceName: Moody's Risk Modeler API\n    serviceCategory: API\n  - name: Moody's Intelligent Risk Platform API\n    baseURL: https://developer.rms.com\n    tags:\n      - Insurance\n      - Platform\n      - Reinsurance\n      - Risk Management\n    serviceName: Moody's Intelligent Risk Platform API\n    serviceCategory: API\n  - name: Moody's Commercial Real Estate API\n    baseURL: https://hub.moodysanalytics.com\n    tags:\n      - Commercial Real\
  \ Estate\n      - CRE\n      - Location Score\n      - Property\n    serviceName: Moody's Commercial Real Estate API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/moodys/refs/heads/main/finops/moodys-finops.yml
sources: []
specification: FinOps Framework
tags:
- Climate Risk
- Compliance
- Credit Risk
- Economic Data
- Entity Verification
- Financial Analytics
- Insurance
- KYC
- Risk
- Screening
- FinOps
- Cost Management
- FOCUS
---
