---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: oracle-weblogic-management-openapi.yml
  format: yaml
  label: WebLogic RESTful Management Services API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/openapi/oracle-weblogic-management-openapi.yml
- filename: oracle-weblogic-monitoring-openapi.yml
  format: yaml
  label: WebLogic Monitoring and Diagnostics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/openapi/oracle-weblogic-monitoring-openapi.yml
- filename: oracle-weblogic-deployment-openapi.yml
  format: yaml
  label: WebLogic Deployment API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/openapi/oracle-weblogic-deployment-openapi.yml
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
description: FinOps framework definition for the Oracle WebLogic Server API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle WebLogic Server
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle WebLogic Server
  PublisherName: Oracle WebLogic Server
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle WebLogic Server
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
name: Oracle Weblogic Finops
provider_name: Oracle WebLogic Server
provider_slug: oracle-weblogic
publisher_name: Oracle WebLogic Server
service_category: API
slug: oracle-weblogic-finops
source_filename: oracle-weblogic-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle WebLogic Server\nproviderId: oracle-weblogic\npublisherName: Oracle WebLogic Server\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Application Server\n  - Enterprise\n  - Java EE\n  - Middleware\n  - Oracle\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle WebLogic Server API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle WebLogic Server\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle WebLogic Server\n  PublisherName: Oracle WebLogic Server\n  InvoiceIssuerName: Oracle WebLogic Server\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description:\
  \ Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: WebLogic RESTful Management Services API\n    baseURL: http://localhost:7001/management/weblogic/latest\n    tags:\n      - Management\n      - Monitoring\n      - REST\n    serviceName: WebLogic RESTful Management Services API\n    serviceCategory: API\n  - name: WebLogic Monitoring and Diagnostics API\n    baseURL: http://localhost:7001/management/weblogic/latest/domainRuntime\n    tags:\n      - Diagnostics\n      - JMX\n      - Metrics\n      - Monitoring\n    serviceName: WebLogic Monitoring and Diagnostics API\n    serviceCategory: API\n  - name: WebLogic Deployment API\n    baseURL: http://localhost:7001/management/weblogic/latest/edit/appDeployments\n\
  \    tags:\n      - Applications\n      - Deployment\n      - Lifecycle\n    serviceName: WebLogic Deployment API\n    serviceCategory: API\n  - name: WebLogic WLST (WebLogic Scripting Tool) API\n    baseURL: https://localhost:5556\n    tags:\n      - Administration\n      - Automation\n      - Python\n      - Scripting\n    serviceName: WebLogic WLST (WebLogic Scripting Tool) API\n    serviceCategory: API\n  - name: WebLogic JMX API\n    baseURL: service:jmx:rmi:///jndi/rmi://localhost:7001/jmxrmi\n    tags:\n      - Java\n      - JMX\n      - Management\n      - MBeans\n    serviceName: WebLogic JMX API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-weblogic/refs/heads/main/finops/oracle-weblogic-finops.yml
sources: []
specification: FinOps Framework
tags:
- Application Server
- Enterprise
- Java EE
- Middleware
- Oracle
- FinOps
- Cost Management
- FOCUS
---
