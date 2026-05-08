---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: appdynamics-controller-rest-api-openapi.yml
  format: yaml
  label: AppDynamics Controller REST API
  slug: controller-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-controller-rest-api-openapi.yml
- filename: appdynamics-metric-and-snapshot-api-openapi.yml
  format: yaml
  label: AppDynamics Metric and Snapshot API
  slug: metric-and-snapshot-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-metric-and-snapshot-api-openapi.yml
- filename: appdynamics-alert-and-respond-api-openapi.yml
  format: yaml
  label: AppDynamics Alert and Respond API
  slug: alert-and-respond-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-alert-and-respond-api-openapi.yml
- filename: appdynamics-configuration-api-openapi.yml
  format: yaml
  label: AppDynamics Configuration API
  slug: configuration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-configuration-api-openapi.yml
- filename: appdynamics-analytics-events-api-openapi.yml
  format: yaml
  label: AppDynamics Analytics Events API
  slug: analytics-events-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-analytics-events-api-openapi.yml
- filename: appdynamics-database-agent-api-openapi.yml
  format: yaml
  label: AppDynamics Database Agent API
  slug: database-agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-database-agent-api-openapi.yml
- filename: appdynamics-machine-agent-api-openapi.yml
  format: yaml
  label: AppDynamics Machine Agent API
  slug: machine-agent-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-machine-agent-api-openapi.yml
- filename: appdynamics-cloud-observability-api-openapi.yml
  format: yaml
  label: Cisco Cloud Observability API
  slug: cloud-observability-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-cloud-observability-api-openapi.yml
- filename: appdynamics-authentication-api-openapi.yml
  format: yaml
  label: AppDynamics OAuth Authentication API
  slug: authentication-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/openapi/appdynamics-authentication-api-openapi.yml
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
description: FinOps framework definition for the AppDynamics API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AppDynamics
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AppDynamics
  PublisherName: AppDynamics
  ServiceCategory: Developer Tools / API
  ServiceName: AppDynamics
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
name: Appdynamics Finops
provider_name: AppDynamics
provider_slug: appdynamics
publisher_name: AppDynamics
service_category: API
slug: appdynamics-finops
source_filename: appdynamics-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AppDynamics\nproviderId: appdynamics\npublisherName: AppDynamics\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - APM\n  - Application Performance Monitoring\n  - Cisco\n  - Cloud Observability\n  - DevOps\n  - Monitoring\n  - Observability\n  - OpenTelemetry\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AppDynamics API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AppDynamics\n  ServiceCategory: Developer Tools / API\n  ProviderName: AppDynamics\n  PublisherName: AppDynamics\n  InvoiceIssuerName: AppDynamics\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: AppDynamics Controller REST API\n    baseURL: https://api.example.com\n    tags:\n      - Application Performance Monitoring\n      - Metrics\n      - Monitoring\n      - Observability\n      - Snapshots\n    serviceName: AppDynamics Controller REST API\n    serviceCategory: API\n  - name: AppDynamics Metric and Snapshot API\n    baseURL: https://api.example.com\n    tags:\n      - Metrics\n      - Monitoring\n      - Performance Data\n      - Snapshots\n      - Time Series\n    serviceName: AppDynamics Metric and Snapshot API\n    serviceCategory: API\n  - name: AppDynamics Alert and Respond API\n    baseURL: https://api.example.com\n\
  \    tags:\n      - Alerts\n      - Health Rules\n      - Incident Response\n      - Monitoring\n      - Notifications\n    serviceName: AppDynamics Alert and Respond API\n    serviceCategory: API\n  - name: AppDynamics Configuration API\n    baseURL: https://api.example.com\n    tags:\n      - Administration\n      - Configuration\n      - Export\n      - Import\n      - Management\n    serviceName: AppDynamics Configuration API\n    serviceCategory: API\n  - name: AppDynamics Analytics Events API\n    baseURL: https://api.example.com\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Custom Data\n      - Events\n      - Observability\n    serviceName: AppDynamics Analytics Events API\n    serviceCategory: API\n  - name: AppDynamics Database Agent API\n    baseURL: https://api.example.com\n    tags:\n      - Collectors\n      - Database\n      - Database Performance\n      - Monitoring\n    serviceName: AppDynamics Database Agent API\n    serviceCategory: API\n  - name:\
  \ AppDynamics Machine Agent API\n    baseURL: https://api.example.com\n    tags:\n      - Custom Metrics\n      - Infrastructure\n      - Metrics\n      - Server Monitoring\n    serviceName: AppDynamics Machine Agent API\n    serviceCategory: API\n  - name: Cisco Cloud Observability API\n    baseURL: https://api.example.com\n    tags:\n      - AWS\n      - Azure\n      - Cloud\n      - Connections\n      - GCP\n      - Observability\n    serviceName: Cisco Cloud Observability API\n    serviceCategory: API\n  - name: AppDynamics OAuth Authentication API\n    baseURL: https://api.example.com\n    tags:\n      - Access Tokens\n      - Authentication\n      - OAuth\n      - Security\n    serviceName: AppDynamics OAuth Authentication API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/appdynamics/refs/heads/main/finops/appdynamics-finops.yml
sources: []
specification: FinOps Framework
tags:
- APM
- Application Performance Monitoring
- Cisco
- Cloud Observability
- DevOps
- Monitoring
- Observability
- OpenTelemetry
- FinOps
- Cost Management
- FOCUS
---
