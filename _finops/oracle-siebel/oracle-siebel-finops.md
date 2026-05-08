---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.json
  format: json
  label: Oracle Siebel REST API
  slug: ''
  spec_type: OpenAPI
  url: https://{siebel-server}/siebel/v1.0/swagger.json
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
description: FinOps framework definition for the Oracle Siebel API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Oracle Siebel
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Oracle Siebel
  PublisherName: Oracle Siebel
  ServiceCategory: Developer Tools / API
  ServiceName: Oracle Siebel
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
name: Oracle Siebel Finops
provider_name: Oracle Siebel
provider_slug: oracle-siebel
publisher_name: Oracle Siebel
service_category: API
slug: oracle-siebel-finops
source_filename: oracle-siebel-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Oracle Siebel\nproviderId: oracle-siebel\npublisherName: Oracle Siebel\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CRM\n  - Customer Management\n  - Enterprise Software\n  - Marketing Automation\n  - Oracle\n  - Sales Automation\n  - Service Automation\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Oracle Siebel API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Oracle Siebel\n  ServiceCategory: Developer Tools / API\n  ProviderName: Oracle Siebel\n  PublisherName: Oracle Siebel\n  InvoiceIssuerName: Oracle Siebel\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n   \
  \ description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Oracle Siebel REST API\n    baseURL: https://{siebel-server}/siebel/v1.0\n    tags:\n      - CRM\n      - Customer Management\n      - Integration\n      - REST\n      - Sales\n    serviceName: Oracle Siebel REST API\n    serviceCategory: API\n  - name: Oracle Siebel SOAP Web Services\n    baseURL: https://{siebel-server}/siebel/app/soap/services\n    tags:\n      - CRM\n      - Enterprise Integration\n      - SOAP\n      - Web Services\n    serviceName: Oracle Siebel SOAP Web Services\n    serviceCategory: API\n  - name: Oracle Siebel Business Service API\n    baseURL: ''\n    tags:\n      - Business\
  \ Services\n      - Custom Logic\n      - Integration\n    serviceName: Oracle Siebel Business Service API\n    serviceCategory: API\n  - name: Oracle Siebel EAI (Enterprise Application Integration)\n    baseURL: ''\n    tags:\n      - Data Exchange\n      - EAI\n      - Integration\n      - Middleware\n    serviceName: Oracle Siebel EAI (Enterprise Application Integration)\n    serviceCategory: API\n  - name: Oracle Siebel Object Interfaces API\n    baseURL: ''\n    tags:\n      - Business Components\n      - Java Data Bean\n      - Object Interfaces\n      - Scripting\n    serviceName: Oracle Siebel Object Interfaces API\n    serviceCategory: API\n  - name: Oracle Siebel Open UI JavaScript API\n    baseURL: ''\n    tags:\n      - Customization\n      - JavaScript\n      - Open UI\n      - User Interface\n    serviceName: Oracle Siebel Open UI JavaScript API\n    serviceCategory: API\n  - name: Oracle Siebel Event Pub/Sub API\n    baseURL: ''\n    tags:\n      - Event-Driven\n      -\
  \ Kafka\n      - Pub/Sub\n      - Real-Time Integration\n    serviceName: Oracle Siebel Event Pub/Sub API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/oracle-siebel/refs/heads/main/finops/oracle-siebel-finops.yml
sources: []
specification: FinOps Framework
tags:
- CRM
- Customer Management
- Enterprise Software
- Marketing Automation
- Oracle
- Sales Automation
- Service Automation
- FinOps
- Cost Management
- FOCUS
---
