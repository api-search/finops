---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: api.github.com.json
  format: json
  label: GitHub Copilot API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot for Business API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot User Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot Metrics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot Usage Metrics API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
- filename: api.github.com.json
  format: json
  label: GitHub Copilot Content Exclusion API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/github/rest-api-description/main/descriptions/api.github.com/api.github.com.json
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
description: FinOps framework definition for the GitHub Copilot API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: GitHub Copilot
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: GitHub Copilot
  PublisherName: GitHub Copilot
  ServiceCategory: Developer Tools / API
  ServiceName: GitHub Copilot
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
name: Github Copilot Finops
provider_name: GitHub Copilot
provider_slug: github-copilot
publisher_name: GitHub Copilot
service_category: API
slug: github-copilot-finops
source_filename: github-copilot-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: GitHub Copilot\nproviderId: github-copilot\npublisherName: GitHub Copilot\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agents\n  - AI\n  - Artificial Intelligence\n  - Code Generation\n  - Code Review\n  - Coding Agent\n  - Custom Instructions\n  - Developer Tools\n  - Extensions\n  - IDE\n  - Machine Learning\n  - MCP\n  - Metrics\n  - Model Context Protocol\n  - Productivity\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the GitHub Copilot API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n\
  \    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting\
  \ for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: GitHub Copilot\n  ServiceCategory: Developer Tools / API\n  ProviderName: GitHub Copilot\n  PublisherName: GitHub Copilot\n  InvoiceIssuerName: GitHub Copilot\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: GitHub Copilot API\n    baseURL: https://api.github.com\n    tags:\n      - AI\n      - Code Completion\n      - Developer Tools\n      - Machine Learning\n    serviceName: GitHub Copilot API\n    serviceCategory: API\n  - name: GitHub Copilot for Business API\n    baseURL: https://api.github.com\n    tags:\n      - Enterprise\n      - Seat Management\n      - Usage Analytics\n    serviceName: GitHub Copilot for Business API\n    serviceCategory: API\n  - name: GitHub Copilot Chat API\n\
  \    baseURL: https://api.github.com\n    tags:\n      - Chat\n      - Conversational AI\n      - IDE Integration\n    serviceName: GitHub Copilot Chat API\n    serviceCategory: API\n  - name: GitHub Copilot User Management API\n    baseURL: https://api.github.com\n    tags:\n      - Billing\n      - Organizations\n      - Seat Management\n      - User Management\n    serviceName: GitHub Copilot User Management API\n    serviceCategory: API\n  - name: GitHub Copilot Metrics API\n    baseURL: https://api.github.com\n    tags:\n      - Analytics\n      - Metrics\n      - Organizations\n      - Usage\n    serviceName: GitHub Copilot Metrics API\n    serviceCategory: API\n  - name: GitHub Copilot Usage Metrics API\n    baseURL: https://api.github.com\n    tags:\n      - Analytics\n      - Enterprise\n      - Reporting\n      - Usage Metrics\n    serviceName: GitHub Copilot Usage Metrics API\n    serviceCategory: API\n  - name: GitHub Copilot Content Exclusion API\n    baseURL: https://api.github.com\n\
  \    tags:\n      - Content Exclusion\n      - Governance\n      - Policy\n      - Security\n    serviceName: GitHub Copilot Content Exclusion API\n    serviceCategory: API\n  - name: GitHub Copilot Extensions API\n    baseURL: https://api.github.com\n    tags:\n      - Agents\n      - Extensions\n      - Integrations\n      - Skillsets\n    serviceName: GitHub Copilot Extensions API\n    serviceCategory: API\n  - name: GitHub Copilot Coding Agent\n    baseURL: https://api.github.com\n    tags:\n      - Agents\n      - Automation\n      - Code Generation\n      - GitHub Actions\n      - Pull Requests\n    serviceName: GitHub Copilot Coding Agent\n    serviceCategory: API\n  - name: GitHub Copilot Code Review\n    baseURL: https://api.github.com\n    tags:\n      - Agents\n      - Code Quality\n      - Code Review\n      - Pull Requests\n    serviceName: GitHub Copilot Code Review\n    serviceCategory: API\n  - name: GitHub MCP Server\n    baseURL: https://api.github.com\n    tags:\n  \
  \    - Agents\n      - Context\n      - Integrations\n      - MCP\n      - Model Context Protocol\n    serviceName: GitHub MCP Server\n    serviceCategory: API\n  - name: GitHub Copilot Custom Instructions\n    baseURL: https://api.github.com\n    tags:\n      - Configuration\n      - Customization\n      - Instructions\n      - Organizations\n    serviceName: GitHub Copilot Custom Instructions\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: http://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/github-copilot/refs/heads/main/finops/github-copilot-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agents
- AI
- Artificial Intelligence
- Code Generation
- Code Review
- Coding Agent
- Custom Instructions
- Developer Tools
- Extensions
- IDE
- Machine Learning
- MCP
- Metrics
- Model Context Protocol
- Productivity
- FinOps
- Cost Management
- FOCUS
---
