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
  label: Oracle Cloud Infrastructure (OCI) REST API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en-us/iaas/api/#/en/iaas/latest/
- filename: openapi.yaml
  format: yaml
  label: Oracle Autonomous Database API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en-us/iaas/api/#/en/database/latest/
- filename: api-integration-cloud.html
  format: yaml
  label: Oracle Integration Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/paas/integration-cloud/rest-api/api-integration-cloud.html
- filename: api-rest.html
  format: yaml
  label: Oracle Analytics Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en/cloud/paas/analytics-cloud/acapi/api-rest.html
- filename: openapi.yaml
  format: yaml
  label: Oracle Cloud Infrastructure Data Science API
  slug: ''
  spec_type: OpenAPI
  url: https://docs.oracle.com/en-us/iaas/api/#/en/data-science/latest/
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
description: FinOps framework definition for the Oracle Platforms API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Platforms
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Platforms
  PublisherName: Oracle Platforms
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Platforms
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
name: Oracle Platforms Finops
provider_name: Oracle Platforms
provider_slug: oracle-platforms
publisher_name: Oracle Platforms
service_category: API
slug: oracle-platforms-finops
source_filename: oracle-platforms-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Platforms\nproviderId: oracle-platforms\npublisherName: Oracle Platforms\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Cloud Computing\n  - Database\n  - Enterprise Software\n  - Infrastructure as a Service\n  - Integration\n  - Machine Learning\n  - Platform as a Service\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Platforms API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering,\
  \ product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n\
  \      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Platforms\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Platforms\n  PublisherName: Oracle Platforms\n  InvoiceIssuerName: Oracle Platforms\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Cloud Infrastructure (OCI) REST API\n    baseURL: https://iaas.{region}.oraclecloud.com\n    tags:\n      - Cloud\n      - Compute\n      - IaaS\n      - Infrastructure\n      - Storage\n    serviceName: Oracle Cloud Infrastructure (OCI) REST API\n    serviceCategory: API\n  - name: Oracle Autonomous Database API\n    baseURL: https://database.{region}.oraclecloud.com\n    tags:\n      - Autonomous\n      - Database\n      - DBaaS\n      - SQL\n    serviceName: Oracle Autonomous Database API\n    serviceCategory: API\n  - name: Oracle Integration\
  \ Cloud API\n    baseURL: https://integration.ocp.oraclecloud.com\n    tags:\n      - API Management\n      - Automation\n      - Integration\n      - iPaaS\n    serviceName: Oracle Integration Cloud API\n    serviceCategory: API\n  - name: Oracle Content Management API\n    baseURL: https://www.oraclecloud.com/content/api\n    tags:\n      - CMS\n      - Collaboration\n      - Content Management\n      - Digital Assets\n    serviceName: Oracle Content Management API\n    serviceCategory: API\n  - name: Oracle Fusion Cloud ERP API\n    baseURL: https://servername.fa.us2.oraclecloud.com\n    tags:\n      - Cloud Applications\n      - ERP\n      - Finance\n      - Procurement\n    serviceName: Oracle Fusion Cloud ERP API\n    serviceCategory: API\n  - name: Oracle Analytics Cloud API\n    baseURL: https://{instanceName}.analytics.ocp.oraclecloud.com\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Data Visualization\n      - Reporting\n    serviceName: Oracle Analytics\
  \ Cloud API\n    serviceCategory: API\n  - name: Oracle Cloud Infrastructure Data Science API\n    baseURL: https://datascience.{region}.oraclecloud.com\n    tags:\n      - AI\n      - Data Science\n      - Machine Learning\n      - MLOps\n    serviceName: Oracle Cloud Infrastructure Data Science API\n    serviceCategory: API\n  - name: Oracle APEX REST APIs\n    baseURL: https://{instance}.adb.{region}.oraclecloudapps.com\n    tags:\n      - APEX\n      - Application Development\n      - Low-Code\n      - REST Services\n    serviceName: Oracle APEX REST APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-platforms/refs/heads/main/finops/oracle-platforms-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Cloud Computing
- Database
- Enterprise Software
- Infrastructure as a Service
- Integration
- Machine Learning
- Platform as a Service
- SaaS
- FinOps
- Cost Management
- FOCUS
---
