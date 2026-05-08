---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: fastly-services-openapi.yml
  format: yaml
  label: Fastly Services API
  slug: services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-services-openapi.yml
- filename: fastly-purging-openapi.yml
  format: yaml
  label: Fastly Purging API
  slug: purging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-purging-openapi.yml
- filename: fastly-logging-openapi.yml
  format: yaml
  label: Fastly Real-Time Logging API
  slug: logging-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-logging-openapi.yml
- filename: fastly-metrics-and-stats-openapi.yml
  format: yaml
  label: Fastly Metrics and Stats API
  slug: metrics-and-stats-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-metrics-and-stats-openapi.yml
- filename: fastly-tls-openapi.yml
  format: yaml
  label: Fastly TLS API
  slug: tls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-tls-openapi.yml
- filename: fastly-vcl-services-openapi.yml
  format: yaml
  label: Fastly VCL Services API
  slug: vcl-services-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-vcl-services-openapi.yml
- filename: fastly-account-openapi.yml
  format: yaml
  label: Fastly Account API
  slug: account-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-account-openapi.yml
- filename: fastly-authentication-tokens-openapi.yml
  format: yaml
  label: Fastly Authentication Tokens API
  slug: authentication-tokens-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-authentication-tokens-openapi.yml
- filename: fastly-acls-openapi.yml
  format: yaml
  label: Fastly Access Control Lists API
  slug: acls-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-acls-openapi.yml
- filename: fastly-dictionaries-openapi.yml
  format: yaml
  label: Fastly Edge Dictionaries API
  slug: dictionaries-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-dictionaries-openapi.yml
- filename: fastly-compute-openapi.yml
  format: yaml
  label: Fastly Compute API
  slug: compute-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-compute-openapi.yml
- filename: fastly-waf-openapi.yml
  format: yaml
  label: Fastly Next-Gen WAF API
  slug: waf-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-waf-openapi.yml
- filename: fastly-domain-management-openapi.yml
  format: yaml
  label: Fastly Domain Management API
  slug: domain-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-domain-management-openapi.yml
- filename: fastly-products-openapi.yml
  format: yaml
  label: Fastly Products API
  slug: products-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/openapi/fastly-products-openapi.yml
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
description: FinOps framework definition for the fastly API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: fastly
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: fastly
  PublisherName: fastly
  ServiceCategory: Developer Tools / API
  ServiceName: fastly
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
name: Fastly Finops
provider_name: fastly
provider_slug: fastly
publisher_name: fastly
service_category: API
slug: fastly-finops
source_filename: fastly-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: fastly\nproviderId: fastly\npublisherName: fastly\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the fastly API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: fastly\n  ServiceCategory: Developer Tools / API\n  ProviderName: fastly\n  PublisherName: fastly\n  InvoiceIssuerName: fastly\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Fastly Services API\n    baseURL: https://api.fastly.com\n    tags:\n      - CDN\n      - Configuration\n      - Edge Cloud\n    serviceName: Fastly Services API\n    serviceCategory: API\n  - name: Fastly Purging API\n    baseURL: https://api.fastly.com\n    tags:\n      - Cache\n      - CDN\n      - Content Delivery\n      - Purging\n    serviceName: Fastly Purging API\n    serviceCategory: API\n  - name: Fastly Real-Time Logging API\n    baseURL: https://api.fastly.com\n    tags:\n      - Analytics\n      - Logging\n      - Monitoring\n      - Observability\n    serviceName: Fastly Real-Time Logging API\n    serviceCategory: API\n  - name: Fastly Metrics and Stats API\n    baseURL: https://rt.fastly.com\n    tags:\n      - Analytics\n      - Metrics\n      - Monitoring\n      - Real-Time\n      - Statistics\n\
  \    serviceName: Fastly Metrics and Stats API\n    serviceCategory: API\n  - name: Fastly TLS API\n    baseURL: https://api.fastly.com\n    tags:\n      - Certificates\n      - Encryption\n      - Security\n      - SSL\n      - TLS\n    serviceName: Fastly TLS API\n    serviceCategory: API\n  - name: Fastly VCL Services API\n    baseURL: https://api.fastly.com\n    tags:\n      - Caching\n      - CDN\n      - Configuration\n      - Edge Logic\n      - VCL\n    serviceName: Fastly VCL Services API\n    serviceCategory: API\n  - name: Fastly Account API\n    baseURL: https://api.fastly.com\n    tags:\n      - Account\n      - Administration\n      - IAM\n      - Users\n    serviceName: Fastly Account API\n    serviceCategory: API\n  - name: Fastly Authentication Tokens API\n    baseURL: https://api.fastly.com\n    tags:\n      - API Keys\n      - Authentication\n      - Security\n      - Tokens\n    serviceName: Fastly Authentication Tokens API\n    serviceCategory: API\n  - name: Fastly\
  \ Access Control Lists API\n    baseURL: https://api.fastly.com\n    tags:\n      - Access Control\n      - Edge Security\n      - IP Filtering\n      - Security\n    serviceName: Fastly Access Control Lists API\n    serviceCategory: API\n  - name: Fastly Edge Dictionaries API\n    baseURL: https://api.fastly.com\n    tags:\n      - Dictionaries\n      - Dynamic Configuration\n      - Edge Configuration\n      - Key-Value\n    serviceName: Fastly Edge Dictionaries API\n    serviceCategory: API\n  - name: Fastly Compute API\n    baseURL: https://api.fastly.com\n    tags:\n      - Compute\n      - Edge Computing\n      - Serverless\n      - WebAssembly\n    serviceName: Fastly Compute API\n    serviceCategory: API\n  - name: Fastly Next-Gen WAF API\n    baseURL: https://api.fastly.com\n    tags:\n      - DDoS Protection\n      - Security\n      - WAF\n      - Web Application Firewall\n    serviceName: Fastly Next-Gen WAF API\n    serviceCategory: API\n  - name: Fastly Domain Management API\n\
  \    baseURL: https://api.fastly.com\n    tags:\n      - CDN\n      - Configuration\n      - DNS\n      - Domains\n    serviceName: Fastly Domain Management API\n    serviceCategory: API\n  - name: Fastly Products API\n    baseURL: https://api.fastly.com\n    tags:\n      - Configuration\n      - Features\n      - Platform\n      - Products\n    serviceName: Fastly Products API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/fastly/refs/heads/main/finops/fastly-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
