---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amazon-connect-openapi.yml
  format: yaml
  label: Amazon Connect Service API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amazon-connect/refs/heads/main/openapi/amazon-connect-openapi.yml
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
description: FinOps framework definition for the Amazon Connect API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amazon Connect
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amazon Connect
  PublisherName: Amazon Connect
  ServiceCategory: Developer Tools / API
  ServiceName: Amazon Connect
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
name: Amazon Connect Finops
provider_name: Amazon Connect
provider_slug: amazon-connect
publisher_name: Amazon Connect
service_category: API
slug: amazon-connect-finops
source_filename: amazon-connect-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amazon Connect\nproviderId: amazon-connect\npublisherName: Amazon Connect\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AWS\n  - Chat\n  - Contact Center\n  - Customer Service\n  - Voice\n  - AI\n  - Omnichannel\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amazon Connect API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amazon Connect\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amazon Connect\n  PublisherName: Amazon Connect\n  InvoiceIssuerName: Amazon Connect\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network\
  \ in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amazon Connect Service API\n    baseURL: https://connect.amazonaws.com\n    tags:\n      - Contact Center\n      - AWS\n      - Voice\n      - Chat\n    serviceName: Amazon Connect Service API\n    serviceCategory: API\n  - name: Amazon Connect Streams SDK\n    baseURL: https://github.com/amazon-connect/amazon-connect-streams\n    tags:\n      - SDK\n      - JavaScript\n      - Browser\n      - Contact Center\n    serviceName: Amazon Connect Streams SDK\n    serviceCategory: API\n  - name: Amazon AppIntegrations API\n    baseURL: https://app-integrations.amazonaws.com\n    tags:\n      - Integrations\n      - AWS\n      - Contact Center\n    serviceName:\
  \ Amazon AppIntegrations API\n    serviceCategory: API\n  - name: Amazon Connect Contact Lens API\n    baseURL: https://contact-lens.amazonaws.com\n    tags:\n      - Analytics\n      - AI\n      - Contact Center\n      - NLP\n    serviceName: Amazon Connect Contact Lens API\n    serviceCategory: API\n  - name: Amazon Connect Outbound Campaigns API\n    baseURL: https://connect-campaigns.amazonaws.com\n    tags:\n      - Outbound\n      - Campaigns\n      - Contact Center\n    serviceName: Amazon Connect Outbound Campaigns API\n    serviceCategory: API\n  - name: Amazon Connect Outbound Campaigns V2 API\n    baseURL: https://connect-campaigns.amazonaws.com\n    tags:\n      - Outbound\n      - Campaigns\n      - Contact Center\n    serviceName: Amazon Connect Outbound Campaigns V2 API\n    serviceCategory: API\n  - name: Amazon Connect Cases API\n    baseURL: https://cases.amazonaws.com\n    tags:\n      - Cases\n      - Case Management\n      - Contact Center\n    serviceName: Amazon\
  \ Connect Cases API\n    serviceCategory: API\n  - name: Amazon Connect Participant Service API\n    baseURL: https://participant.connect.amazonaws.com\n    tags:\n      - Chat\n      - Participants\n      - Contact Center\n    serviceName: Amazon Connect Participant Service API\n    serviceCategory: API\n  - name: Amazon Connect Customer Profiles API\n    baseURL: https://profile.profile.amazonaws.com\n    tags:\n      - Customer Profiles\n      - CRM\n      - Contact Center\n    serviceName: Amazon Connect Customer Profiles API\n    serviceCategory: API\n  - name: Amazon Q Connect API\n    baseURL: https://wisdom.amazonaws.com\n    tags:\n      - AI\n      - Generative AI\n      - Agent Assist\n      - Contact Center\n    serviceName: Amazon Q Connect API\n    serviceCategory: API\n  - name: Amazon Voice ID API\n    baseURL: https://voiceid.amazonaws.com\n    tags:\n      - Voice\n      - Authentication\n      - Fraud Detection\n      - Contact Center\n    serviceName: Amazon Voice ID\
  \ API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amazon-connect/refs/heads/main/finops/amazon-connect-finops.yml
sources: []
specification: FinOps Framework
tags:
- Chat
- Contact Center
- Customer Service
- Voice
- AI
- Omnichannel
- FinOps
- Cost Management
- FOCUS
---
