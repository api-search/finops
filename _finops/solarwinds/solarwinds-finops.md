---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: solarwinds-orion-openapi.yml
  format: yaml
  label: SolarWinds Orion API
  slug: solarwinds-orion-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-orion-openapi.yml
- filename: solarwinds-service-desk-openapi.yml
  format: yaml
  label: SolarWinds Service Desk API
  slug: solarwinds-service-desk-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-service-desk-openapi.yml
- filename: openapi.json
  format: json
  label: SolarWinds Observability API
  slug: solarwinds-observability-api
  spec_type: OpenAPI
  url: https://api.na-01.cloud.solarwinds.com/v1/openapi.json
- filename: solarwinds-pingdom-openapi.yml
  format: yaml
  label: SolarWinds Pingdom API
  slug: solarwinds-pingdom-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-pingdom-openapi.yml
- filename: solarwinds-loggly-openapi.yml
  format: yaml
  label: SolarWinds Loggly API
  slug: solarwinds-loggly-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-loggly-openapi.yml
- filename: solarwinds-papertrail-openapi.yml
  format: yaml
  label: SolarWinds Papertrail API
  slug: solarwinds-papertrail-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/openapi/solarwinds-papertrail-openapi.yml
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
description: FinOps framework definition for the SolarWinds API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SolarWinds
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SolarWinds
  PublisherName: SolarWinds
  ServiceCategory: Developer Tools / API
  ServiceName: SolarWinds
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
name: Solarwinds Finops
provider_name: SolarWinds
provider_slug: solarwinds
publisher_name: SolarWinds
service_category: API
slug: solarwinds-finops
source_filename: solarwinds-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SolarWinds\nproviderId: solarwinds\npublisherName: SolarWinds\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Application Monitoring\n  - Database Monitoring\n  - Infrastructure\n  - IP Address Management\n  - IT Management\n  - ITSM\n  - Log Management\n  - Network Monitoring\n  - Observability\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SolarWinds API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and\
  \ finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud\
  \ Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SolarWinds\n  ServiceCategory: Developer Tools / API\n  ProviderName: SolarWinds\n  PublisherName: SolarWinds\n  InvoiceIssuerName: SolarWinds\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SolarWinds Orion API\n    baseURL: https://{orion-server}:17778/SolarWinds/InformationService/v3\n    tags:\n      - Infrastructure Management\n      - Network Monitoring\n      - Orion\n      - SWIS\n    serviceName: SolarWinds Orion API\n    serviceCategory: API\n  - name: SolarWinds Service Desk API\n    baseURL: https://{instance}.samanage.com/api\n    tags:\n      - Help Desk\n      - ITSM\n      - Service Desk\n      - Ticketing\n    serviceName: SolarWinds Service Desk API\n    serviceCategory: API\n  - name: SolarWinds Observability API\n    baseURL: https://api.na-01.cloud.solarwinds.com\n\
  \    tags:\n      - APM\n      - Cloud\n      - Logs\n      - Metrics\n      - Monitoring\n      - Observability\n      - Tracing\n    serviceName: SolarWinds Observability API\n    serviceCategory: API\n  - name: SolarWinds Database Performance Analyzer API\n    baseURL: https://{dpa-server}:8124/iwc/api\n    tags:\n      - Database\n      - Monitoring\n      - Performance\n      - SQL\n    serviceName: SolarWinds Database Performance Analyzer API\n    serviceCategory: API\n  - name: SolarWinds NPM REST API\n    baseURL: https://{npm-server}:17778/SolarWinds/InformationService/v3\n    tags:\n      - Monitoring\n      - Network\n      - Performance\n      - SNMP\n    serviceName: SolarWinds NPM REST API\n    serviceCategory: API\n  - name: SolarWinds Web Help Desk API\n    baseURL: https://{whd-server}/helpdesk/WebObjects/Helpdesk.woa/ra\n    tags:\n      - Asset Management\n      - Help Desk\n      - IT Support\n      - Ticketing\n    serviceName: SolarWinds Web Help Desk API\n    serviceCategory:\
  \ API\n  - name: SolarWinds Pingdom API\n    baseURL: https://api.pingdom.com/api/3.1\n    tags:\n      - Performance\n      - Synthetic Monitoring\n      - Uptime Monitoring\n      - Website Monitoring\n    serviceName: SolarWinds Pingdom API\n    serviceCategory: API\n  - name: SolarWinds Loggly API\n    baseURL: https://{subdomain}.loggly.com/apiv2\n    tags:\n      - Cloud\n      - Log Management\n      - Logging\n      - Search\n    serviceName: SolarWinds Loggly API\n    serviceCategory: API\n  - name: SolarWinds Papertrail API\n    baseURL: https://papertrailapp.com/api/v1\n    tags:\n      - Cloud\n      - Log Management\n      - Logging\n      - Search\n    serviceName: SolarWinds Papertrail API\n    serviceCategory: API\n  - name: SolarWinds IPAM API\n    baseURL: https://{orion-server}:17778/SolarWinds/InformationService/v3\n    tags:\n      - DHCP\n      - DNS\n      - IP Address Management\n      - IPAM\n      - Network\n    serviceName: SolarWinds IPAM API\n    serviceCategory:\
  \ API\n  - name: SolarWinds NCM API\n    baseURL: https://{orion-server}:17778/SolarWinds/InformationService/v3\n    tags:\n      - Automation\n      - Compliance\n      - Configuration Management\n      - Network Configuration\n    serviceName: SolarWinds NCM API\n    serviceCategory: API\n  - name: SolarWinds SAM API\n    baseURL: https://{orion-server}:17778/SolarWinds/InformationService/v3\n    tags:\n      - APM\n      - Application Monitoring\n      - Performance\n      - Server Monitoring\n    serviceName: SolarWinds SAM API\n    serviceCategory: API\n  - name: SolarWinds AppOptics API\n    baseURL: https://api.appoptics.com/v1\n    tags:\n      - APM\n      - Deprecated\n      - Metrics\n      - Monitoring\n      - Tracing\n    serviceName: SolarWinds AppOptics API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/solarwinds/refs/heads/main/finops/solarwinds-finops.yml
sources: []
specification: FinOps Framework
tags:
- Application Monitoring
- Database Monitoring
- Infrastructure
- IP Address Management
- IT Management
- ITSM
- Log Management
- Network Monitoring
- Observability
- FinOps
- Cost Management
- FOCUS
---
