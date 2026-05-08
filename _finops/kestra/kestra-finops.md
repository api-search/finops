---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: open-source
  format: yaml
  label: Kestra Flows API
  slug: flows-api
  spec_type: OpenAPI
  url: https://kestra.io/docs/api-reference/open-source
- filename: open-source
  format: yaml
  label: Kestra Executions API
  slug: executions-api
  spec_type: OpenAPI
  url: https://kestra.io/docs/api-reference/open-source
- filename: open-source
  format: yaml
  label: Kestra Namespaces API
  slug: namespaces-api
  spec_type: OpenAPI
  url: https://kestra.io/docs/api-reference/open-source
- filename: open-source
  format: yaml
  label: Kestra Key-Value Store API
  slug: kv-store-api
  spec_type: OpenAPI
  url: https://kestra.io/docs/api-reference/open-source
- filename: open-source
  format: yaml
  label: Kestra Namespace Files API
  slug: namespace-files-api
  spec_type: OpenAPI
  url: https://kestra.io/docs/api-reference/open-source
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
description: FinOps framework definition for the Kestra API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Kestra
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Kestra
  PublisherName: Kestra
  ServiceCategory: Developer Tools / API
  ServiceName: Kestra
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
name: Kestra Finops
provider_name: Kestra
provider_slug: kestra
publisher_name: Kestra
service_category: API
slug: kestra-finops
source_filename: kestra-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Kestra\nproviderId: kestra\npublisherName: Kestra\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Automation\n  - Data Pipelines\n  - Event-Driven\n  - Orchestration\n  - Workflows\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Kestra API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the\
  \ consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Kestra\n  ServiceCategory: Developer Tools / API\n  ProviderName: Kestra\n  PublisherName: Kestra\n  InvoiceIssuerName: Kestra\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n\
  \      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Kestra Flows API\n    baseURL: ''\n    tags:\n      - Flows\n      - Orchestration\n      - Workflows\n    serviceName: Kestra Flows API\n    serviceCategory: API\n  - name: Kestra Executions API\n    baseURL: ''\n    tags:\n      - Executions\n      - Orchestration\n      - Workflows\n    serviceName: Kestra Executions API\n    serviceCategory: API\n  - name: Kestra Namespaces API\n    baseURL: ''\n    tags:\n      - Namespaces\n      - Orchestration\n      - Organization\n    serviceName: Kestra Namespaces API\n    serviceCategory: API\n  - name: Kestra Key-Value Store API\n    baseURL: ''\n    tags:\n      - Key-Value Store\n      - State Management\n      - Storage\n    serviceName: Kestra Key-Value Store API\n \
  \   serviceCategory: API\n  - name: Kestra Namespace Files API\n    baseURL: ''\n    tags:\n      - Files\n      - Namespaces\n      - Storage\n    serviceName: Kestra Namespace Files API\n    serviceCategory: API\n  - name: Kestra Enterprise API\n    baseURL: ''\n    tags:\n      - Authentication\n      - Enterprise\n      - Governance\n      - RBAC\n    serviceName: Kestra Enterprise API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/kestra/refs/heads/main/finops/kestra-finops.yml
sources: []
specification: FinOps Framework
tags:
- Automation
- Data Pipelines
- Event-Driven
- Orchestration
- Workflows
- FinOps
- Cost Management
- FOCUS
---
