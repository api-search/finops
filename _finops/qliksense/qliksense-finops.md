---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Qlik Sense APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Qlik Sense APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Qlik Sense APIs
  PublisherName: Qlik Sense APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Qlik Sense APIs
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
name: Qliksense Finops
provider_name: Qlik Sense APIs
provider_slug: qliksense
publisher_name: Qlik Sense APIs
service_category: API
slug: qliksense-finops
source_filename: qliksense-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Qlik Sense APIs\nproviderId: qliksense\npublisherName: Qlik Sense APIs\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Cloud\n  - Data Visualization\n  - Enterprise\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Qlik Sense APIs API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Qlik Sense APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Qlik Sense APIs\n  PublisherName: Qlik Sense APIs\n  InvoiceIssuerName: Qlik Sense APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Qlik Engine API\n    baseURL: wss://your-tenant.qlikcloud.com/app/\n    tags:\n      - Analytics\n      - Business Intelligence\n      - JSON-RPC\n      - WebSocket\n    serviceName: Qlik Engine API\n    serviceCategory: API\n  - name: Qlik Apps API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/apps\n    tags:\n      - Applications\n      - Apps\n      - Cloud\n      - REST\n    serviceName: Qlik Apps API\n    serviceCategory: API\n  - name: Qlik Users API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/users\n    tags:\n      - Identity\n      - REST\n      - Users\n    serviceName: Qlik Users API\n    serviceCategory: API\n\
  \  - name: Qlik Spaces API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/spaces\n    tags:\n      - Collaboration\n      - Organization\n      - REST\n      - Spaces\n    serviceName: Qlik Spaces API\n    serviceCategory: API\n  - name: Qlik Data Connections API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/data-connections\n    tags:\n      - Connections\n      - Data\n      - Integration\n      - REST\n    serviceName: Qlik Data Connections API\n    serviceCategory: API\n  - name: Qlik Automations API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/automations\n    tags:\n      - Automations\n      - No-Code\n      - REST\n      - Workflows\n    serviceName: Qlik Automations API\n    serviceCategory: API\n  - name: Qlik Reload API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/reloads\n    tags:\n      - Data\n      - ETL\n      - Reload\n      - REST\n    serviceName: Qlik Reload API\n    serviceCategory: API\n  - name: Qlik Webhooks API\n    baseURL:\
  \ https://your-tenant.qlikcloud.com/api/v1/webhooks\n    tags:\n      - Events\n      - Real-Time\n      - REST\n      - Webhooks\n    serviceName: Qlik Webhooks API\n    serviceCategory: API\n  - name: Qlik Reports API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/reports\n    tags:\n      - Export\n      - Reports\n      - REST\n    serviceName: Qlik Reports API\n    serviceCategory: API\n  - name: Qlik Machine Learning API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/ml\n    tags:\n      - AI\n      - Machine Learning\n      - Predictions\n      - REST\n    serviceName: Qlik Machine Learning API\n    serviceCategory: API\n  - name: Qlik Natural Language API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/questions\n    tags:\n      - AI\n      - Natural Language\n      - NLP\n      - REST\n    serviceName: Qlik Natural Language API\n    serviceCategory: API\n  - name: Qlik Tenants API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/tenants\n    tags:\n\
  \      - Administration\n      - Configuration\n      - REST\n      - Tenants\n    serviceName: Qlik Tenants API\n    serviceCategory: API\n  - name: Qlik Audits API\n    baseURL: https://your-tenant.qlikcloud.com/api/v1/audits\n    tags:\n      - Audits\n      - Compliance\n      - Logging\n      - REST\n    serviceName: Qlik Audits API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/qliksense/refs/heads/main/finops/qliksense-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Cloud
- Data Visualization
- Enterprise
- FinOps
- Cost Management
- FOCUS
---
