---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: dynatrace-metrics-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Metrics API v2
  slug: dynatrace-metrics-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-metrics-api-v2-openapi.yml
- filename: dynatrace-log-monitoring-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Log Monitoring API v2
  slug: dynatrace-log-monitoring-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-log-monitoring-api-v2-openapi.yml
- filename: dynatrace-account-management-api-openapi.yml
  format: yaml
  label: Dynatrace Account Management API
  slug: dynatrace-account-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-account-management-api-openapi.yml
- filename: dynatrace-events-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Events API v2
  slug: dynatrace-events-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-events-api-v2-openapi.yml
- filename: dynatrace-problems-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Problems API v2
  slug: dynatrace-problems-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-problems-api-v2-openapi.yml
- filename: dynatrace-entities-api-v2-openapi.yml
  format: yaml
  label: Dynatrace Entities API v2
  slug: dynatrace-entities-api-v2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/openapi/dynatrace-entities-api-v2-openapi.yml
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
description: FinOps framework definition for the Dynatrace API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Dynatrace
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Dynatrace
  PublisherName: Dynatrace
  ServiceCategory: Developer Tools / API
  ServiceName: Dynatrace
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
name: Dynatrace Finops
provider_name: Dynatrace
provider_slug: dynatrace
publisher_name: Dynatrace
service_category: API
slug: dynatrace-finops
source_filename: dynatrace-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dynatrace\nproviderId: dynatrace\npublisherName: Dynatrace\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI Operations\n  - Analytics\n  - APM\n  - Application Performance Monitoring\n  - Application Security\n  - Automation\n  - Cloud Monitoring\n  - Digital Experience Management\n  - Intelligence\n  - Observability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Dynatrace API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Dynatrace\n  ServiceCategory: Developer Tools / API\n  ProviderName: Dynatrace\n  PublisherName: Dynatrace\n  InvoiceIssuerName: Dynatrace\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Dynatrace Environment API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Analytics\n      - Automation\n      - Intelligence\n      - Monitoring\n      - Observability\n    serviceName: Dynatrace Environment API\n    serviceCategory: API\n  - name: Dynatrace Metrics API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Metrics\n      - Monitoring\n      - Observability\n      - Time Series\n    serviceName: Dynatrace Metrics API v2\n    serviceCategory: API\n  - name: Dynatrace Log Monitoring API v2\n    baseURL:\
  \ https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Log Management\n      - Logs\n      - Monitoring\n      - Observability\n    serviceName: Dynatrace Log Monitoring API v2\n    serviceCategory: API\n  - name: Dynatrace Synthetic API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Digital Experience\n      - Observability\n      - Synthetic Monitoring\n      - Testing\n    serviceName: Dynatrace Synthetic API v2\n    serviceCategory: API\n  - name: Dynatrace Configuration API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/config/v1\n    tags:\n      - Configuration\n      - Management\n      - Monitoring\n      - Observability\n    serviceName: Dynatrace Configuration API\n    serviceCategory: API\n  - name: Dynatrace Account Management API\n    baseURL: https://api.dynatrace.com/iam/v1\n    tags:\n      - Access Management\n      - Account Management\n      - Administration\n      - Identity\n    serviceName: Dynatrace Account\
  \ Management API\n    serviceCategory: API\n  - name: Dynatrace OpenPipeline API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n    tags:\n      - Data Ingestion\n      - Data Pipelines\n      - Observability\n      - Platform\n    serviceName: Dynatrace OpenPipeline API\n    serviceCategory: API\n  - name: Dynatrace Automation API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n    tags:\n      - Automation\n      - Orchestration\n      - Platform\n      - Workflows\n    serviceName: Dynatrace Automation API\n    serviceCategory: API\n  - name: Dynatrace Events API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Alerting\n      - Events\n      - Monitoring\n      - Observability\n    serviceName: Dynatrace Events API v2\n    serviceCategory: API\n  - name: Dynatrace Problems API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Alerting\n      - Monitoring\n      - Observability\n      -\
  \ Problems\n    serviceName: Dynatrace Problems API v2\n    serviceCategory: API\n  - name: Dynatrace Entities API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Entities\n      - Monitoring\n      - Observability\n      - Topology\n    serviceName: Dynatrace Entities API v2\n    serviceCategory: API\n  - name: Dynatrace Settings API 2.0\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Configuration\n      - Management\n      - Observability\n      - Settings\n    serviceName: Dynatrace Settings API 2.0\n    serviceCategory: API\n  - name: Dynatrace Extensions API 2.0\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Extensions\n      - Integrations\n      - Monitoring\n      - Observability\n    serviceName: Dynatrace Extensions API 2.0\n    serviceCategory: API\n  - name: Dynatrace DQL/Grail Query API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n    tags:\n      - Analytics\n\
  \      - DQL\n      - Grail\n      - Observability\n      - Query\n    serviceName: Dynatrace DQL/Grail Query API\n    serviceCategory: API\n  - name: Dynatrace Access Tokens API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Access Management\n      - Authentication\n      - Security\n      - Tokens\n    serviceName: Dynatrace Access Tokens API v2\n    serviceCategory: API\n  - name: Dynatrace Service-Level Objectives API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Observability\n      - Reliability\n      - Service Level Objectives\n      - SLO\n    serviceName: Dynatrace Service-Level Objectives API\n    serviceCategory: API\n  - name: Dynatrace Releases API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Deployment\n      - Observability\n      - Releases\n      - Version Management\n    serviceName: Dynatrace Releases API\n    serviceCategory: API\n  - name: Dynatrace Network Zones\
  \ API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Infrastructure\n      - Monitoring\n      - Network Zones\n      - Networking\n    serviceName: Dynatrace Network Zones API\n    serviceCategory: API\n  - name: Dynatrace Deployment API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - ActiveGate\n      - Deployment\n      - Installation\n      - OneAgent\n    serviceName: Dynatrace Deployment API\n    serviceCategory: API\n  - name: Dynatrace Audit Logs API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Audit Logs\n      - Compliance\n      - Governance\n      - Security\n    serviceName: Dynatrace Audit Logs API\n    serviceCategory: API\n  - name: Dynatrace Business Events API v2\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Business Analytics\n      - Business Events\n      - Business Intelligence\n      - Observability\n    serviceName: Dynatrace Business\
  \ Events API v2\n    serviceCategory: API\n  - name: Dynatrace Application Security API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Application Security\n      - Runtime Protection\n      - Security\n      - Vulnerabilities\n    serviceName: Dynatrace Application Security API\n    serviceCategory: API\n  - name: Dynatrace Custom Tags API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Entities\n      - Metadata\n      - Monitoring\n    serviceName: Dynatrace Custom Tags API\n    serviceCategory: API\n  - name: Dynatrace ActiveGate API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - ActiveGate\n      - Deployment\n      - Infrastructure\n      - Monitoring\n    serviceName: Dynatrace ActiveGate API\n    serviceCategory: API\n  - name: Dynatrace Credential Vault API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Credentials\n      - Secrets\n      - Security\n\
  \      - Synthetic Monitoring\n    serviceName: Dynatrace Credential Vault API\n    serviceCategory: API\n  - name: Dynatrace Document API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform/document/v1\n    tags:\n      - Dashboards\n      - Documents\n      - Notebooks\n      - Platform\n    serviceName: Dynatrace Document API\n    serviceCategory: API\n  - name: Dynatrace Grail Bucket Management API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n    tags:\n      - Data Management\n      - Grail\n      - Platform\n      - Storage\n    serviceName: Dynatrace Grail Bucket Management API\n    serviceCategory: API\n  - name: Dynatrace Davis AI API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n    tags:\n      - Causal Analysis\n      - Davis AI\n      - Machine Learning\n      - Platform\n      - Predictive Analytics\n    serviceName: Dynatrace Davis AI API\n    serviceCategory: API\n  - name: Dynatrace Hub API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n\
  \    tags:\n      - Apps\n      - Catalog\n      - Extensions\n      - Hub\n      - Platform\n    serviceName: Dynatrace Hub API\n    serviceCategory: API\n  - name: Dynatrace OneAgent on a Host API\n    baseURL: https://mySampleEnv.live.dynatrace.com/api/v2\n    tags:\n      - Deployment\n      - Host Monitoring\n      - Infrastructure\n      - OneAgent\n    serviceName: Dynatrace OneAgent on a Host API\n    serviceCategory: API\n  - name: Dynatrace Platform Management API\n    baseURL: https://mySampleEnv.live.dynatrace.com/platform\n    tags:\n      - Administration\n      - Environment Management\n      - Platform\n      - Settings\n    serviceName: Dynatrace Platform Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dynatrace/refs/heads/main/finops/dynatrace-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI Operations
- Analytics
- APM
- Application Performance Monitoring
- Application Security
- Automation
- Cloud Monitoring
- Digital Experience Management
- Intelligence
- Observability
- FinOps
- Cost Management
- FOCUS
---
