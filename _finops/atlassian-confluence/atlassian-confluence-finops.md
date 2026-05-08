---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger.v3.json
  format: json
  label: Confluence Cloud REST API
  slug: confluence-cloud-rest-api
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/confluence/swagger.v3.json
- filename: openapi-v2.v3.json
  format: json
  label: Confluence Cloud REST API V2
  slug: confluence-cloud-rest-api-v2
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/confluence/openapi-v2.v3.json
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
description: FinOps framework definition for the Atlassian Confluence API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Atlassian Confluence
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Atlassian Confluence
  PublisherName: Atlassian Confluence
  ServiceCategory: Developer Tools / API
  ServiceName: Atlassian Confluence
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
name: Atlassian Confluence Finops
provider_name: Atlassian Confluence
provider_slug: atlassian-confluence
publisher_name: Atlassian Confluence
service_category: API
slug: atlassian-confluence-finops
source_filename: atlassian-confluence-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Atlassian Confluence\nproviderId: atlassian-confluence\npublisherName: Atlassian Confluence\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Atlassian\n  - Collaboration\n  - Content Management\n  - Documentation\n  - Knowledge Management\n  - Wiki\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Atlassian Confluence API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Atlassian Confluence\n  ServiceCategory: Developer Tools / API\n  ProviderName: Atlassian Confluence\n  PublisherName: Atlassian Confluence\n  InvoiceIssuerName: Atlassian Confluence\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Confluence Cloud REST API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Content\n      - Pages\n      - REST\n      - Spaces\n    serviceName: Confluence Cloud REST API\n    serviceCategory: API\n  - name: Confluence Cloud REST API V2\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Content\n      - Pages\n      - REST\n      - Spaces\n    serviceName: Confluence Cloud REST API V2\n    serviceCategory: API\n  - name: Confluence Cloud GraphQL API\n    baseURL: https://api.atlassian.com/graphql\n    tags:\n     \
  \ - Content\n      - GraphQL\n      - Pages\n      - Spaces\n    serviceName: Confluence Cloud GraphQL API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/atlassian-confluence/refs/heads/main/finops/atlassian-confluence-finops.yml
sources: []
specification: FinOps Framework
tags:
- Atlassian
- Collaboration
- Content Management
- Documentation
- Knowledge Management
- Wiki
- FinOps
- Cost Management
- FOCUS
---
