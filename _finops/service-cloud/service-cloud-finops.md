---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Service Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://api.salesforce.com/service-cloud/openapi.json
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
description: FinOps framework definition for the Salesforce Service Cloud APIs API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Service Cloud APIs
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Service Cloud APIs
  PublisherName: Salesforce Service Cloud APIs
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Service Cloud APIs
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
name: Service Cloud Finops
provider_name: Salesforce Service Cloud APIs
provider_slug: service-cloud
publisher_name: Salesforce Service Cloud APIs
service_category: API
slug: service-cloud-finops
source_filename: service-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Service Cloud APIs\nproviderId: service-cloud\npublisherName: Salesforce Service Cloud APIs\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud\n  - CRM\n  - Customer-Service\n  - Enterprise\n  - Salesforce\n  - Support\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Service Cloud APIs API surface. Provides a\n  FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the\n  provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Service Cloud APIs\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Service Cloud APIs\n  PublisherName: Salesforce Service Cloud APIs\n  InvoiceIssuerName: Salesforce Service Cloud APIs\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n\
  \      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Service Cloud REST API\n    baseURL: ''\n    tags:\n      - Cases\n      - CRM\n      - Customers\n      - REST\n      - Support\n    serviceName: Service Cloud REST API\n    serviceCategory: API\n  - name: Service Cloud Case Management API\n    baseURL: ''\n    tags:\n      - Cases\n      - Escalation\n      - Routing\n      - Tickets\n    serviceName: Service Cloud Case Management API\n    serviceCategory: API\n  - name: Service Cloud Knowledge API\n    baseURL: ''\n    tags:\n      - Articles\n      - Documentation\n      - Knowledge\n    \
  \  - Self-Service\n    serviceName: Service Cloud Knowledge API\n    serviceCategory: API\n  - name: Service Cloud Omni-Channel API\n    baseURL: ''\n    tags:\n      - Omnichannel\n      - Presence\n      - Routing\n      - Workforce\n    serviceName: Service Cloud Omni-Channel API\n    serviceCategory: API\n  - name: Service Cloud Live Agent API\n    baseURL: ''\n    tags:\n      - Chat\n      - Live-Agent\n      - Messaging\n      - Real-Time\n    serviceName: Service Cloud Live Agent API\n    serviceCategory: API\n  - name: Service Cloud Einstein Bots API\n    baseURL: ''\n    tags:\n      - AI\n      - Automation\n      - Bots\n      - Chatbots\n      - Einstein\n    serviceName: Service Cloud Einstein Bots API\n    serviceCategory: API\n  - name: Service Cloud Streaming API\n    baseURL: ''\n    tags:\n      - Events\n      - Push-Notifications\n      - Real-Time\n      - Streaming\n    serviceName: Service Cloud Streaming API\n    serviceCategory: API\n  - name: Service Cloud CTI\
  \ API\n    baseURL: ''\n    tags:\n      - Call-Center\n      - CTI\n      - Phone\n      - Telephony\n    serviceName: Service Cloud CTI API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Salesforce\n    email: developer@salesforce.com\n    url: https://developer.salesforce.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/service-cloud/refs/heads/main/finops/service-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud
- CRM
- Customer-Service
- Enterprise
- Salesforce
- Support
- FinOps
- Cost Management
- FOCUS
---
