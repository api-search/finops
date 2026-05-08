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
  label: Amazon CloudWatch API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/monitoring/2010-08-01/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Logs API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/logs/2014-03-28/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Events API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/events/2015-10-07/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Application Insights API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/application-insights/2018-11-25/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Synthetics API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/synthetics/2017-10-11/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Internet Monitor API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/internetmonitor/2021-06-03/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch RUM API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/rum/2018-05-10/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Amazon CloudWatch Observability Access Manager API
  slug: ''
  spec_type: OpenAPI
  url: https://api.apis.guru/v2/specs/amazonaws.com/oam/2022-06-10/openapi.yaml
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
description: FinOps framework definition for the AWS CloudWatch API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: AWS CloudWatch
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: AWS CloudWatch
  PublisherName: AWS CloudWatch
  ServiceCategory: Developer Tools / API
  ServiceName: AWS CloudWatch
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
name: Cloudwatch Finops
provider_name: AWS CloudWatch
provider_slug: cloudwatch
publisher_name: AWS CloudWatch
service_category: API
slug: cloudwatch-finops
source_filename: cloudwatch-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: AWS CloudWatch\nproviderId: cloudwatch\npublisherName: AWS CloudWatch\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Alarms\n  - Aws\n  - Dashboards\n  - Logs\n  - Metrics\n  - Monitoring\n  - Observability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the AWS CloudWatch API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: AWS CloudWatch\n  ServiceCategory: Developer Tools / API\n  ProviderName: AWS CloudWatch\n  PublisherName: AWS CloudWatch\n  InvoiceIssuerName: AWS CloudWatch\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon CloudWatch API\n    baseURL: https://monitoring.amazonaws.com\n    tags:\n      - Alarms\n      - Dashboards\n      - Metric-Streams\n      - Metrics\n      - Statistics\n    serviceName: Amazon CloudWatch API\n    serviceCategory: API\n  - name: Amazon CloudWatch Logs API\n    baseURL: https://logs.amazonaws.com\n    tags:\n      - Insights\n      - Log-Analytics\n      - Log-Groups\n      - Log-Streams\n      - Logs\n    serviceName: Amazon CloudWatch Logs API\n    serviceCategory: API\n  - name: Amazon CloudWatch Events API\n    baseURL: https://events.amazonaws.com\n    tags:\n      - Event-Bus\n      - Eventbridge\n      - Events\n  \
  \    - Rules\n      - Targets\n    serviceName: Amazon CloudWatch Events API\n    serviceCategory: API\n  - name: Amazon CloudWatch Application Insights API\n    baseURL: https://applicationinsights.amazonaws.com\n    tags:\n      - Anomaly-Detection\n      - Application-Insights\n      - Observability\n    serviceName: Amazon CloudWatch Application Insights API\n    serviceCategory: API\n  - name: Amazon CloudWatch Synthetics API\n    baseURL: https://synthetics.amazonaws.com\n    tags:\n      - Canaries\n      - Endpoint-Monitoring\n      - Monitoring\n      - Synthetics\n    serviceName: Amazon CloudWatch Synthetics API\n    serviceCategory: API\n  - name: Amazon CloudWatch Internet Monitor API\n    baseURL: https://internetmonitor.amazonaws.com\n    tags:\n      - Availability\n      - Internet-Monitor\n      - Latency\n      - Network-Performance\n    serviceName: Amazon CloudWatch Internet Monitor API\n    serviceCategory: API\n  - name: Amazon CloudWatch RUM API\n    baseURL: https://rum.amazonaws.com\n\
  \    tags:\n      - Client-Side\n      - Real-User-Monitoring\n      - Rum\n      - Web-Performance\n    serviceName: Amazon CloudWatch RUM API\n    serviceCategory: API\n  - name: Amazon CloudWatch Observability Access Manager API\n    baseURL: https://oam.amazonaws.com\n    tags:\n      - Cross-Account\n      - Monitoring-Account\n      - Oam\n      - Observability\n    serviceName: Amazon CloudWatch Observability Access Manager API\n    serviceCategory: API\n  - name: Amazon CloudWatch Application Signals API\n    baseURL: https://application-signals.amazonaws.com\n    tags:\n      - Apm\n      - Application-Signals\n      - Service-Level-Objectives\n      - Slo\n    serviceName: Amazon CloudWatch Application Signals API\n    serviceCategory: API\n  - name: Amazon CloudWatch Network Monitor API\n    baseURL: https://networkmonitor.amazonaws.com\n    tags:\n      - Direct-Connect\n      - Hybrid-Connectivity\n      - Network-Monitor\n      - Network-Performance\n    serviceName: Amazon\
  \ CloudWatch Network Monitor API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cloudwatch/refs/heads/main/finops/cloudwatch-finops.yml
sources: []
specification: FinOps Framework
tags:
- Alarms
- Aws
- Dashboards
- Logs
- Metrics
- Monitoring
- Observability
- FinOps
- Cost Management
- FOCUS
---
