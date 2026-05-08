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
  url: https://api.sap.com/api/API_ANALYTICS_CLOUD/overview
- filename: overview
  format: yaml
  label: SAP BusinessObjects BI Platform REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/BOBJ_BIPLATFORM/overview
- filename: sap-bi-bw4hana-odata-openapi.yml
  format: yaml
  label: SAP BW/4HANA OData API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-bi/refs/heads/main/openapi/sap-bi-bw4hana-odata-openapi.yml
- filename: overview
  format: yaml
  label: SAP Datasphere API
  slug: ''
  spec_type: OpenAPI
  url: https://api.sap.com/api/datasphere/overview
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
description: FinOps framework definition for the SAP Business Intelligence API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP Business Intelligence
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP Business Intelligence
  PublisherName: SAP Business Intelligence
  ServiceCategory: Developer Tools / API
  ServiceName: SAP Business Intelligence
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
name: Sap Bi Finops
provider_name: SAP Business Intelligence
provider_slug: sap-bi
publisher_name: SAP Business Intelligence
service_category: API
slug: sap-bi-finops
source_filename: sap-bi-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Business Intelligence\nproviderId: sap-bi\npublisherName: SAP Business Intelligence\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Data Visualization\n  - Reporting\n  - SAP\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Business Intelligence API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Business Intelligence\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Business Intelligence\n  PublisherName: SAP Business Intelligence\n  InvoiceIssuerName: SAP Business Intelligence\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n \
  \ - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Analytics Cloud API\n    baseURL: https://[tenant].sapanalytics.cloud/api/v1\n    tags:\n      - Analytics\n      - Cloud\n      - Dashboards\n    serviceName: SAP Analytics Cloud API\n    serviceCategory: API\n  - name: SAP BusinessObjects BI Platform REST API\n    baseURL: https://[server]:[port]/biprws\n    tags:\n      - BusinessObjects\n      - Platform Administration\n      - Reports\n    serviceName: SAP BusinessObjects BI Platform REST API\n    serviceCategory: API\n  - name: SAP HANA XS Advanced API\n    baseURL: https://[host]:[port]\n    tags:\n      - Analytics\n\
  \      - Database\n      - HANA\n      - XS Advanced\n    serviceName: SAP HANA XS Advanced API\n    serviceCategory: API\n  - name: SAP BW/4HANA OData API\n    baseURL: https://[server]:[port]/sap/opu/odata/sap/\n    tags:\n      - BW/4HANA\n      - Data Warehouse\n      - ETL\n      - OData\n    serviceName: SAP BW/4HANA OData API\n    serviceCategory: API\n  - name: SAP Datasphere API\n    baseURL: https://[tenant].datasphere.cloud.sap/api/v1\n    tags:\n      - Cloud\n      - Data Integration\n      - Data Warehouse\n      - Datasphere\n    serviceName: SAP Datasphere API\n    serviceCategory: API\n  - name: SAP Crystal Reports API\n    baseURL: https://[server]/crystal/\n    tags:\n      - Crystal Reports\n      - Embedded Analytics\n      - Reporting\n    serviceName: SAP Crystal Reports API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-bi/refs/heads/main/finops/sap-bi-finops.yml
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
