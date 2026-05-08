---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: kubecost-allocation-openapi.yml
  format: yaml
  label: Kubecost Allocation API
  slug: allocation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-allocation-openapi.yml
- filename: kubecost-assets-openapi.yml
  format: yaml
  label: Kubecost Assets API
  slug: assets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-assets-openapi.yml
- filename: kubecost-cloud-cost-openapi.yml
  format: yaml
  label: Kubecost Cloud Cost API
  slug: cloud-cost-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-cloud-cost-openapi.yml
- filename: kubecost-budget-openapi.yml
  format: yaml
  label: Kubecost Budget API
  slug: budget-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-budget-openapi.yml
- filename: kubecost-forecast-openapi.yml
  format: yaml
  label: Kubecost Forecast API
  slug: forecast-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-forecast-openapi.yml
- filename: kubecost-savings-openapi.yml
  format: yaml
  label: Kubecost Savings API
  slug: savings-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/openapi/kubecost-savings-openapi.yml
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
description: FinOps framework definition for the Kubecost API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Kubecost
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Kubecost
  PublisherName: Kubecost
  ServiceCategory: Developer Tools / API
  ServiceName: Kubecost
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
name: Kubecost Finops
provider_name: Kubecost
provider_slug: kubecost
publisher_name: Kubecost
service_category: API
slug: kubecost-finops
source_filename: kubecost-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Kubecost\nproviderId: kubecost\npublisherName: Kubecost\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Cost\n  - Cost Monitoring\n  - Kubernetes\n  - Optimization\n  - Spending\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Kubecost API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Kubecost\n  ServiceCategory: Developer Tools / API\n  ProviderName: Kubecost\n  PublisherName: Kubecost\n  InvoiceIssuerName: Kubecost\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Kubecost Allocation API\n    baseURL: ''\n    tags:\n      - Cost Allocation\n      - Kubernetes\n      - Monitoring\n    serviceName: Kubecost Allocation API\n    serviceCategory: API\n  - name: Kubecost Assets API\n    baseURL: ''\n    tags:\n      - Assets\n      - Kubernetes\n      - Monitoring\n    serviceName: Kubecost Assets API\n    serviceCategory: API\n  - name: Kubecost Cloud Cost API\n    baseURL: ''\n    tags:\n      - AWS\n      - Azure\n      - Cloud Cost\n      - GCP\n      - Monitoring\n    serviceName: Kubecost Cloud Cost API\n    serviceCategory: API\n  - name: Kubecost Budget API\n    baseURL: ''\n    tags:\n      - Budget\n      - Governance\n      - Spending\n    serviceName: Kubecost\
  \ Budget API\n    serviceCategory: API\n  - name: Kubecost Forecast API\n    baseURL: ''\n    tags:\n      - Cost Prediction\n      - Forecast\n      - Governance\n    serviceName: Kubecost Forecast API\n    serviceCategory: API\n  - name: Kubecost Savings API\n    baseURL: ''\n    tags:\n      - Optimization\n      - Right-Sizing\n      - Savings\n    serviceName: Kubecost Savings API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kubecost/refs/heads/main/finops/kubecost-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Cost
- Cost Monitoring
- Kubernetes
- Optimization
- Spending
- FinOps
- Cost Management
- FOCUS
---
