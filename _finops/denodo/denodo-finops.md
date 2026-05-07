---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Denodo API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Denodo
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Denodo
  PublisherName: Denodo
  ServiceCategory: Developer Tools / API
  ServiceName: Denodo
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
name: Denodo Finops
provider_name: Denodo
provider_slug: denodo
publisher_name: Denodo
service_category: API
slug: denodo-finops
source_filename: denodo-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Denodo\nproviderId: denodo\npublisherName: Denodo\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Data Catalog\n  - Data Fabric\n  - Data Mesh\n  - Data Virtualization\n  - GraphQL\n  - Logical Data Warehouse\n  - OData\n  - REST\n  - Scheduler\n  - Solution Manager\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Denodo API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Denodo\n  ServiceCategory: Developer Tools / API\n  ProviderName: Denodo\n  PublisherName: Denodo\n  InvoiceIssuerName: Denodo\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Denodo Solution Manager REST API\n    baseURL: https://solution-manager.example.com/solution-manager\n    tags:\n      - Administration\n      - Clusters\n      - Deployment\n      - Environments\n      - Solution Manager\n    serviceName: Denodo Solution Manager REST API\n    serviceCategory: API\n  - name: Denodo Data Catalog REST API\n    baseURL: https://denodo.example.com/denodo-data-catalog\n    tags:\n      - Catalog\n      - Data Catalog\n      - Governance\n      - Metadata\n      - Search\n    serviceName: Denodo Data Catalog REST API\n    serviceCategory: API\n  - name: Denodo RESTful Web Service\n    baseURL: https://denodo.example.com/denodo-restfulws\n\
  \    tags:\n      - HATEOAS\n      - REST\n      - Virtual DataPort\n      - Web Services\n    serviceName: Denodo RESTful Web Service\n    serviceCategory: API\n  - name: Denodo OData 4.0 Service\n    baseURL: https://denodo.example.com/denodo-odata4-service\n    tags:\n      - OData\n      - Query\n      - REST\n      - Virtual DataPort\n    serviceName: Denodo OData 4.0 Service\n    serviceCategory: API\n  - name: Denodo GraphQL Service\n    baseURL: https://denodo.example.com/denodo-graphql-service\n    tags:\n      - GraphQL\n      - Query\n      - Virtual DataPort\n    serviceName: Denodo GraphQL Service\n    serviceCategory: API\n  - name: Denodo Scheduler REST API\n    baseURL: https://denodo.example.com/webadmin/denodo-scheduler-admin\n    tags:\n      - Jobs\n      - Scheduler\n      - Workflow\n    serviceName: Denodo Scheduler REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n\
  \  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/denodo/refs/heads/main/finops/denodo-finops.yml
sources: []
specification: FinOps Framework
tags:
- Data Catalog
- Data Fabric
- Data Mesh
- Data Virtualization
- GraphQL
- Logical Data Warehouse
- OData
- REST
- Scheduler
- Solution Manager
- FinOps
- Cost Management
- FOCUS
---
