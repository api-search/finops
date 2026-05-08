---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: index.html
  format: yaml
  label: Dataiku Public API
  slug: dataiku-public-api
  spec_type: OpenAPI
  url: https://doc.dataiku.com/dss/latest/publicapi/rest/index.html
- filename: dataiku-api-node-admin-openapi.yml
  format: yaml
  label: Dataiku API Node Administration API
  slug: dataiku-api-node-administration-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dataiku/refs/heads/main/openapi/dataiku-api-node-admin-openapi.yml
- filename: dataiku-govern-api-openapi.yml
  format: yaml
  label: Dataiku Govern API
  slug: dataiku-govern-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/dataiku/refs/heads/main/openapi/dataiku-govern-api-openapi.yml
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
description: FinOps framework definition for the Dataiku API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Dataiku
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Dataiku
  PublisherName: Dataiku
  ServiceCategory: Developer Tools / API
  ServiceName: Dataiku
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
name: Dataiku Finops
provider_name: Dataiku
provider_slug: dataiku
publisher_name: Dataiku
service_category: API
slug: dataiku-finops
source_filename: dataiku-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Dataiku\nproviderId: dataiku\npublisherName: Dataiku\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Artificial Intelligence\n  - Data Platform\n  - Data Science\n  - Machine Learning\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Dataiku API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Dataiku\n  ServiceCategory: Developer Tools / API\n  ProviderName: Dataiku\n  PublisherName: Dataiku\n  InvoiceIssuerName: Dataiku\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Dataiku Public API\n    baseURL: https://dss.example.com/public/api\n    tags:\n      - Data Science\n      - Datasets\n      - Projects\n      - Workflows\n    serviceName: Dataiku Public API\n    serviceCategory: API\n  - name: Dataiku Python API\n    baseURL: https://pypi.org/project/dataiku-api-client/\n    tags:\n      - Client Library\n      - Python\n      - Sdk\n    serviceName: Dataiku Python API\n    serviceCategory: API\n  - name: Dataiku Internal API\n    baseURL: ''\n    tags:\n      - Internal\n      - Plugins\n      - Recipes\n    serviceName: Dataiku Internal API\n    serviceCategory: API\n  - name: Dataiku R API\n    baseURL: ''\n    tags:\n      - Client Library\n      - R Language\n\
  \      - Sdk\n    serviceName: Dataiku R API\n    serviceCategory: API\n  - name: Dataiku JavaScript API\n    baseURL: ''\n    tags:\n      - Javascript\n      - Visualization\n      - Webapps\n    serviceName: Dataiku JavaScript API\n    serviceCategory: API\n  - name: Dataiku Scala API\n    baseURL: ''\n    tags:\n      - Big Data\n      - Scala\n      - Spark\n    serviceName: Dataiku Scala API\n    serviceCategory: API\n  - name: Dataiku API Node Administration API\n    baseURL: ''\n    tags:\n      - Api Node\n      - Deployment\n      - Model Serving\n      - Real-Time\n    serviceName: Dataiku API Node Administration API\n    serviceCategory: API\n  - name: Dataiku Govern API\n    baseURL: ''\n    tags:\n      - Ai Governance\n      - Blueprints\n      - Compliance\n      - Governance\n    serviceName: Dataiku Govern API\n    serviceCategory: API\n  - name: Dataiku Plugin API\n    baseURL: ''\n    tags:\n      - Custom Components\n      - Extensions\n      - Plugins\n    serviceName:\
  \ Dataiku Plugin API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.dataiku.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/dataiku/refs/heads/main/finops/dataiku-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Artificial Intelligence
- Data Platform
- Data Science
- Machine Learning
- FinOps
- Cost Management
- FOCUS
---
