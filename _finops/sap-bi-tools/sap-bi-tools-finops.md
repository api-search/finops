---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: overview
  format: yaml
  label: SAP Analytics Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/SACOpenAPI/overview
- filename: overview
  format: yaml
  label: SAP HANA Cloud Data Lake Files REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/HanaCloudDataLake/overview
- filename: overview
  format: yaml
  label: SAP Datasphere API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/Datasphere/overview
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
description: FinOps framework definition for the SAP BI Tools API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP BI Tools
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP BI Tools
  PublisherName: SAP BI Tools
  ServiceCategory: Developer Tools / API
  ServiceName: SAP BI Tools
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
name: Sap Bi Tools Finops
provider_name: SAP BI Tools
provider_slug: sap-bi-tools
publisher_name: SAP BI Tools
service_category: API
slug: sap-bi-tools-finops
source_filename: sap-bi-tools-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP BI Tools\nproviderId: sap-bi-tools\npublisherName: SAP BI Tools\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Data Visualization\n  - Reporting\n  - SAP\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP BI Tools API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP BI Tools\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP BI Tools\n  PublisherName: SAP BI Tools\n  InvoiceIssuerName: SAP BI Tools\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Analytics Cloud API\n    baseURL: https://api.sapanalytics.cloud\n    tags:\n      - Analytics\n      - Cloud\n      - Models\n      - Stories\n    serviceName: SAP Analytics Cloud API\n    serviceCategory: API\n  - name: SAP Analytics Cloud Data Export API\n    baseURL: https://api.sapanalytics.cloud\n    tags:\n      - Analytics\n      - Cloud\n      - Data Export\n      - OData\n    serviceName: SAP Analytics Cloud Data Export API\n    serviceCategory: API\n  - name: SAP Analytics Cloud Content Network REST API\n    baseURL: https://api.sapanalytics.cloud\n    tags:\n      - Analytics\n      - Cloud\n      - Content Management\n    serviceName: SAP Analytics Cloud Content\
  \ Network REST API\n    serviceCategory: API\n  - name: SAP Analytics Cloud Analytics Designer API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Application Design\n      - Embedded Analytics\n      - JavaScript\n    serviceName: SAP Analytics Cloud Analytics Designer API\n    serviceCategory: API\n  - name: SAP BusinessObjects BI Platform RESTful Web Services\n    baseURL: https://server:port/biprws\n    tags:\n      - BusinessObjects\n      - Documents\n      - Reports\n      - Scheduling\n    serviceName: SAP BusinessObjects BI Platform RESTful Web Services\n    serviceCategory: API\n  - name: SAP BusinessObjects Web Intelligence RESTful Web Services API\n    baseURL: https://server:port/biprws\n    tags:\n      - BusinessObjects\n      - Data Providers\n      - Reports\n      - Web Intelligence\n    serviceName: SAP BusinessObjects Web Intelligence RESTful Web Services API\n    serviceCategory: API\n  - name: SAP BusinessObjects BI Semantic Layer REST API\n    baseURL: https://server:port/biprws\n\
  \    tags:\n      - BusinessObjects\n      - Data Access\n      - Semantic Layer\n      - Universes\n    serviceName: SAP BusinessObjects BI Semantic Layer REST API\n    serviceCategory: API\n  - name: SAP Crystal Reports RESTful Web Services API\n    baseURL: ''\n    tags:\n      - Crystal Reports\n      - Embedded Analytics\n      - Reporting\n    serviceName: SAP Crystal Reports RESTful Web Services API\n    serviceCategory: API\n  - name: SAP Crystal Reports .NET SDK\n    baseURL: ''\n    tags:\n      - .NET\n      - Crystal Reports\n      - SDK\n      - Visual Studio\n    serviceName: SAP Crystal Reports .NET SDK\n    serviceCategory: API\n  - name: SAP Lumira Discovery Extensions API\n    baseURL: ''\n    tags:\n      - Extensions\n      - JavaScript\n      - Lumira\n      - Visualization\n    serviceName: SAP Lumira Discovery Extensions API\n    serviceCategory: API\n  - name: SAP HANA Cloud Data Lake Files REST API\n    baseURL: https://api.hana.ondemand.com\n    tags:\n      -\
  \ Cloud\n      - Data Access\n      - Data Lake\n      - HANA\n    serviceName: SAP HANA Cloud Data Lake Files REST API\n    serviceCategory: API\n  - name: SAP Datasphere API\n    baseURL: https://datasphere-api.cfapps.eu10.hana.ondemand.com\n    tags:\n      - Data Modeling\n      - Data Warehouse\n      - Datasphere\n      - Integration\n    serviceName: SAP Datasphere API\n    serviceCategory: API\n  - name: SAP Datasphere Consumption and Catalog API\n    baseURL: https://datasphere-api.cfapps.eu10.hana.ondemand.com\n    tags:\n      - Catalog\n      - Data Consumption\n      - Datasphere\n      - OData\n    serviceName: SAP Datasphere Consumption and Catalog API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-bi-tools/refs/heads/main/finops/sap-bi-tools-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Data Visualization
- Reporting
- SAP
- FinOps
- Cost Management
- FOCUS
---
