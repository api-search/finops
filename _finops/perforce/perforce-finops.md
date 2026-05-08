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
  label: Perforce Helix Core API
  slug: ''
  spec_type: OpenAPI
  url: https://api.perforce.com/helix-core/openapi.json
- filename: perforce-helix-swarm-openapi.yml
  format: yaml
  label: Perforce Helix Swarm API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/perforce/refs/heads/main/openapi/perforce-helix-swarm-openapi.yml
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
description: FinOps framework definition for the Perforce API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Perforce
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Perforce
  PublisherName: Perforce
  ServiceCategory: Developer Tools / API
  ServiceName: Perforce
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
name: Perforce Finops
provider_name: Perforce
provider_slug: perforce
publisher_name: Perforce
service_category: API
slug: perforce-finops
source_filename: perforce-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Perforce\nproviderId: perforce\npublisherName: Perforce\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Perforce API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n\
  \  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n\
  \      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Perforce\n  ServiceCategory: Developer Tools / API\n  ProviderName: Perforce\n  PublisherName: Perforce\n  InvoiceIssuerName: Perforce\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description:\
  \ Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Perforce Helix Core API\n    baseURL: https://api.perforce.com/helix-core/v1\n    tags:\n      - DevOps\n      - SCM\n      - Source Control\n      - Version Control\n    serviceName: Perforce Helix Core API\n    serviceCategory: API\n  - name: Perforce P4 REST API\n    baseURL: https://p4server.example.com/api/v0\n    tags:\n      - Automation\n      - DevOps\n      - REST API\n      - Version Control\n    serviceName: Perforce P4 REST API\n    serviceCategory: API\n  - name: Perforce Helix Swarm API\n    baseURL: https://swarm.example.com/api/v10\n    tags:\n      - Code Review\n      - Collaboration\n      - Workflow\n    serviceName: Perforce Helix Swarm API\n    serviceCategory: API\n  - name: Perforce Hansoft API\n    baseURL: https://hansoft.example.com/api\n    tags:\n      - Agile\n      - Planning\n\
  \      - Project Management\n    serviceName: Perforce Hansoft API\n    serviceCategory: API\n  - name: Perforce P4 Plan API\n    baseURL: https://p4plan.example.com/api\n    tags:\n      - Agile\n      - GraphQL\n      - Planning\n      - Project Management\n    serviceName: Perforce P4 Plan API\n    serviceCategory: API\n  - name: Perforce Helix ALM REST API\n    baseURL: https://helixalm.example.com/helix-alm/api/v0\n    tags:\n      - Application Lifecycle Management\n      - Issue Tracking\n      - Requirements Management\n      - Test Management\n    serviceName: Perforce Helix ALM REST API\n    serviceCategory: API\n  - name: Perforce Helix TeamHub API\n    baseURL: https://teamhub.example.com/api/v1\n    tags:\n      - Collaboration\n      - Git\n      - Repositories\n      - Source Code Management\n    serviceName: Perforce Helix TeamHub API\n    serviceCategory: API\n  - name: Perforce P4 DAM REST API\n    baseURL: https://dam.example.com/api\n    tags:\n      - Asset Management\n\
  \      - Digital Asset Management\n      - Media\n      - Version Control\n    serviceName: Perforce P4 DAM REST API\n    serviceCategory: API\n  - name: Perforce P4 Search API\n    baseURL: https://p4search.example.com/api\n    tags:\n      - Code Search\n      - Indexing\n      - Search\n    serviceName: Perforce P4 Search API\n    serviceCategory: API\n  - name: Perforce Helix Authentication Service API\n    baseURL: https://auth.example.com\n    tags:\n      - Authentication\n      - Identity\n      - OpenID Connect\n      - SAML\n      - SSO\n    serviceName: Perforce Helix Authentication Service API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/perforce/refs/heads/main/finops/perforce-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
