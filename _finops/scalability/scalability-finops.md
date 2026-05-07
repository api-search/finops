---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: KEDA (Kubernetes Event-Driven Autoscaling) API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/kedacore/keda/main/apis/keda/v1alpha1/
- filename: openapi.yaml
  format: yaml
  label: AWS Auto Scaling API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/amazonaws.com/autoscaling/2011-01-01/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Google Cloud Compute Engine Autoscaler API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/googleapis.com/compute/v1/openapi.yaml
- filename: autoScale_API.json
  format: json
  label: Azure Autoscale REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/Azure/azure-rest-api-specs/main/specification/monitor/resource-manager/Microsoft.Insights/stable/2022-10-01/autoScale_API.json
- filename: openapi.yaml
  format: yaml
  label: CloudWatch Application Signals API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/APIs-guru/openapi-directory/main/APIs/amazonaws.com/monitoring/2010-08-01/openapi.yaml
- filename: api.go
  format: yaml
  label: Prometheus HTTP API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/prometheus/prometheus/main/web/api/v1/api.go
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
description: FinOps framework definition for the Scalability API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalability
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalability
  PublisherName: Scalability
  ServiceCategory: Developer Tools / API
  ServiceName: Scalability
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
name: Scalability Finops
provider_name: Scalability
provider_slug: scalability
publisher_name: Scalability
service_category: API
slug: scalability-finops
source_filename: scalability-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalability\nproviderId: scalability\npublisherName: Scalability\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Auto Scaling\n  - Cloud Computing\n  - DevOps\n  - Distributed Systems\n  - Elasticity\n  - High Availability\n  - Infrastructure\n  - Load Balancing\n  - Performance\n  - Scalability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalability API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalability\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalability\n  PublisherName: Scalability\n  InvoiceIssuerName: Scalability\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: KEDA (Kubernetes Event-Driven Autoscaling) API\n    baseURL: ''\n    tags:\n      - Auto Scaling\n      - CNCF\n      - Event-Driven\n      - Kubernetes\n      - Scale To Zero\n    serviceName: KEDA (Kubernetes Event-Driven Autoscaling) API\n    serviceCategory: API\n  - name: AWS Auto Scaling API\n    baseURL: ''\n    tags:\n      - Amazon Web Services\n      - Auto Scaling\n      - Cloud\n      - EC2\n      - Elasticity\n    serviceName: AWS Auto Scaling API\n    serviceCategory: API\n  - name: Google Cloud Compute Engine Autoscaler API\n    baseURL: ''\n    tags:\n      - Auto\
  \ Scaling\n      - Cloud\n      - GKE\n      - Google Cloud\n      - Instance Groups\n    serviceName: Google Cloud Compute Engine Autoscaler API\n    serviceCategory: API\n  - name: Azure Autoscale REST API\n    baseURL: ''\n    tags:\n      - Auto Scaling\n      - Azure\n      - Cloud\n      - Microsoft\n      - Virtual Machine Scale Sets\n    serviceName: Azure Autoscale REST API\n    serviceCategory: API\n  - name: CloudWatch Application Signals API\n    baseURL: ''\n    tags:\n      - Amazon Web Services\n      - Observability\n      - APM\n      - Monitoring\n      - Performance\n    serviceName: CloudWatch Application Signals API\n    serviceCategory: API\n  - name: Prometheus HTTP API\n    baseURL: ''\n    tags:\n      - CNCF\n      - Metrics\n      - Monitoring\n      - Observability\n      - Open Source\n      - Prometheus\n      - Time Series\n    serviceName: Prometheus HTTP API\n    serviceCategory: API\n  - name: Grafana HTTP API\n    baseURL: ''\n    tags:\n      - Dashboards\n\
  \      - Grafana\n      - Metrics\n      - Monitoring\n      - Observability\n      - Open Source\n    serviceName: Grafana HTTP API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalability/refs/heads/main/finops/scalability-finops.yml
sources: []
specification: FinOps Framework
tags:
- Auto Scaling
- Cloud Computing
- DevOps
- Distributed Systems
- Elasticity
- High Availability
- Infrastructure
- Load Balancing
- Performance
- Scalability
- FinOps
- Cost Management
- FOCUS
---
