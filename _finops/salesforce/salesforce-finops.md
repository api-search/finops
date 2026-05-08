---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-openapi.yml
  format: yaml
  label: Salesforce REST API
  slug: salesforce-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-openapi.yml
- filename: salesforce-bulk-api-2-openapi.yml
  format: yaml
  label: Salesforce Bulk API 2.0
  slug: salesforce-bulk-api-2
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-bulk-api-2-openapi.yml
- filename: salesforce-streaming-asyncapi.yml
  format: yaml
  label: Salesforce Streaming API
  slug: salesforce-streaming-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/asyncapi/salesforce-streaming-asyncapi.yml
- filename: salesforce-platform-events-asyncapi.yml
  format: yaml
  label: Salesforce Platform Events API
  slug: salesforce-platform-events-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/asyncapi/salesforce-platform-events-asyncapi.yml
- filename: salesforce-change-data-capture-asyncapi.yml
  format: yaml
  label: Salesforce Change Data Capture API
  slug: salesforce-change-data-capture-api
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/asyncapi/salesforce-change-data-capture-asyncapi.yml
- filename: salesforce-ui-api-openapi.yml
  format: yaml
  label: Salesforce UI API
  slug: salesforce-ui-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-ui-api-openapi.yml
- filename: salesforce-marketing-cloud-rest-openapi.yml
  format: yaml
  label: Salesforce Marketing Cloud REST API
  slug: salesforce-marketing-cloud-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-marketing-cloud-rest-openapi.yml
- filename: salesforce-openapi.yml
  format: yaml
  label: Salesforce
  slug: salesforce-salesforce
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/openapi/salesforce-openapi.yml
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
description: FinOps framework definition for the Salesforce API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce
  PublisherName: Salesforce
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce
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
name: Salesforce Finops
provider_name: Salesforce
provider_slug: salesforce
publisher_name: Salesforce
service_category: API
slug: salesforce-finops
source_filename: salesforce-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce\nproviderId: salesforce\npublisherName: Salesforce\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI\n  - Analytics\n  - Cloud\n  - Commerce\n  - CRM\n  - Customer Service\n  - Enterprise\n  - Marketing\n  - Platform\n  - Sales\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce\n  PublisherName: Salesforce\n  InvoiceIssuerName: Salesforce\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Salesforce REST API\n    baseURL: https://{instance}.salesforce.com/services/data\n    tags:\n      - CRM\n      - Objects\n      - Records\n      - REST\n      - SOQL\n      - SOSL\n    serviceName: Salesforce REST API\n    serviceCategory: API\n  - name: Salesforce SOAP API\n    baseURL: https://{instance}.salesforce.com/services/Soap\n    tags:\n      - CRM\n      - Enterprise\n      - Objects\n      - Records\n      - SOAP\n    serviceName: Salesforce SOAP API\n    serviceCategory: API\n  - name: Salesforce Bulk API\n    baseURL: https://{instance}.salesforce.com/services/async\n    tags:\n      - Bulk\n      - CRM\n      - Data Loading\n\
  \      - ETL\n      - Records\n    serviceName: Salesforce Bulk API\n    serviceCategory: API\n  - name: Salesforce Bulk API 2.0\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/jobs\n    tags:\n      - Bulk\n      - CRM\n      - Data Loading\n      - ETL\n      - Records\n    serviceName: Salesforce Bulk API 2.0\n    serviceCategory: API\n  - name: Salesforce Streaming API\n    baseURL: https://{instance}.salesforce.com/cometd\n    tags:\n      - CRM\n      - Events\n      - Push Notifications\n      - Real-Time\n      - Streaming\n    serviceName: Salesforce Streaming API\n    serviceCategory: API\n  - name: Salesforce Metadata API\n    baseURL: https://{instance}.salesforce.com/services/Soap/m\n    tags:\n      - Configuration\n      - CRM\n      - Deployment\n      - DevOps\n      - Metadata\n    serviceName: Salesforce Metadata API\n    serviceCategory: API\n  - name: Salesforce Tooling API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/tooling\n\
  \    tags:\n      - Apex\n      - CRM\n      - Development\n      - IDE\n      - Tooling\n    serviceName: Salesforce Tooling API\n    serviceCategory: API\n  - name: Salesforce Connect API (Chatter)\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/chatter\n    tags:\n      - Chatter\n      - Collaboration\n      - Connect\n      - CRM\n      - Feed\n      - Social\n    serviceName: Salesforce Connect API (Chatter)\n    serviceCategory: API\n  - name: Salesforce Analytics REST API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/wave\n    tags:\n      - Analytics\n      - CRM\n      - CRM Analytics\n      - Dashboards\n      - Reports\n      - Tableau CRM\n    serviceName: Salesforce Analytics REST API\n    serviceCategory: API\n  - name: Salesforce Reports and Dashboards REST API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/analytics\n    tags:\n      - Analytics\n      - CRM\n      - Dashboards\n      - Reports\n\
  \    serviceName: Salesforce Reports and Dashboards REST API\n    serviceCategory: API\n  - name: Salesforce Einstein Platform Services API\n    baseURL: https://api.einstein.ai/v2\n    tags:\n      - AI\n      - Computer Vision\n      - Einstein\n      - Machine Learning\n      - Natural Language Processing\n      - Prediction\n    serviceName: Salesforce Einstein Platform Services API\n    serviceCategory: API\n  - name: Salesforce Einstein Prediction Service API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/einstein\n    tags:\n      - AI\n      - CRM\n      - Einstein\n      - Machine Learning\n      - Prediction\n    serviceName: Salesforce Einstein Prediction Service API\n    serviceCategory: API\n  - name: Salesforce GraphQL API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/graphql\n    tags:\n      - CRM\n      - GraphQL\n      - Queries\n      - Records\n    serviceName: Salesforce GraphQL API\n    serviceCategory: API\n  -\
  \ name: Salesforce Pub/Sub API\n    baseURL: https://api.pubsub.salesforce.com\n    tags:\n      - CRM\n      - Events\n      - gRPC\n      - Platform Events\n      - Pub/Sub\n      - Real-Time\n    serviceName: Salesforce Pub/Sub API\n    serviceCategory: API\n  - name: Salesforce Platform Events API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/sobjects\n    tags:\n      - CRM\n      - Event-Driven\n      - Events\n      - Integration\n      - Platform Events\n    serviceName: Salesforce Platform Events API\n    serviceCategory: API\n  - name: Salesforce Change Data Capture API\n    baseURL: https://{instance}.salesforce.com/cometd\n    tags:\n      - CDC\n      - Change Data Capture\n      - CRM\n      - Events\n      - Integration\n    serviceName: Salesforce Change Data Capture API\n    serviceCategory: API\n  - name: Salesforce UI API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/ui-api\n    tags:\n      - Components\n      -\
  \ CRM\n      - Lightning\n      - UI\n      - User Interface\n    serviceName: Salesforce UI API\n    serviceCategory: API\n  - name: Salesforce Composite API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/composite\n    tags:\n      - Batch\n      - Composite\n      - CRM\n      - Performance\n      - REST\n    serviceName: Salesforce Composite API\n    serviceCategory: API\n  - name: Salesforce Apex REST API\n    baseURL: https://{instance}.salesforce.com/services/apexrest\n    tags:\n      - Apex\n      - CRM\n      - Custom APIs\n      - Development\n      - REST\n    serviceName: Salesforce Apex REST API\n    serviceCategory: API\n  - name: Salesforce Data Cloud API\n    baseURL: https://{instance}.salesforce.com/api/v1\n    tags:\n      - CDP\n      - CRM\n      - Customer Data Platform\n      - Data Cloud\n      - Identity Resolution\n    serviceName: Salesforce Data Cloud API\n    serviceCategory: API\n  - name: Salesforce Marketing Cloud REST API\n  \
  \  baseURL: https://{subdomain}.rest.marketingcloudapis.com\n    tags:\n      - Email\n      - Journeys\n      - Marketing Automation\n      - Marketing Cloud\n      - REST\n    serviceName: Salesforce Marketing Cloud REST API\n    serviceCategory: API\n  - name: Salesforce Marketing Cloud SOAP API\n    baseURL: https://{subdomain}.soap.marketingcloudapis.com\n    tags:\n      - Email\n      - Marketing Automation\n      - Marketing Cloud\n      - SOAP\n    serviceName: Salesforce Marketing Cloud SOAP API\n    serviceCategory: API\n  - name: Salesforce Pardot API (Account Engagement)\n    baseURL: https://pi.pardot.com/api\n    tags:\n      - Account Engagement\n      - B2B Marketing\n      - Lead Generation\n      - Marketing\n      - Pardot\n    serviceName: Salesforce Pardot API (Account Engagement)\n    serviceCategory: API\n  - name: Salesforce Commerce Cloud OCAPI\n    baseURL: https://{instance}.dx.commercecloud.salesforce.com\n    tags:\n      - B2C Commerce\n      - Commerce\n\
  \      - OCAPI\n      - Orders\n      - Storefront\n    serviceName: Salesforce Commerce Cloud OCAPI\n    serviceCategory: API\n  - name: Salesforce Commerce Cloud Shopper APIs (SCAPI)\n    baseURL: https://{shortCode}.api.commercecloud.salesforce.com\n    tags:\n      - B2C Commerce\n      - Commerce\n      - Orders\n      - Products\n      - Shopper\n      - Storefront\n    serviceName: Salesforce Commerce Cloud Shopper APIs (SCAPI)\n    serviceCategory: API\n  - name: Salesforce Field Service API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}\n    tags:\n      - Field Service\n      - Mobile\n      - Scheduling\n      - Service Cloud\n      - Work Orders\n    serviceName: Salesforce Field Service API\n    serviceCategory: API\n  - name: Salesforce Health Cloud API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}\n    tags:\n      - Clinical\n      - FHIR\n      - Health Cloud\n      - Healthcare\n      - Patients\n    serviceName: Salesforce\
  \ Health Cloud API\n    serviceCategory: API\n  - name: Salesforce Financial Services Cloud API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}\n    tags:\n      - Banking\n      - CRM\n      - Financial Services\n      - Insurance\n      - Wealth Management\n    serviceName: Salesforce Financial Services Cloud API\n    serviceCategory: API\n  - name: Salesforce Experience Cloud API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/connect/communities\n    tags:\n      - Communities\n      - Experience Cloud\n      - Portals\n      - Sites\n    serviceName: Salesforce Experience Cloud API\n    serviceCategory: API\n  - name: Salesforce MuleSoft Anypoint Platform API\n    baseURL: https://anypoint.mulesoft.com/accounts/api\n    tags:\n      - API Management\n      - Integration\n      - iPaaS\n      - MuleSoft\n    serviceName: Salesforce MuleSoft Anypoint Platform API\n    serviceCategory: API\n  - name: Salesforce Tableau REST API\n    baseURL:\
  \ https://{server}/api/{version}\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Dashboards\n      - Data Visualization\n      - Tableau\n    serviceName: Salesforce Tableau REST API\n    serviceCategory: API\n  - name: Salesforce Lightning Web Components (LWC)\n    baseURL: https://developer.salesforce.com/docs/platform/lwc\n    tags:\n      - Components\n      - JavaScript\n      - Lightning\n      - LWC\n      - UI Framework\n    serviceName: Salesforce Lightning Web Components (LWC)\n    serviceCategory: API\n  - name: Salesforce Aura Components\n    baseURL: https://developer.salesforce.com/docs/atlas.en-us.lightning.meta/lightning\n    tags:\n      - Aura\n      - Components\n      - JavaScript\n      - Legacy\n      - Lightning\n    serviceName: Salesforce Aura Components\n    serviceCategory: API\n  - name: Salesforce Lightning Design System (SLDS)\n    baseURL: https://www.lightningdesignsystem.com\n    tags:\n      - Components\n      - CSS\n      - Design\
  \ System\n      - Lightning\n      - UI\n    serviceName: Salesforce Lightning Design System (SLDS)\n    serviceCategory: API\n  - name: Salesforce Agentforce Agent API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/agent\n    tags:\n      - Agentforce\n      - Agents\n      - AI\n      - Conversational AI\n      - GenAI\n      - REST\n    serviceName: Salesforce Agentforce Agent API\n    serviceCategory: API\n  - name: Salesforce Models API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/einstein\n    tags:\n      - Agentforce\n      - AI\n      - Einstein\n      - GenAI\n      - LLM\n      - Machine Learning\n    serviceName: Salesforce Models API\n    serviceCategory: API\n  - name: Salesforce Interaction Service API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}\n    tags:\n      - BYOC\n      - Customer Service\n      - Messaging\n      - Omnichannel\n      - Service Cloud\n    serviceName: Salesforce Interaction\
  \ Service API\n    serviceCategory: API\n  - name: Salesforce B2B Commerce API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/commerce\n    tags:\n      - B2B Commerce\n      - Cart\n      - Commerce\n      - Orders\n      - Products\n      - Storefront\n    serviceName: Salesforce B2B Commerce API\n    serviceCategory: API\n  - name: Salesforce Actions API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/actions\n    tags:\n      - Actions\n      - Automation\n      - CRM\n      - Flow\n      - Invocable\n    serviceName: Salesforce Actions API\n    serviceCategory: API\n  - name: Salesforce IoT REST API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}/iot\n    tags:\n      - Events\n      - IoT\n      - Orchestrations\n      - REST\n    serviceName: Salesforce IoT REST API\n    serviceCategory: API\n  - name: Salesforce Service Cloud Voice API\n    baseURL: https://{instance}.salesforce.com/services/data/v{version}\n\
  \    tags:\n      - Contact Center\n      - CTI\n      - Service Cloud\n      - Telephony\n      - Voice\n    serviceName: Salesforce Service Cloud Voice API\n    serviceCategory: API\n  - name: Salesforce Mobile SDK\n    baseURL: https://developer.salesforce.com/docs/platform/mobile-sdk\n    tags:\n      - Android\n      - iOS\n      - Mobile\n      - React Native\n      - SDK\n    serviceName: Salesforce Mobile SDK\n    serviceCategory: API\n  - name: Salesforce\n    baseURL: ''\n    tags:\n      - CRM\n    serviceName: Salesforce\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce/refs/heads/main/finops/salesforce-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI
- Analytics
- Cloud
- Commerce
- CRM
- Customer Service
- Enterprise
- Marketing
- Platform
- Sales
- FinOps
- Cost Management
- FOCUS
---
