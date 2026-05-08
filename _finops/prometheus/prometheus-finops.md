---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: prometheus-http-api-openapi.yml
  format: yaml
  label: Prometheus HTTP API
  slug: prometheus-http-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-http-api-openapi.yml
- filename: prometheus-management-api-openapi.yml
  format: yaml
  label: Prometheus Management API
  slug: prometheus-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-management-api-openapi.yml
- filename: prometheus-pushgateway-api-openapi.yml
  format: yaml
  label: Prometheus Pushgateway API
  slug: prometheus-pushgateway-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-pushgateway-api-openapi.yml
- filename: prometheus-alertmanager-api-openapi.yml
  format: yaml
  label: Prometheus Alertmanager API
  slug: prometheus-alertmanager-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/openapi/prometheus-alertmanager-api-openapi.yml
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
description: FinOps framework definition for the Prometheus API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Prometheus
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Prometheus
  PublisherName: Prometheus
  ServiceCategory: Developer Tools / API
  ServiceName: Prometheus
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
name: Prometheus Finops
provider_name: Prometheus
provider_slug: prometheus
publisher_name: Prometheus
service_category: API
slug: prometheus-finops
source_filename: prometheus-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Prometheus\nproviderId: prometheus\npublisherName: Prometheus\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Alerting\n  - Metrics\n  - Monitoring\n  - Observability\n  - Time Series\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Prometheus API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Prometheus\n  ServiceCategory: Developer Tools / API\n  ProviderName: Prometheus\n  PublisherName: Prometheus\n  InvoiceIssuerName: Prometheus\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Prometheus HTTP API\n    baseURL: ''\n    tags:\n      - Metrics\n      - PromQL\n      - Query\n      - Time Series\n    serviceName: Prometheus HTTP API\n    serviceCategory: API\n  - name: Prometheus Management API\n    baseURL: ''\n    tags:\n      - Administration\n      - Management\n      - Monitoring\n    serviceName: Prometheus Management API\n    serviceCategory: API\n  - name: Prometheus Pushgateway API\n    baseURL: ''\n    tags:\n      - Batch Jobs\n      - Metrics\n      - Pushgateway\n    serviceName: Prometheus Pushgateway API\n    serviceCategory: API\n  - name: Prometheus Alertmanager API\n    baseURL: ''\n    tags:\n      - Alerting\n      - Notifications\n      - Silences\n\
  \    serviceName: Prometheus Alertmanager API\n    serviceCategory: API\n  - name: Prometheus Remote Write API\n    baseURL: ''\n    tags:\n      - Integration\n      - Remote Write\n      - Storage\n      - Time Series\n    serviceName: Prometheus Remote Write API\n    serviceCategory: API\n  - name: Prometheus Client Libraries\n    baseURL: ''\n    tags:\n      - Client Libraries\n      - Instrumentation\n      - Metrics\n      - SDK\n    serviceName: Prometheus Client Libraries\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/prometheus/refs/heads/main/finops/prometheus-finops.yml
sources: []
specification: FinOps Framework
tags:
- Alerting
- Metrics
- Monitoring
- Observability
- Time Series
- FinOps
- Cost Management
- FOCUS
---
