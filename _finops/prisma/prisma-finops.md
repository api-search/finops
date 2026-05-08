---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Prisma Data Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://api.cloud.prisma.io/openapi.json
- filename: prisma-accelerate-openapi.yml
  format: yaml
  label: Prisma Accelerate API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-accelerate-openapi.yml
- filename: prisma-pulse-openapi.yml
  format: yaml
  label: Prisma Pulse API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-pulse-openapi.yml
- filename: prisma-postgres-management-openapi.yml
  format: yaml
  label: Prisma Postgres Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-postgres-management-openapi.yml
- filename: prisma-client-openapi.yml
  format: yaml
  label: Prisma Client API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-client-openapi.yml
- filename: prisma-optimize-openapi.yml
  format: yaml
  label: Prisma Optimize API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/openapi/prisma-optimize-openapi.yml
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
description: FinOps framework definition for the Prisma API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Prisma
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Prisma
  PublisherName: Prisma
  ServiceCategory: Developer Tools / API
  ServiceName: Prisma
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
name: Prisma Finops
provider_name: Prisma
provider_slug: prisma
publisher_name: Prisma
service_category: API
slug: prisma-finops
source_filename: prisma-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Prisma\nproviderId: prisma\npublisherName: Prisma\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Prisma API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Prisma\n  ServiceCategory: Developer Tools / API\n  ProviderName: Prisma\n  PublisherName: Prisma\n  InvoiceIssuerName: Prisma\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Prisma Data Platform API\n    baseURL: ''\n    tags:\n      - Database\n      - Developer Tools\n      - ORM\n      - Platform\n    serviceName: Prisma Data Platform API\n    serviceCategory: API\n  - name: Prisma Accelerate API\n    baseURL: ''\n    tags:\n      - Caching\n      - Connection Pooling\n      - Database\n      - Performance\n      - Serverless\n    serviceName: Prisma Accelerate API\n    serviceCategory: API\n  - name: Prisma Pulse API\n    baseURL: ''\n    tags:\n      - Change Data Capture\n      - Database\n      - Events\n      - Real-Time\n      - Subscriptions\n    serviceName: Prisma Pulse API\n    serviceCategory: API\n  - name: Prisma Postgres Management API\n    baseURL: ''\n    tags:\n      - Database\n      - Infrastructure\n      - Managed Database\n      - PostgreSQL\n      -\
  \ Provisioning\n    serviceName: Prisma Postgres Management API\n    serviceCategory: API\n  - name: Prisma Client API\n    baseURL: ''\n    tags:\n      - Database\n      - Node.js\n      - ORM\n      - Query Builder\n      - TypeScript\n    serviceName: Prisma Client API\n    serviceCategory: API\n  - name: Prisma Optimize API\n    baseURL: ''\n    tags:\n      - AI\n      - Database\n      - Developer Tools\n      - Performance\n      - Query Optimization\n    serviceName: Prisma Optimize API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.prisma.io\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/prisma/refs/heads/main/finops/prisma-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
