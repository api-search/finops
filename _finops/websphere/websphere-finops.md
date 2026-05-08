---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: 9.0.5
  format: yaml
  label: WebSphere Application Server Admin API
  slug: websphere-admin-rest-api
  spec_type: OpenAPI
  url: https://www.ibm.com/docs/en/was/9.0.5?topic=api-openapi-specification
- filename: websphere-liberty-admin-rest-api.yml
  format: yaml
  label: WebSphere Liberty Admin REST API
  slug: websphere-liberty-admin-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-liberty-admin-rest-api.yml
- filename: websphere-liberty-rest-connector-api.yml
  format: yaml
  label: WebSphere Liberty REST Connector API
  slug: websphere-liberty-rest-connector-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-liberty-rest-connector-api.yml
- filename: websphere-mq-rest-api.yml
  format: yaml
  label: WebSphere MQ REST API
  slug: websphere-mq-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-mq-rest-api.yml
- filename: websphere-liberty-collective-controller-rest-api.yml
  format: yaml
  label: WebSphere Liberty Collective Controller REST API
  slug: websphere-liberty-collective-controller-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-liberty-collective-controller-rest-api.yml
- filename: websphere-automation-rest-api.yml
  format: yaml
  label: WebSphere Automation REST API
  slug: websphere-automation-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/websphere-automation-rest-api.yml
- filename: open-liberty-apis.yml
  format: yaml
  label: Open Liberty APIs
  slug: open-liberty-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/openapi/open-liberty-apis.yml
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
description: FinOps framework definition for the IBM WebSphere API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: IBM WebSphere
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: IBM WebSphere
  PublisherName: IBM WebSphere
  ServiceCategory: Developer Tools / API
  ServiceName: IBM WebSphere
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
name: Websphere Finops
provider_name: IBM WebSphere
provider_slug: websphere
publisher_name: IBM WebSphere
service_category: API
slug: websphere-finops
source_filename: websphere-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: IBM WebSphere\nproviderId: websphere\npublisherName: IBM WebSphere\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Application Server\n  - Cloud Native\n  - Enterprise Java\n  - J2EE\n  - Microservices\n  - Middleware\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the IBM WebSphere API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: IBM WebSphere\n  ServiceCategory: Developer Tools / API\n  ProviderName: IBM WebSphere\n  PublisherName: IBM WebSphere\n  InvoiceIssuerName: IBM WebSphere\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: WebSphere Application Server Admin API\n    baseURL: https://localhost:9443/ibm/api\n    tags:\n      - Administration\n      - Configuration\n      - Deployment\n      - Monitoring\n    serviceName: WebSphere Application Server Admin API\n    serviceCategory: API\n  - name: WebSphere Liberty Admin REST API\n    baseURL: https://localhost:9443/ibm/api\n    tags:\n      - Administration\n      - Configuration\n      - Liberty\n      - REST API\n    serviceName: WebSphere Liberty Admin REST API\n    serviceCategory: API\n  - name: WebSphere Liberty REST Connector API\n    baseURL: https://localhost:9443/IBMJMXConnectorREST/api\n    tags:\n      - JMX\n\
  \      - Liberty\n      - Remote Administration\n      - REST Connector\n    serviceName: WebSphere Liberty REST Connector API\n    serviceCategory: API\n  - name: WebSphere MQ REST API\n    baseURL: https://localhost:9443/ibmmq/rest/v2\n    tags:\n      - Integration\n      - Messaging\n      - Publish Subscribe\n      - Queue Management\n    serviceName: WebSphere MQ REST API\n    serviceCategory: API\n  - name: WebSphere Application Server JMX API\n    baseURL: service:jmx:rmi:///jndi/rmi://localhost:2809/jmxrmi\n    tags:\n      - JMX\n      - Management\n      - MBeans\n      - Monitoring\n    serviceName: WebSphere Application Server JMX API\n    serviceCategory: API\n  - name: WebSphere Liberty Collective Controller REST API\n    baseURL: https://localhost:9443/ibm/api/collective\n    tags:\n      - Clustering\n      - Collective\n      - Liberty\n      - Management\n    serviceName: WebSphere Liberty Collective Controller REST API\n    serviceCategory: API\n  - name: WebSphere\
  \ Automation REST API\n    baseURL: https://automation-api.example.com/v1\n    tags:\n      - Automation\n      - Health Monitoring\n      - Patching\n      - Vulnerability Management\n    serviceName: WebSphere Automation REST API\n    serviceCategory: API\n  - name: Open Liberty APIs\n    baseURL: https://localhost:9443/ibm/api\n    tags:\n      - Cloud Native\n      - Jakarta EE\n      - MicroProfile\n      - Open Liberty\n    serviceName: Open Liberty APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/websphere/refs/heads/main/finops/websphere-finops.yml
sources: []
specification: FinOps Framework
tags:
- Application Server
- Cloud Native
- Enterprise Java
- J2EE
- Microservices
- Middleware
- FinOps
- Cost Management
- FOCUS
---
