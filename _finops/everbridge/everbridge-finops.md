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
  label: Everbridge Suite API
  slug: ''
  spec_type: OpenAPI
  url: https://api.everbridge.net/rest/swagger.json
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
description: FinOps framework definition for the Everbridge API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Everbridge
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Everbridge
  PublisherName: Everbridge
  ServiceCategory: Developer Tools / API
  ServiceName: Everbridge
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
name: Everbridge Finops
provider_name: Everbridge
provider_slug: everbridge
publisher_name: Everbridge
service_category: API
slug: everbridge-finops
source_filename: everbridge-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Everbridge\nproviderId: everbridge\npublisherName: Everbridge\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Critical Event Management\n  - Emergency Management\n  - Incident Management\n  - IT Alerting\n  - Mass Notification\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Everbridge API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Everbridge\n  ServiceCategory: Developer Tools / API\n  ProviderName: Everbridge\n  PublisherName: Everbridge\n  InvoiceIssuerName: Everbridge\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Everbridge Suite API\n    baseURL: https://api.everbridge.net/rest\n    tags:\n      - Contacts\n      - Groups\n      - Incidents\n      - Mass Notification\n      - Notifications\n      - Organizations\n    serviceName: Everbridge Suite API\n    serviceCategory: API\n  - name: Everbridge Asset Management API\n    baseURL: https://api.everbridge.net/rest\n    tags:\n      - Asset Management\n      - Assets\n      - Critical Events\n    serviceName: Everbridge Asset Management API\n    serviceCategory: API\n  - name: Everbridge Asset Query API\n    baseURL: https://api.everbridge.net/rest\n    tags:\n      - Assets\n      - Queries\n      - Search\n    serviceName:\
  \ Everbridge Asset Query API\n    serviceCategory: API\n  - name: Everbridge CEM Alerts API\n    baseURL: https://api.everbridge.net\n    tags:\n      - Alerts\n      - Critical Events\n      - GraphQL\n      - Risk Intelligence\n    serviceName: Everbridge CEM Alerts API\n    serviceCategory: API\n  - name: Everbridge SnapComms API\n    baseURL: https://api.snapcomms.com\n    tags:\n      - Desktop Alerts\n      - Employee Communications\n      - Internal Communications\n    serviceName: Everbridge SnapComms API\n    serviceCategory: API\n  - name: Everbridge Digital Apps API\n    baseURL: https://api.everbridge.net\n    tags:\n      - Contacts\n      - Digital Apps\n      - Mobile\n      - Push Notifications\n    serviceName: Everbridge Digital Apps API\n    serviceCategory: API\n  - name: Everbridge Communications API\n    baseURL: https://api.everbridge.net\n    tags:\n      - Communications\n      - Messaging\n      - Templates\n    serviceName: Everbridge Communications API\n   \
  \ serviceCategory: API\n  - name: Everbridge iPaaS API\n    baseURL: https://ipaas-ingestion.everbridge.net\n    tags:\n      - Integration\n      - iPaaS\n      - IT Alerting\n      - ITSM\n    serviceName: Everbridge iPaaS API\n    serviceCategory: API\n  - name: Everbridge Safety Devices API\n    baseURL: https://api.everbridge.net\n    tags:\n      - Devices\n      - IoT\n      - Safety\n    serviceName: Everbridge Safety Devices API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/everbridge/refs/heads/main/finops/everbridge-finops.yml
sources: []
specification: FinOps Framework
tags:
- Critical Event Management
- Emergency Management
- Incident Management
- IT Alerting
- Mass Notification
- FinOps
- Cost Management
- FOCUS
---
