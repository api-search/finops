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
  label: Helicone
  slug: helicone
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: ai-gateway.openapi.json
  format: json
  label: Helicone AI Gateway API
  slug: ai-gateway-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/ai-gateway.openapi.json
- filename: swagger.json
  format: json
  label: Helicone Request API
  slug: request-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Prompt API
  slug: prompt-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Experiment API
  slug: experiment-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Evals API
  slug: evals-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Session API
  slug: session-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone User API
  slug: user-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Webhook API
  slug: webhook-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Model Registry API
  slug: model-registry-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Trace API
  slug: trace-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Dashboard API
  slug: dashboard-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
- filename: swagger.json
  format: json
  label: Helicone Property API
  slug: property-api
  spec_type: OpenAPI
  url: https://docs.helicone.ai/swagger.json
billing_model:
  billingCurrency: USD
  billingFrequency: Monthly
  chargeCategories:
  - Purchase
  - Usage
  - Tax
  - Credit
  - Adjustment
  chargeFrequency: Recurring
  pricingCategory: Tiered Subscription + Usage-Based Overage
description: 'FOCUS-aligned FinOps definition for Helicone: a tiered subscription with per-tier included request and storage allotments, plus usage-based overage for logged requests and storage. Enterprise tier is custom-priced.'
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Helicone, Inc.
  PricingCategory: Tiered Subscription + Usage-Based
  PricingUnit: request
  ProviderName: Helicone
  PublisherName: Helicone, Inc.
  ServiceCategory: AI Observability
  ServiceName: Helicone
layout: finops
meters:
- aggregation: sum
  description: Flat monthly subscription fee for the active Helicone tier (Pro $79, Team $799, Enterprise custom)
  dimensions:
  - tier
  - organization
  name: subscription_fee
  unit: month
- aggregation: sum
  description: Count of LLM requests logged through the AI Gateway or Request API
  dimensions:
  - tier
  - organization
  - model
  - provider
  - consumer
  name: logged_requests
  unit: request
- aggregation: sum
  description: Logged requests above the 10,000-per-month included quota, billed via the published pricing calculator
  dimensions:
  - tier
  - organization
  name: request_overage
  unit: request
- aggregation: max
  description: Stored payloads and trace data
  dimensions:
  - tier
  - organization
  - retention_window
  name: storage_used
  unit: GB
- aggregation: max
  description: Storage above the 1 GB included allotment, billed via the pricing calculator
  dimensions:
  - tier
  - organization
  name: storage_overage
  unit: GB
- aggregation: max
  description: Active seats per organization (Pro and above are unlimited; Hobby is 1)
  dimensions:
  - tier
  - organization
  name: seats
  unit: seat
- aggregation: max
  description: Number of organizations under the account (Hobby/Pro 1, Team 5, Enterprise unlimited)
  dimensions:
  - tier
  name: organizations
  unit: organization
name: Helicone Finops
provider_name: Helicone
provider_slug: helicone
publisher_name: Helicone, Inc.
service_category: AI Observability
slug: helicone-finops
source_filename: helicone-finops.yml
source_heading: FinOps Profile
source_url: https://helicone.ai/pricing
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Helicone\nproviderId: helicone\npublisherName: Helicone, Inc.\nserviceCategory: AI Observability\ncreated: '2026-05-04'\nmodified: '2026-05-05'\nreconciled: true\ntags:\n  - AI Gateways\n  - AI Monitoring\n  - Gateways\n  - LLM Observability\n  - LLM Routing\n  - Prompt Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: 'FOCUS-aligned FinOps definition for Helicone: a tiered subscription with per-tier included\n  request and storage allotments, plus usage-based overage for logged requests and storage. Enterprise tier\n  is custom-priced.'\nsources:\n  - https://helicone.ai/pricing\n  - https://docs.helicone.ai/getting-started/integration-method/gateway\nbillingModel:\n \
  \ pricingCategory: Tiered Subscription + Usage-Based Overage\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Purchase\n    - Usage\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Helicone\n  ServiceCategory: AI Observability\n  ProviderName: Helicone\n  PublisherName: Helicone, Inc.\n  InvoiceIssuerName: Helicone, Inc.\n  PricingCategory: Tiered Subscription + Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nprinciples:\n  - name: Visibility\n    description: Use the Helicone dashboard, request and session APIs, and HQL queries (Pro and above) to\n      surface per-application LLM cost, latency, and token consumption in near real-time.\n  - name: Allocation\n    description: Tag each gateway call with custom properties (Helicone Property API) - e.g. team, environment,\n      feature, customer-id - so cost can be attributed via the Property and User APIs.\n  - name:\
  \ Optimization\n    description: Helicone-specific levers include caching, prompt versioning, model routing through the AI\n      Gateway, retry/timeout tuning, and using the Evals API to compare cheaper models for the same quality.\n  - name: Accountability\n    description: Set per-organization budgets, configure alerts and reports (Pro and above), and use the\n      dedicated Slack channel on Team and above to escalate spend anomalies.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n \
  \   capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nmeters:\n  - name: subscription_fee\n    description: Flat monthly subscription fee for the active Helicone tier (Pro $79, Team $799, Enterprise\n      custom)\n    unit: month\n    aggregation: sum\n    dimensions:\n      - tier\n      - organization\n  - name: logged_requests\n    description: Count of LLM requests logged through the AI Gateway or Request API\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n      - organization\n      - model\n      - provider\n      - consumer\n  - name: request_overage\n    description: Logged requests above the 10,000-per-month included quota, billed via the published\n      pricing calculator\n    unit: request\n    aggregation: sum\n    dimensions:\n      - tier\n      - organization\n  - name: storage_used\n    description: Stored\
  \ payloads and trace data\n    unit: GB\n    aggregation: max\n    dimensions:\n      - tier\n      - organization\n      - retention_window\n  - name: storage_overage\n    description: Storage above the 1 GB included allotment, billed via the pricing calculator\n    unit: GB\n    aggregation: max\n    dimensions:\n      - tier\n      - organization\n  - name: seats\n    description: Active seats per organization (Pro and above are unlimited; Hobby is 1)\n    unit: seat\n    aggregation: max\n    dimensions:\n      - tier\n      - organization\n  - name: organizations\n    description: Number of organizations under the account (Hobby/Pro 1, Team 5, Enterprise unlimited)\n    unit: organization\n    aggregation: max\n    dimensions:\n      - tier\napis:\n  - name: Helicone\n    baseURL: ''\n    tags:\n      - AI Gateways\n      - Gateways\n      - LLM Routing\n    serviceName: Helicone\n    serviceCategory: AI Observability\n  - name: Helicone AI Gateway API\n    baseURL: https://ai-gateway.helicone.ai\n\
  \    tags:\n      - AI Gateways\n      - AI Models\n      - Chat Completions\n      - LLM Routing\n    serviceName: Helicone AI Gateway API\n    serviceCategory: AI Observability\n  - name: Helicone Request API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Analytics\n      - LLM Observability\n      - Requests\n    serviceName: Helicone Request API\n    serviceCategory: AI Observability\n  - name: Helicone Prompt API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Prompt Management\n      - Prompts\n      - Versioning\n    serviceName: Helicone Prompt API\n    serviceCategory: AI Observability\n  - name: Helicone Experiment API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Datasets\n      - Evaluations\n      - Experiments\n    serviceName: Helicone Experiment API\n    serviceCategory: AI Observability\n  - name: Helicone Evals API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Evaluations\n      - LLM Quality\n      - Scoring\n    serviceName:\
  \ Helicone Evals API\n    serviceCategory: AI Observability\n  - name: Helicone Session API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Debugging\n      - Sessions\n      - Tracing\n    serviceName: Helicone Session API\n    serviceCategory: AI Observability\n  - name: Helicone User API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Analytics\n      - Metrics\n      - Users\n    serviceName: Helicone User API\n    serviceCategory: AI Observability\n  - name: Helicone Webhook API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Events\n      - Notifications\n      - Webhooks\n    serviceName: Helicone Webhook API\n    serviceCategory: AI Observability\n  - name: Helicone Model Registry API\n    baseURL: https://api.helicone.ai\n    tags:\n      - AI Models\n      - Models\n      - Registry\n    serviceName: Helicone Model Registry API\n    serviceCategory: AI Observability\n  - name: Helicone Trace API\n    baseURL: https://api.helicone.ai\n    tags:\n\
  \      - Logging\n      - Observability\n      - Tracing\n    serviceName: Helicone Trace API\n    serviceCategory: AI Observability\n  - name: Helicone Dashboard API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Analytics\n      - Dashboard\n      - Scoring\n    serviceName: Helicone Dashboard API\n    serviceCategory: AI Observability\n  - name: Helicone Property API\n    baseURL: https://api.helicone.ai\n    tags:\n      - Custom Properties\n      - Metadata\n      - Properties\n    serviceName: Helicone Property API\n    serviceCategory: AI Observability\nunitEconomics:\n  - name: Cost per 1K Logged Requests\n    metric: billed_cost / (logged_requests / 1000)\n    target: TBD\n  - name: Cost per Active Organization\n    metric: billed_cost / organizations\n    target: TBD\n  - name: Subscription Effective Cost per Logged Request\n    metric: subscription_fee / logged_requests\n    target: trends down as throughput increases\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/helicone/refs/heads/main/finops/helicone-finops.yml
sources:
- https://helicone.ai/pricing
- https://docs.helicone.ai/getting-started/integration-method/gateway
specification: FinOps Framework
tags:
- AI Gateways
- AI Monitoring
- Gateways
- LLM Observability
- LLM Routing
- Prompt Management
- FinOps
- Cost Management
- FOCUS
---
