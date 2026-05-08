---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-marketing-cloud-openapi.yml
  format: yaml
  label: Marketing Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-marketing-cloud/refs/heads/main/openapi/salesforce-marketing-cloud-openapi.yml
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
description: FinOps framework definition for the Salesforce Marketing Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Marketing Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Marketing Cloud
  PublisherName: Salesforce Marketing Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Marketing Cloud
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
name: Salesforce Marketing Cloud Finops
provider_name: Salesforce Marketing Cloud
provider_slug: salesforce-marketing-cloud
publisher_name: Salesforce Marketing Cloud
service_category: API
slug: salesforce-marketing-cloud-finops
source_filename: salesforce-marketing-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Marketing Cloud\nproviderId: salesforce-marketing-cloud\npublisherName: Salesforce Marketing Cloud\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Automation\n  - Customer Journey\n  - Digital Marketing\n  - Email\n  - Marketing\n  - Personalization\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Marketing Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Marketing Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Marketing Cloud\n  PublisherName: Salesforce Marketing Cloud\n  InvoiceIssuerName: Salesforce Marketing Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n    \
  \  - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Marketing Cloud REST API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com\n    tags:\n      - Email\n      - Push\n      - REST\n      - SMS\n    serviceName: Marketing Cloud REST API\n    serviceCategory: API\n  - name: SOAP API\n    baseURL: https://YOUR_SUBDOMAIN.soap.marketingcloudapis.com\n    tags:\n      - Legacy\n      - SOAP\n      - Subscriber\n    serviceName: SOAP API\n    serviceCategory: API\n  - name: Transactional Messaging API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/messaging/v1\n\
  \    tags:\n      - Messaging\n      - Transactional\n      - Triggered\n    serviceName: Transactional Messaging API\n    serviceCategory: API\n  - name: Journey Builder API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/interaction/v1\n    tags:\n      - Automation\n      - Journey\n      - Orchestration\n    serviceName: Journey Builder API\n    serviceCategory: API\n  - name: Data Extensions API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/data/v1\n    tags:\n      - Data\n      - Segmentation\n      - Storage\n    serviceName: Data Extensions API\n    serviceCategory: API\n  - name: Email Send Definition API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/messaging/v1\n    tags:\n      - Campaigns\n      - Email\n      - Sending\n    serviceName: Email Send Definition API\n    serviceCategory: API\n  - name: Mobile Push API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/push/v1\n    tags:\n      - Mobile\n  \
  \    - Notifications\n      - Push\n    serviceName: Mobile Push API\n    serviceCategory: API\n  - name: SMS/MMS API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/sms/v1\n    tags:\n      - MMS\n      - Mobile Messaging\n      - SMS\n    serviceName: SMS/MMS API\n    serviceCategory: API\n  - name: Asset API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/asset/v1\n    tags:\n      - Assets\n      - Content\n      - Templates\n    serviceName: Asset API\n    serviceCategory: API\n  - name: Einstein Recommendations API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/einstein/v1\n    tags:\n      - AI\n      - Personalization\n      - Recommendations\n    serviceName: Einstein Recommendations API\n    serviceCategory: API\n  - name: Content Builder API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/asset/v1\n    tags:\n      - Assets\n      - Content\n      - Email\n      - Templates\n    serviceName: Content Builder\
  \ API\n    serviceCategory: API\n  - name: Contacts API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/contacts/v1\n    tags:\n      - Contacts\n      - Data\n      - Subscribers\n    serviceName: Contacts API\n    serviceCategory: API\n  - name: Automation Studio API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/automation/v1\n    tags:\n      - Automation\n      - Scheduling\n      - Workflows\n    serviceName: Automation Studio API\n    serviceCategory: API\n  - name: Campaign API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/hub/v1\n    tags:\n      - Campaigns\n      - Execution\n      - Marketing\n    serviceName: Campaign API\n    serviceCategory: API\n  - name: Event Notification Service API\n    baseURL: https://YOUR_SUBDOMAIN.rest.marketingcloudapis.com/platform/v1\n    tags:\n      - Events\n      - Notifications\n      - Real-Time\n      - Webhooks\n    serviceName: Event Notification Service API\n    serviceCategory:\
  \ API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-marketing-cloud/refs/heads/main/finops/salesforce-marketing-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Customer Journey
- Digital Marketing
- Email
- Marketing
- Personalization
- FinOps
- Cost Management
- FOCUS
---
