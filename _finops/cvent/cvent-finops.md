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
description: FinOps framework definition for the Cvent API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Cvent
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Cvent
  PublisherName: Cvent
  ServiceCategory: Developer Tools / API
  ServiceName: Cvent
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
name: Cvent Finops
provider_name: Cvent
provider_slug: cvent
publisher_name: Cvent
service_category: API
slug: cvent-finops
source_filename: cvent-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Cvent\nproviderId: cvent\npublisherName: Cvent\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Attendee Hub\n  - Attendee Management\n  - Conferences\n  - Diagramming\n  - Event Management\n  - Event Marketing\n  - Events\n  - Exhibitors\n  - Hospitality\n  - Hospitality Cloud\n  - Hybrid Events\n  - Meetings\n  - OAuth 2.0\n  - Passkey\n  - Registration\n  - REST API\n  - SOAP API\n  - SSO\n  - Supplier Network\n  - Surveys\n  - Venue Management\n  - Venue Sourcing\n  - Virtual Events\n  - Webhooks\n  - White Label\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Cvent API surface. Provides a FOCUS-aligned mapping\
  \ for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n \
  \     - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Cvent\n  ServiceCategory: Developer Tools / API\n  ProviderName: Cvent\n  PublisherName: Cvent\n  InvoiceIssuerName: Cvent\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name:\
  \ api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Cvent REST API\n    baseURL: https://api-platform.cvent.com\n    tags:\n      - Attendees\n      - Contacts\n      - Events\n      - OAuth 2.0\n      - Registration\n      - REST\n      - Sessions\n      - Surveys\n      - Webhooks\n    serviceName: Cvent REST API\n    serviceCategory: API\n  - name: Cvent Webhooks API\n    baseURL: ''\n    tags:\n      - Attendees\n      - Events\n\
  \      - Notifications\n      - Sessions\n      - Webhooks\n    serviceName: Cvent Webhooks API\n    serviceCategory: API\n  - name: Cvent Supplier Network (CSN) API\n    baseURL: ''\n    tags:\n      - Hospitality\n      - Proposals\n      - RFP\n      - Suppliers\n      - Venues\n    serviceName: Cvent Supplier Network (CSN) API\n    serviceCategory: API\n  - name: Cvent Passkey RegLink API\n    baseURL: ''\n    tags:\n      - Accommodations\n      - Hotels\n      - Registration\n      - Reservations\n    serviceName: Cvent Passkey RegLink API\n    serviceCategory: API\n  - name: Cvent SOAP API (Legacy)\n    baseURL: ''\n    tags:\n      - Contacts\n      - Deprecated\n      - Events\n      - Legacy\n      - Registration\n      - SOAP\n    serviceName: Cvent SOAP API (Legacy)\n    serviceCategory: API\n  - name: Cvent Custom Widgets API\n    baseURL: ''\n    tags:\n      - Customization\n      - Embedding\n      - Registration\n      - Widgets\n    serviceName: Cvent Custom Widgets API\n\
  \    serviceCategory: API\n  - name: Cvent Single Sign-On (SSO) Integration\n    baseURL: ''\n    tags:\n      - Authentication\n      - Identity\n      - OpenID Connect\n      - SAML\n      - SSO\n    serviceName: Cvent Single Sign-On (SSO) Integration\n    serviceCategory: API\n  - name: Cvent White Label API\n    baseURL: ''\n    tags:\n      - Branding\n      - RFP\n      - White Label\n      - Widgets\n    serviceName: Cvent White Label API\n    serviceCategory: API\n  - name: Cvent Salesforce App\n    baseURL: ''\n    tags:\n      - CRM\n      - Events\n      - Integration\n      - Salesforce\n    serviceName: Cvent Salesforce App\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - FN: Cvent Developer Relations\n    email: developersupport@cvent.com\n\
  \    url: https://developers.cvent.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/cvent/refs/heads/main/finops/cvent-finops.yml
sources: []
specification: FinOps Framework
tags:
- Attendee Hub
- Attendee Management
- Conferences
- Diagramming
- Event Management
- Event Marketing
- Events
- Exhibitors
- Hospitality
- Hospitality Cloud
- Hybrid Events
- Meetings
- OAuth 2.0
- Passkey
- Registration
- REST API
- SOAP API
- SSO
- Supplier Network
- Surveys
- Venue Management
- Venue Sourcing
- Virtual Events
- Webhooks
- White Label
- FinOps
- Cost Management
- FOCUS
---
