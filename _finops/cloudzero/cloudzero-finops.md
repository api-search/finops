---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: cloudzero-api-openapi.yml
  format: yaml
  label: CloudZero API
  slug: api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/openapi/cloudzero-api-openapi.yml
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
description: FinOps framework definition for the CloudZero API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: CloudZero
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: CloudZero
  PublisherName: CloudZero
  ServiceCategory: Developer Tools / API
  ServiceName: CloudZero
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
name: Cloudzero Finops
provider_name: CloudZero
provider_slug: cloudzero
publisher_name: CloudZero
service_category: API
slug: cloudzero-finops
source_filename: cloudzero-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: CloudZero\nproviderId: cloudzero\npublisherName: CloudZero\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Budgets\n  - Cloud Cost Management\n  - Cost Allocation\n  - Cost Optimization\n  - FinOps\n  - Telemetry\n  - Unit Economics\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the CloudZero API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: CloudZero\n  ServiceCategory: Developer Tools / API\n  ProviderName: CloudZero\n  PublisherName: CloudZero\n  InvoiceIssuerName: CloudZero\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: CloudZero API\n    baseURL: https://api.cloudzero.com\n    tags:\n      - Billing\n      - Budgets\n      - Cloud Costs\n      - Cost Allocation\n      - FinOps\n      - Insights\n      - Telemetry\n      - Unit Economics\n    serviceName: CloudZero API\n    serviceCategory: API\n  - name: CloudZero Billing API\n    baseURL: https://api.cloudzero.com/v2/billing\n    tags:\n      - Billing\n      - Cost Reporting\n      - Dimensions\n    serviceName: CloudZero Billing API\n    serviceCategory: API\n  - name: CloudZero Insights API\n    baseURL: https://api.cloudzero.com/v2/insights\n    tags:\n      - Cost Optimization\n      - Insights\n      - Recommendations\n\
  \    serviceName: CloudZero Insights API\n    serviceCategory: API\n  - name: CloudZero Budgets API\n    baseURL: https://api.cloudzero.com/v2/budgets\n    tags:\n      - Alerts\n      - Budgets\n      - FinOps\n    serviceName: CloudZero Budgets API\n    serviceCategory: API\n  - name: CloudZero Allocation Telemetry API\n    baseURL: https://api.cloudzero.com/v1/telemetry/allocation\n    tags:\n      - Allocation\n      - Cost Splitting\n      - Telemetry\n    serviceName: CloudZero Allocation Telemetry API\n    serviceCategory: API\n  - name: CloudZero Unit Metric Telemetry API\n    baseURL: https://api.cloudzero.com/v1/telemetry\n    tags:\n      - Telemetry\n      - Unit Economics\n      - Unit Metrics\n    serviceName: CloudZero Unit Metric Telemetry API\n    serviceCategory: API\n  - name: CloudZero AnyCost API\n    baseURL: https://api.cloudzero.com/v2/connections/billing/anycost\n    tags:\n      - AnyCost\n      - Billing Drop\n      - CBF\n      - Common Bill Format\n      -\
  \ Ingestion\n    serviceName: CloudZero AnyCost API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudzero/refs/heads/main/finops/cloudzero-finops.yml
sources: []
specification: FinOps Framework
tags:
- Budgets
- Cloud Cost Management
- Cost Allocation
- Cost Optimization
- FinOps
- Telemetry
- Unit Economics
- FinOps
- Cost Management
- FOCUS
---
