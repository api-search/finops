---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-business-one-service-layer-openapi.yml
  format: yaml
  label: SAP Business One Service Layer API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/openapi/sap-business-one-service-layer-openapi.yml
- filename: sap-s4hana-cloud-business-partner-openapi.yml
  format: yaml
  label: SAP S/4HANA Cloud API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/openapi/sap-s4hana-cloud-business-partner-openapi.yml
- filename: sap-event-mesh-asyncapi.yml
  format: yaml
  label: SAP Event Mesh API
  slug: ''
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/asyncapi/sap-event-mesh-asyncapi.yml
- filename: sap-ai-core-openapi.yml
  format: yaml
  label: SAP AI Core API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/openapi/sap-ai-core-openapi.yml
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
description: FinOps framework definition for the SAP API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP
  PublisherName: SAP
  ServiceCategory: Developer Tools / API
  ServiceName: SAP
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
name: Sap Finops
provider_name: SAP
provider_slug: sap
publisher_name: SAP
service_category: API
slug: sap-finops
source_filename: sap-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP\nproviderId: sap\npublisherName: SAP\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - BTP\n  - Business Applications\n  - Cloud\n  - Data Management\n  - Enterprise\n  - ERP\n  - Integration\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP\n  PublisherName: SAP\n  InvoiceIssuerName: SAP\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Business One Service Layer API\n    baseURL: ''\n    tags:\n      - Business Management\n      - Enterprise\n      - ERP\n    serviceName: SAP Business One Service Layer API\n    serviceCategory: API\n  - name: SAP S/4HANA Cloud API\n    baseURL: ''\n    tags:\n      - Cloud\n      - Enterprise Resource Planning\n      - ERP\n      - S/4HANA\n    serviceName: SAP S/4HANA Cloud API\n    serviceCategory: API\n  - name: SAP SuccessFactors API\n    baseURL: ''\n    tags:\n      - HCM\n      - HR\n      - Human Resources\n      - Talent Management\n    serviceName: SAP SuccessFactors API\n    serviceCategory: API\n  - name: SAP Ariba APIs\n    baseURL: ''\n    tags:\n      - Procurement\n      - Sourcing\n      - Supplier\
  \ Management\n      - Supply Chain\n    serviceName: SAP Ariba APIs\n    serviceCategory: API\n  - name: SAP Cloud Platform Integration Suite\n    baseURL: ''\n    tags:\n      - Cloud Platform\n      - Integration\n      - iPaaS\n      - Middleware\n    serviceName: SAP Cloud Platform Integration Suite\n    serviceCategory: API\n  - name: SAP Commerce Cloud API\n    baseURL: ''\n    tags:\n      - Commerce\n      - E-Commerce\n      - OCC\n      - Retail\n    serviceName: SAP Commerce Cloud API\n    serviceCategory: API\n  - name: SAP Analytics Cloud API\n    baseURL: ''\n    tags:\n      - Analytics\n      - BI\n      - Business Intelligence\n      - Planning\n    serviceName: SAP Analytics Cloud API\n    serviceCategory: API\n  - name: SAP Concur API\n    baseURL: ''\n    tags:\n      - Concur\n      - Expense Management\n      - Invoice\n      - Travel\n    serviceName: SAP Concur API\n    serviceCategory: API\n  - name: SAP Fieldglass API\n    baseURL: ''\n    tags:\n      - Contingent\
  \ Workforce\n      - External Workers\n      - Vendor Management\n      - VMS\n    serviceName: SAP Fieldglass API\n    serviceCategory: API\n  - name: SAP BTP Core Services API\n    baseURL: ''\n    tags:\n      - BTP\n      - Cloud Management\n      - Cloud Platform\n      - Platform Services\n    serviceName: SAP BTP Core Services API\n    serviceCategory: API\n  - name: SAP Datasphere API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Data Integration\n      - Data Warehousing\n      - Datasphere\n    serviceName: SAP Datasphere API\n    serviceCategory: API\n  - name: SAP Event Mesh API\n    baseURL: ''\n    tags:\n      - AMQP\n      - Event-Driven\n      - Messaging\n      - MQTT\n    serviceName: SAP Event Mesh API\n    serviceCategory: API\n  - name: SAP Master Data Integration API\n    baseURL: ''\n    tags:\n      - Data Integration\n      - Data Quality\n      - Master Data\n      - MDI\n    serviceName: SAP Master Data Integration API\n    serviceCategory: API\n \
  \ - name: SAP Signavio Process Manager API\n    baseURL: ''\n    tags:\n      - BPM\n      - BPMN\n      - Process Management\n      - Process Mining\n    serviceName: SAP Signavio Process Manager API\n    serviceCategory: API\n  - name: SAP Document Management Service API\n    baseURL: ''\n    tags:\n      - BTP\n      - CMIS\n      - Content Management\n      - Document Management\n    serviceName: SAP Document Management Service API\n    serviceCategory: API\n  - name: SAP Integration Suite API Management\n    baseURL: ''\n    tags:\n      - API Gateway\n      - API Management\n      - API Proxy\n      - Integration Suite\n    serviceName: SAP Integration Suite API Management\n    serviceCategory: API\n  - name: SAP AI Core API\n    baseURL: ''\n    tags:\n      - AI Core\n      - Artificial Intelligence\n      - BTP\n      - Machine Learning\n    serviceName: SAP AI Core API\n    serviceCategory: API\n  - name: SAP Emarsys Customer Engagement API\n    baseURL: ''\n    tags:\n     \
  \ - CRM\n      - Customer Engagement\n      - Email Marketing\n      - Marketing Automation\n    serviceName: SAP Emarsys Customer Engagement API\n    serviceCategory: API\n  - name: SAP Build Work Zone API\n    baseURL: ''\n    tags:\n      - BTP\n      - Digital Workplace\n      - Portal\n      - Work Zone\n    serviceName: SAP Build Work Zone API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap/refs/heads/main/finops/sap-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- BTP
- Business Applications
- Cloud
- Data Management
- Enterprise
- ERP
- Integration
- FinOps
- Cost Management
- FOCUS
---
