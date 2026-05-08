---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-hana-cloud-rest-api.yml
  format: yaml
  label: SAP HANA Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-hana/refs/heads/main/openapi/sap-hana-cloud-rest-api.yml
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
description: FinOps framework definition for the SAP HANA API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP HANA
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP HANA
  PublisherName: SAP HANA
  ServiceCategory: Developer Tools / API
  ServiceName: SAP HANA
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
name: Sap Hana Finops
provider_name: SAP HANA
provider_slug: sap-hana
publisher_name: SAP HANA
service_category: API
slug: sap-hana-finops
source_filename: sap-hana-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP HANA\nproviderId: sap-hana\npublisherName: SAP HANA\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Cloud\n  - Database\n  - Enterprise\n  - In-Memory\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP HANA API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP HANA\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP HANA\n  PublisherName: SAP HANA\n  InvoiceIssuerName: SAP HANA\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP HANA Cloud REST API\n    baseURL: https://api.cf.{region}.hana.ondemand.com\n    tags:\n      - Administration\n      - Cloud\n      - Database Management\n    serviceName: SAP HANA Cloud REST API\n    serviceCategory: API\n  - name: SAP HANA SQL API\n    baseURL: jdbc:sap://{host}:{port}\n    tags:\n      - Database\n      - Query\n      - SQL\n    serviceName: SAP HANA SQL API\n    serviceCategory: API\n  - name: SAP HANA XS Engine API\n    baseURL: https://{host}:{port}\n    tags:\n      - Application Development\n      - JavaScript\n      - OData\n      - XS\n    serviceName: SAP HANA XS Engine API\n    serviceCategory: API\n  - name: SAP HANA Cockpit API\n    baseURL: https://{host}:{port}/sap/hana/\n    tags:\n\
  \      - Administration\n      - Management\n      - Monitoring\n    serviceName: SAP HANA Cockpit API\n    serviceCategory: API\n  - name: SAP HANA Smart Data Integration API\n    baseURL: https://{host}:{port}\n    tags:\n      - Data Integration\n      - ETL\n      - Replication\n    serviceName: SAP HANA Smart Data Integration API\n    serviceCategory: API\n  - name: SAP HANA Cloud Alerts and Metrics REST API\n    baseURL: https://api.cf.{region}.hana.ondemand.com\n    tags:\n      - Alerts\n      - Metering\n      - Metrics\n      - Monitoring\n    serviceName: SAP HANA Cloud Alerts and Metrics REST API\n    serviceCategory: API\n  - name: SAP HANA Spatial Services API\n    baseURL: https://api.cf.{region}.hana.ondemand.com\n    tags:\n      - Geocoding\n      - Location\n      - Mapping\n      - Routing\n      - Spatial\n    serviceName: SAP HANA Spatial Services API\n    serviceCategory: API\n  - name: SAP HANA Cloud Data Lake Files REST API\n    baseURL: https://{host}:{port}\n\
  \    tags:\n      - Cloud Storage\n      - Data Lake\n      - File Storage\n    serviceName: SAP HANA Cloud Data Lake Files REST API\n    serviceCategory: API\n  - name: SAP HANA Deployment Infrastructure (HDI) API\n    baseURL: https://{host}:{port}\n    tags:\n      - Containers\n      - Deployment\n      - DevOps\n      - HDI\n    serviceName: SAP HANA Deployment Infrastructure (HDI) API\n    serviceCategory: API\n  - name: SAP HANA Predictive Analysis Library (PAL) API\n    baseURL: https://{host}:{port}\n    tags:\n      - AI\n      - Machine Learning\n      - Predictive Analytics\n      - Statistics\n    serviceName: SAP HANA Predictive Analysis Library (PAL) API\n    serviceCategory: API\n  - name: SAP HANA JSON Document Store API\n    baseURL: https://{host}:{port}\n    tags:\n      - Document Store\n      - JSON\n      - Multi-Model\n      - NoSQL\n    serviceName: SAP HANA JSON Document Store API\n    serviceCategory: API\n  - name: SAP HANA Graph Engine API\n    baseURL: https://{host}:{port}\n\
  \    tags:\n      - Graph\n      - Knowledge Graph\n      - Multi-Model\n      - Network Analysis\n    serviceName: SAP HANA Graph Engine API\n    serviceCategory: API\n  - name: SAP HANA REST Info API\n    baseURL: https://{host}:{port}\n    tags:\n      - Metadata\n      - REST\n      - System Information\n    serviceName: SAP HANA REST Info API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-hana/refs/heads/main/finops/sap-hana-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Cloud
- Database
- Enterprise
- In-Memory
- FinOps
- Cost Management
- FOCUS
---
