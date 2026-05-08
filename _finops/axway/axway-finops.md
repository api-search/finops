---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: axway-amplify-platform-openapi-original.json
  format: json
  label: Axway Amplify Platform API
  slug: axway-amplify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/axway/refs/heads/main/openapi/axway-amplify-platform-openapi-original.json
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
description: FinOps framework definition for the Axway API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Axway
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Axway
  PublisherName: Axway
  ServiceCategory: Developer Tools / API
  ServiceName: Axway
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
name: Axway Finops
provider_name: Axway
provider_slug: axway
publisher_name: Axway
service_category: API
slug: axway-finops
source_filename: axway-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Axway\nproviderId: axway\npublisherName: Axway\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - API Management\n  - Enterprise\n  - Integration\n  - Security\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Axway API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Axway\n  ServiceCategory: Developer Tools / API\n  ProviderName: Axway\n  PublisherName: Axway\n  InvoiceIssuerName: Axway\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Axway Amplify Platform API\n    baseURL: https://platform.axway.com/api/v1\n    tags:\n      - Amplify\n      - API Management\n      - Enterprise\n    serviceName: Axway Amplify Platform API\n    serviceCategory: API\n  - name: Axway Amplify Central API\n    baseURL: https://apicentral.axway.com\n    tags:\n      - Amplify\n      - API Catalog\n      - API Management\n      - Governance\n    serviceName: Axway Amplify Central API\n    serviceCategory: API\n  - name: Axway API Gateway\n    baseURL: https://docs.axway.com\n    tags:\n      - API Gateway\n      - Enterprise\n      - On-Premises\n      - Security\n    serviceName: Axway API Gateway\n    serviceCategory: API\n  - name: Axway API Manager\n    baseURL: https://docs.axway.com\n    tags:\n\
  \      - Administration\n      - API Lifecycle\n      - API Management\n      - Enterprise\n    serviceName: Axway API Manager\n    serviceCategory: API\n  - name: Axway API Builder\n    baseURL: https://docs.axway.com\n    tags:\n      - API Builder\n      - Low-Code\n      - Microservices\n      - Node.js\n    serviceName: Axway API Builder\n    serviceCategory: API\n  - name: Axway Amplify Streams\n    baseURL: https://streams-open-docs.netlify.app\n    tags:\n      - Event-Driven\n      - Real-Time\n      - Streaming\n      - WebSocket\n    serviceName: Axway Amplify Streams\n    serviceCategory: API\n  - name: Axway Amplify Engage\n    baseURL: ''\n    tags:\n      - API Marketplace\n      - API Monetization\n      - Governance\n      - Observability\n    serviceName: Axway Amplify Engage\n    serviceCategory: API\n  - name: Axway Amplify AI Gateway\n    baseURL: ''\n    tags:\n      - AI\n      - AI Gateway\n      - Governance\n      - LLM\n      - MCP\n    serviceName: Axway Amplify\
  \ AI Gateway\n    serviceCategory: API\n  - name: Axway Amplify Fusion\n    baseURL: ''\n    tags:\n      - Automation\n      - Integration\n      - Low-Code\n      - Workflow\n    serviceName: Axway Amplify Fusion\n    serviceCategory: API\n  - name: Axway Flow Manager\n    baseURL: https://docs.axway.com\n    tags:\n      - B2B Integration\n      - Enterprise\n      - File Transfer\n      - MFT\n    serviceName: Axway Flow Manager\n    serviceCategory: API\n  - name: Axway SecureTransport\n    baseURL: ''\n    tags:\n      - Compliance\n      - Enterprise\n      - File Transfer\n      - MFT\n    serviceName: Axway SecureTransport\n    serviceCategory: API\n  - name: Axway Transfer CFT\n    baseURL: ''\n    tags:\n      - Decentralized\n      - Enterprise\n      - File Transfer\n      - MFT\n    serviceName: Axway Transfer CFT\n    serviceCategory: API\n  - name: Axway B2Bi\n    baseURL: ''\n    tags:\n      - B2B\n      - EDI\n      - Integration\n      - Trading Partners\n    serviceName:\
  \ Axway B2Bi\n    serviceCategory: API\n  - name: Axway Open Banking\n    baseURL: ''\n    tags:\n      - Banking\n      - Compliance\n      - Finance\n      - Open Banking\n      - PSD2\n    serviceName: Axway Open Banking\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/axway/refs/heads/main/finops/axway-finops.yml
sources: []
specification: FinOps Framework
tags:
- API Management
- Enterprise
- Integration
- Security
- FinOps
- Cost Management
- FOCUS
---
