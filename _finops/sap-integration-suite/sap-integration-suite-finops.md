---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: sap-integration-suite-cloud-integration-openapi.yml
  format: yaml
  label: SAP Cloud Integration API
  slug: sap-cloud-integration
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-integration-suite/refs/heads/main/openapi/sap-integration-suite-cloud-integration-openapi.yml
- filename: sap-integration-suite-api-management-openapi.yml
  format: yaml
  label: SAP API Management API
  slug: sap-api-management
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/sap-integration-suite/refs/heads/main/openapi/sap-integration-suite-api-management-openapi.yml
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
description: FinOps framework definition for the SAP Integration Suite API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: SAP Integration Suite
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: SAP Integration Suite
  PublisherName: SAP Integration Suite
  ServiceCategory: Developer Tools / API
  ServiceName: SAP Integration Suite
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
name: Sap Integration Suite Finops
provider_name: SAP Integration Suite
provider_slug: sap-integration-suite
publisher_name: SAP Integration Suite
service_category: API
slug: sap-integration-suite-finops
source_filename: sap-integration-suite-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: SAP Integration Suite\nproviderId: sap-integration-suite\npublisherName: SAP Integration Suite\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Management\n  - Cloud Integration\n  - Enterprise Integration\n  - Event Mesh\n  - iPaaS\n  - SAP\n  - SAP BTP\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the SAP Integration Suite API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n   \
  \   real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      -\
  \ Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: SAP Integration Suite\n  ServiceCategory: Developer Tools / API\n  ProviderName: SAP Integration Suite\n  PublisherName: SAP Integration Suite\n  InvoiceIssuerName: SAP Integration Suite\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n\
  \      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: SAP Cloud Integration API\n    baseURL: https://{host}/api/v1\n    tags:\n      - Cloud Integration\n      - Integration Flows\n      - OData\n      - Runtime Monitoring\n    serviceName: SAP Cloud Integration API\n    serviceCategory: API\n  - name: SAP API Management API\n    baseURL: https://{api-portal-host}/apiportal/api/1.0\n    tags:\n      - API Gateway\n      - API Management\n      - API Proxy\n      - Developer Portal\n      - OData\n    serviceName: SAP API Management API\n    serviceCategory: API\n  - name: SAP Integration Advisor API\n    baseURL:\
  \ https://{host}/api\n    tags:\n      - B2B Integration\n      - EDI\n      - Integration Advisor\n      - Mapping Guidelines\n      - Message Implementation Guidelines\n    serviceName: SAP Integration Advisor API\n    serviceCategory: API\n  - name: SAP Open Connectors API\n    baseURL: https://api.openconnectors.ext.hana.ondemand.com\n    tags:\n      - Cloud Connectors\n      - Normalization\n      - Open Connectors\n      - Third-Party Integration\n      - Unified API\n    serviceName: SAP Open Connectors API\n    serviceCategory: API\n  - name: SAP Trading Partner Management API\n    baseURL: https://{host}/api\n    tags:\n      - AS2\n      - B2B\n      - EDI\n      - Trading Partner Management\n    serviceName: SAP Trading Partner Management API\n    serviceCategory: API\n  - name: SAP Event Mesh API\n    baseURL: https://enterprise-messaging.cfapps.sap.hana.ondemand.com\n    tags:\n      - Asynchronous\n      - CloudEvents\n      - Event Mesh\n      - Messaging\n      - Pub/Sub\n\
  \    serviceName: SAP Event Mesh API\n    serviceCategory: API\n  - name: SAP Integration Suite Advanced Event Mesh API\n    baseURL: https://api.solacecloud.com/api/v2\n    tags:\n      - Advanced Event Mesh\n      - Broker Management\n      - Event Streaming\n      - Messaging\n      - REST\n    serviceName: SAP Integration Suite Advanced Event Mesh API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/sap-integration-suite/refs/heads/main/finops/sap-integration-suite-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Management
- Cloud Integration
- Enterprise Integration
- Event Mesh
- iPaaS
- SAP
- SAP BTP
- FinOps
- Cost Management
- FOCUS
---
