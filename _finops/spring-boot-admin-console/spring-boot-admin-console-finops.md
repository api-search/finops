---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: spring-boot-admin-console-openapi.yml
  format: yaml
  label: Spring Boot Admin Server API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/spring-boot-admin-console/refs/heads/main/openapi/spring-boot-admin-console-openapi.yml
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
description: FinOps framework definition for the Spring Boot Admin Console API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Spring Boot Admin Console
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Spring Boot Admin Console
  PublisherName: Spring Boot Admin Console
  ServiceCategory: Developer Tools / API
  ServiceName: Spring Boot Admin Console
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
name: Spring Boot Admin Console Finops
provider_name: Spring Boot Admin Console
provider_slug: spring-boot-admin-console
publisher_name: Spring Boot Admin Console
service_category: API
slug: spring-boot-admin-console-finops
source_filename: spring-boot-admin-console-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Spring Boot Admin Console\nproviderId: spring-boot-admin-console\npublisherName: Spring Boot Admin Console\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Actuator\n  - Administration\n  - Java\n  - Microservices\n  - Monitoring\n  - Spring Boot\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Spring Boot Admin Console API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Spring Boot Admin Console\n  ServiceCategory: Developer Tools / API\n  ProviderName: Spring Boot Admin Console\n  PublisherName: Spring Boot Admin Console\n  InvoiceIssuerName: Spring Boot Admin Console\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Spring Boot Admin Server API\n    baseURL: http://localhost:8080\n    tags:\n      - Administration\n      - Monitoring\n      - Server\n    serviceName: Spring Boot Admin Server API\n    serviceCategory: API\n  - name: Applications API\n    baseURL: http://localhost:8080/applications\n    tags:\n      - Applications\n      - Registration\n    serviceName: Applications API\n    serviceCategory: API\n  - name: Instances API\n    baseURL: http://localhost:8080/instances\n    tags:\n      - Actuator\n      - Instances\n      - Monitoring\n    serviceName: Instances\
  \ API\n    serviceCategory: API\n  - name: Events API\n    baseURL: http://localhost:8080/instances/events\n    tags:\n      - Events\n      - Notifications\n      - SSE\n    serviceName: Events API\n    serviceCategory: API\n  - name: Notifications API\n    baseURL: http://localhost:8080\n    tags:\n      - Alerts\n      - Notifications\n      - Webhooks\n    serviceName: Notifications API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: codecentric AG\n    url: https://www.codecentric.de/\n    email: info@codecentric.de\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/spring-boot-admin-console/refs/heads/main/finops/spring-boot-admin-console-finops.yml
sources: []
specification: FinOps Framework
tags:
- Actuator
- Administration
- Java
- Microservices
- Monitoring
- Spring Boot
- FinOps
- Cost Management
- FOCUS
---
