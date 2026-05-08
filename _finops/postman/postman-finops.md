---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: postman-webhooks-asyncapi.yml
  format: yaml
  label: Postman
  slug: postman
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/asyncapi/postman-webhooks-asyncapi.yml
- filename: postman-collections-api-openapi.yml
  format: yaml
  label: Postman Collections API
  slug: collections-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-collections-api-openapi.yml
- filename: postman-workspaces-api-openapi.yml
  format: yaml
  label: Postman Workspaces API
  slug: workspaces-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-workspaces-api-openapi.yml
- filename: postman-environments-api-openapi.yml
  format: yaml
  label: Postman Environments API
  slug: environments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-environments-api-openapi.yml
- filename: postman-mock-servers-api-openapi.yml
  format: yaml
  label: Postman Mock Servers API
  slug: mock-servers-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-mock-servers-api-openapi.yml
- filename: postman-monitors-api-openapi.yml
  format: yaml
  label: Postman Monitors API
  slug: monitors-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-monitors-api-openapi.yml
- filename: postman-apis-api-openapi.yml
  format: yaml
  label: Postman APIs API
  slug: apis-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-apis-api-openapi.yml
- filename: postman-private-api-network-api-openapi.yml
  format: yaml
  label: Postman Private API Network API
  slug: private-api-network-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-private-api-network-api-openapi.yml
- filename: postman-webhooks-api-openapi.yml
  format: yaml
  label: Postman Webhooks API
  slug: webhooks-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-webhooks-api-openapi.yml
- filename: postman-collection-runs-api-openapi.yml
  format: yaml
  label: Postman Collection Runs API
  slug: collection-runs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-collection-runs-api-openapi.yml
- filename: postman-tags-api-openapi.yml
  format: yaml
  label: Postman Tags API
  slug: tags-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-tags-api-openapi.yml
- filename: postman-audit-logs-api-openapi.yml
  format: yaml
  label: Postman Audit Logs API
  slug: audit-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-audit-logs-api-openapi.yml
- filename: postman-secret-scanner-api-openapi.yml
  format: yaml
  label: Postman Secret Scanner API
  slug: secret-scanner-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/openapi/postman-secret-scanner-api-openapi.yml
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
description: FinOps framework definition for the Postman API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Postman
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Postman
  PublisherName: Postman
  ServiceCategory: Developer Tools / API
  ServiceName: Postman
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
name: Postman Finops
provider_name: Postman
provider_slug: postman
publisher_name: Postman
service_category: API
slug: postman-finops
source_filename: postman-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Postman\nproviderId: postman\npublisherName: Postman\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - AI Agent Builder\n  - API Development\n  - API Documentation\n  - API Governance\n  - API Monitoring\n  - API Testing\n  - Automation\n  - Client\n  - Clients\n  - Collaboration\n  - Collections\n  - Discovery\n  - Environments\n  - MCP\n  - Mock Servers\n  - Mocking\n  - Network\n  - Platform\n  - Testing\n  - Workflows\n  - Workspaces\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Postman API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across\
  \ the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize\
  \ Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Postman\n  ServiceCategory: Developer Tools / API\n  ProviderName: Postman\n  PublisherName: Postman\n  InvoiceIssuerName: Postman\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Postman\n    baseURL: ''\n    tags:\n      - Automation\n      - Client\n      - Collections\n      - Discovery\n      - Mocking\n      - Network\n      - Platform\n      - Testing\n      - Workflows\n    serviceName: Postman\n    serviceCategory: API\n  - name: Postman Collections API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Management\n      - Automation\n      - Collections\n    serviceName: Postman Collections API\n    serviceCategory:\
  \ API\n  - name: Postman Workspaces API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Management\n      - Collaboration\n      - Workspaces\n    serviceName: Postman Workspaces API\n    serviceCategory: API\n  - name: Postman Environments API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Configuration\n      - Environments\n      - Variables\n    serviceName: Postman Environments API\n    serviceCategory: API\n  - name: Postman Mock Servers API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Development\n      - Mocking\n      - Simulation\n    serviceName: Postman Mock Servers API\n    serviceCategory: API\n  - name: Postman Monitors API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Automation\n      - Monitoring\n      - Scheduling\n      - Testing\n    serviceName: Postman Monitors API\n    serviceCategory: API\n  - name: Postman APIs API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Builder\n     \
  \ - API Design\n      - Specifications\n    serviceName: Postman APIs API\n    serviceCategory: API\n  - name: Postman Private API Network API\n    baseURL: https://api.getpostman.com\n    tags:\n      - API Network\n      - Discovery\n      - Governance\n    serviceName: Postman Private API Network API\n    serviceCategory: API\n  - name: Postman Webhooks API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Automation\n      - Events\n      - Integrations\n      - Webhooks\n    serviceName: Postman Webhooks API\n    serviceCategory: API\n  - name: Postman Collection Runs API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Automation\n      - CI/CD\n      - Collection Runner\n      - Testing\n    serviceName: Postman Collection Runs API\n    serviceCategory: API\n  - name: Postman Tags API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Governance\n      - Metadata\n      - Organization\n    serviceName: Postman Tags API\n    serviceCategory: API\n\
  \  - name: Postman Audit Logs API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Audit Logs\n      - Compliance\n      - Governance\n      - Security\n    serviceName: Postman Audit Logs API\n    serviceCategory: API\n  - name: Postman Secret Scanner API\n    baseURL: https://api.getpostman.com\n    tags:\n      - Compliance\n      - Governance\n      - Secret Scanning\n      - Security\n    serviceName: Postman Secret Scanner API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - name: Postman\n    email: help@postman.com\n    url: https://www.postman.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/postman/refs/heads/main/finops/postman-finops.yml
sources: []
specification: FinOps Framework
tags:
- AI Agent Builder
- API Development
- API Documentation
- API Governance
- API Monitoring
- API Testing
- Automation
- Client
- Clients
- Collaboration
- Collections
- Discovery
- Environments
- MCP
- Mock Servers
- Mocking
- Network
- Platform
- Testing
- Workflows
- Workspaces
- FinOps
- Cost Management
- FOCUS
---
