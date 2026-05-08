---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: datahub-openapi-openapi.yml
  format: yaml
  label: DataHub OpenAPI
  slug: datahub-openapi
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/datahub/refs/heads/main/openapi/datahub-openapi-openapi.yml
- filename: datahub-actions-asyncapi.yml
  format: yaml
  label: DataHub Actions Framework
  slug: datahub-actions-framework
  spec_type: AsyncAPI
  url: https://raw.githubusercontent.com/api-evangelist/datahub/refs/heads/main/asyncapi/datahub-actions-asyncapi.yml
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
description: FinOps framework definition for the DataHub API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: DataHub
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: DataHub
  PublisherName: DataHub
  ServiceCategory: Developer Tools / API
  ServiceName: DataHub
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
name: Datahub Finops
provider_name: DataHub
provider_slug: datahub
publisher_name: DataHub
service_category: API
slug: datahub-finops
source_filename: datahub-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: DataHub\nproviderId: datahub\npublisherName: DataHub\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Data Catalog\n  - Data Discovery\n  - Data Governance\n  - Data Lineage\n  - Metadata\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the DataHub API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: DataHub\n  ServiceCategory: Developer Tools / API\n  ProviderName: DataHub\n  PublisherName: DataHub\n  InvoiceIssuerName: DataHub\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: DataHub GraphQL API\n    baseURL: http://localhost:8080/api/graphql\n    tags:\n      - GraphQL\n      - Metadata\n      - Queries\n      - Search\n    serviceName: DataHub GraphQL API\n    serviceCategory: API\n  - name: DataHub OpenAPI\n    baseURL: http://localhost:8080/openapi/\n    tags:\n      - Entities\n      - Metadata\n      - OpenAPI\n      - REST\n    serviceName: DataHub OpenAPI\n    serviceCategory: API\n  - name: DataHub REST API\n    baseURL: http://localhost:8080/\n    tags:\n      - Entities\n      - Internal\n      - Metadata\n      - REST\n    serviceName: DataHub REST API\n    serviceCategory: API\n  - name: DataHub Python SDK\n    baseURL: https://pypi.org/project/acryl-datahub/\n\
  \    tags:\n      - Emitter\n      - Ingestion\n      - Python\n      - SDK\n    serviceName: DataHub Python SDK\n    serviceCategory: API\n  - name: DataHub Java SDK\n    baseURL: https://github.com/datahub-project/datahub\n    tags:\n      - Emitter\n      - Java\n      - Metadata\n      - SDK\n    serviceName: DataHub Java SDK\n    serviceCategory: API\n  - name: DataHub CLI\n    baseURL: https://pypi.org/project/acryl-datahub/\n    tags:\n      - CLI\n      - Command Line\n      - Ingestion\n      - Metadata\n    serviceName: DataHub CLI\n    serviceCategory: API\n  - name: DataHub Actions Framework\n    baseURL: https://pypi.org/project/acryl-datahub-actions/\n    tags:\n      - Actions\n      - Automation\n      - Events\n      - Real-Time\n    serviceName: DataHub Actions Framework\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/datahub/refs/heads/main/finops/datahub-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Catalog
- Data Discovery
- Data Governance
- Data Lineage
- Metadata
- FinOps
- Cost Management
- FOCUS
---
