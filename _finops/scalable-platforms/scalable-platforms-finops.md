---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.yaml
  format: yaml
  label: Vercel REST API
  slug: ''
  spec_type: OpenAPI
  url: https://openapi.vercel.sh/
- filename: openapi.yaml
  format: yaml
  label: Netlify API
  slug: ''
  spec_type: OpenAPI
  url: https://open-api.netlify.com/
- filename: openapi.yaml
  format: yaml
  label: Cloudflare API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/cloudflare/api-schemas/main/openapi.yaml
- filename: api-docs
  format: yaml
  label: Heroku Platform API
  slug: ''
  spec_type: OpenAPI
  url: https://devcenter.heroku.com/api-docs
- filename: openapi.yaml
  format: yaml
  label: Fly.io Machines API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/superfly/fly-openapi/refs/heads/main/openapi.yaml
- filename: openapi.yaml
  format: yaml
  label: Render API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/renderinc/openapi-specs/main/openapi.yaml
- filename: openapi.json
  format: json
  label: Northflank API
  slug: ''
  spec_type: OpenAPI
  url: https://api.northflank.com/v1/openapi.json
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
description: FinOps framework definition for the Scalable Platforms API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Scalable Platforms
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Scalable Platforms
  PublisherName: Scalable Platforms
  ServiceCategory: Developer Tools / API
  ServiceName: Scalable Platforms
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
name: Scalable Platforms Finops
provider_name: Scalable Platforms
provider_slug: scalable-platforms
publisher_name: Scalable Platforms
service_category: API
slug: scalable-platforms-finops
source_filename: scalable-platforms-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Scalable Platforms\nproviderId: scalable-platforms\npublisherName: Scalable Platforms\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Infrastructure\n  - Deployment\n  - Developer Experience\n  - DevOps\n  - PaaS\n  - Platform\n  - Scalability\n  - Serverless\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Scalable Platforms API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n\
  \      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n   \
  \   - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Scalable Platforms\n  ServiceCategory: Developer Tools / API\n  ProviderName: Scalable Platforms\n  PublisherName: Scalable Platforms\n  InvoiceIssuerName: Scalable Platforms\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      -\
  \ consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Vercel REST API\n    baseURL: ''\n    tags:\n      - CDN\n      - Deployment\n      - Edge Computing\n      - Frontend\n      - Next.js\n      - Serverless\n      - Vercel\n    serviceName: Vercel REST API\n    serviceCategory: API\n  - name: Netlify API\n    baseURL: ''\n    tags:\n      - CDN\n      - CI/CD\n      - Deployment\n      - Frontend\n      - JAMstack\n      - Netlify\n      - Serverless\n    serviceName: Netlify API\n    serviceCategory: API\n  - name: Cloudflare API\n    baseURL: ''\n    tags:\n      - CDN\n      - Cloudflare\n      - DNS\n      - Edge\
  \ Computing\n      - Security\n      - Serverless\n      - Workers\n    serviceName: Cloudflare API\n    serviceCategory: API\n  - name: Heroku Platform API\n    baseURL: ''\n    tags:\n      - Deployment\n      - Dynos\n      - Heroku\n      - PaaS\n      - Pipelines\n      - Salesforce\n    serviceName: Heroku Platform API\n    serviceCategory: API\n  - name: Fly.io Machines API\n    baseURL: ''\n    tags:\n      - Containers\n      - Deployment\n      - Edge Computing\n      - Fly.io\n      - Global Deployment\n      - Scale To Zero\n    serviceName: Fly.io Machines API\n    serviceCategory: API\n  - name: Railway API\n    baseURL: ''\n    tags:\n      - Containers\n      - Deployment\n      - Developer Experience\n      - PaaS\n      - Railway\n      - Usage-Based Pricing\n    serviceName: Railway API\n    serviceCategory: API\n  - name: Render API\n    baseURL: ''\n    tags:\n      - Containers\n      - Deployment\n      - Managed Databases\n      - PaaS\n      - Render\n      - Serverless\n\
  \    serviceName: Render API\n    serviceCategory: API\n  - name: Northflank API\n    baseURL: ''\n    tags:\n      - BYOC\n      - CI/CD\n      - Containers\n      - Deployment\n      - Kubernetes\n      - Managed Databases\n      - Northflank\n      - PaaS\n    serviceName: Northflank API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: API Evangelist\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/scalable-platforms/refs/heads/main/finops/scalable-platforms-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Infrastructure
- Deployment
- Developer Experience
- DevOps
- PaaS
- Platform
- Scalability
- Serverless
- FinOps
- Cost Management
- FOCUS
---
