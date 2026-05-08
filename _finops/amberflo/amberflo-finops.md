---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amberflo-metering-openapi.yaml
  format: yaml
  label: Amberflo Metering API
  slug: metering-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amberflo/refs/heads/main/openapi/amberflo-metering-openapi.yaml
- filename: amberflo-billing-openapi.yaml
  format: yaml
  label: Amberflo Billing API
  slug: billing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amberflo/refs/heads/main/openapi/amberflo-billing-openapi.yaml
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
description: FinOps framework definition for the Amberflo API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amberflo
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amberflo
  PublisherName: Amberflo
  ServiceCategory: Developer Tools / API
  ServiceName: Amberflo
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
name: Amberflo Finops
provider_name: Amberflo
provider_slug: amberflo
publisher_name: Amberflo
service_category: API
slug: amberflo-finops
source_filename: amberflo-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amberflo\nproviderId: amberflo\npublisherName: Amberflo\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Usage-Based Billing\n  - Metering\n  - FinOps\n  - AI Cost Management\n  - Billing\n  - Monetization\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amberflo API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amberflo\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amberflo\n  PublisherName: Amberflo\n  InvoiceIssuerName: Amberflo\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amberflo Metering API\n    baseURL: https://app.amberflo.io\n    tags:\n      - Metering\n      - Event Ingestion\n      - Usage Tracking\n    serviceName: Amberflo Metering API\n    serviceCategory: API\n  - name: Amberflo Billing API\n    baseURL: https://app.amberflo.io\n    tags:\n      - Billing\n      - Customers\n      - Invoicing\n      - Pricing Plans\n    serviceName: Amberflo Billing API\n    serviceCategory: API\n  - name: Amberflo Cost Tracking API\n    baseURL: https://app.amberflo.io\n    tags:\n      - Cost Tracking\n      - FinOps\n      - Cloud Cost Management\n      - Budgets\n    serviceName: Amberflo Cost Tracking API\n    serviceCategory: API\n  - name: Amberflo AI Gateway\
  \ API\n    baseURL: https://app.amberflo.io\n    tags:\n      - AI Gateway\n      - LLM\n      - Model Routing\n      - AI Cost Management\n    serviceName: Amberflo AI Gateway API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amberflo/refs/heads/main/finops/amberflo-finops.yml
sources: []
specification: FinOps Framework
tags:
- Usage-Based Billing
- Metering
- FinOps
- AI Cost Management
- Billing
- Monetization
- FinOps
- Cost Management
- FOCUS
---
