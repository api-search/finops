---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: contentstack-content-delivery-api-openapi.yml
  format: yaml
  label: Contentstack Content Delivery API
  slug: content-delivery-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-content-delivery-api-openapi.yml
- filename: contentstack-content-management-api-openapi.yml
  format: yaml
  label: Contentstack Content Management API
  slug: content-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-content-management-api-openapi.yml
- filename: contentstack-personalize-management-api-openapi.yml
  format: yaml
  label: Contentstack Personalize Management API
  slug: personalize-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-personalize-management-api-openapi.yml
- filename: contentstack-personalize-edge-api-openapi.yml
  format: yaml
  label: Contentstack Personalize Edge API
  slug: personalize-edge-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-personalize-edge-api-openapi.yml
- filename: contentstack-automate-management-api-openapi.yml
  format: yaml
  label: Contentstack Automate Management API
  slug: automate-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-automate-management-api-openapi.yml
- filename: contentstack-analytics-api-openapi.yml
  format: yaml
  label: Contentstack Analytics API
  slug: analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-analytics-api-openapi.yml
- filename: contentstack-scim-api-openapi.yml
  format: yaml
  label: Contentstack SCIM API
  slug: scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-scim-api-openapi.yml
- filename: contentstack-brand-kit-management-api-openapi.yml
  format: yaml
  label: Contentstack Brand Kit Management API
  slug: brand-kit-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-brand-kit-management-api-openapi.yml
- filename: contentstack-knowledge-vault-api-openapi.yml
  format: yaml
  label: Contentstack Knowledge Vault API
  slug: knowledge-vault-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-knowledge-vault-api-openapi.yml
- filename: contentstack-generative-ai-api-openapi.yml
  format: yaml
  label: Contentstack Generative AI API
  slug: generative-ai-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-generative-ai-api-openapi.yml
- filename: contentstack-launch-api-openapi.yml
  format: yaml
  label: Contentstack Launch API
  slug: launch-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/openapi/contentstack-launch-api-openapi.yml
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
description: FinOps framework definition for the contentstack API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: contentstack
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: contentstack
  PublisherName: contentstack
  ServiceCategory: Developer Tools / API
  ServiceName: contentstack
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
name: Contentstack Finops
provider_name: contentstack
provider_slug: contentstack
publisher_name: contentstack
service_category: API
slug: contentstack-finops
source_filename: contentstack-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: contentstack\nproviderId: contentstack\npublisherName: contentstack\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the contentstack API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so\
  \ cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n\
  \      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: contentstack\n  ServiceCategory: Developer Tools / API\n  ProviderName: contentstack\n  PublisherName: contentstack\n  InvoiceIssuerName: contentstack\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n\
  \      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Contentstack Content Delivery API\n    baseURL: https://cdn.contentstack.io\n    tags:\n      - Content Delivery\n      - Content Management\n      - Headless CMS\n      - REST\n    serviceName: Contentstack Content Delivery API\n    serviceCategory: API\n  - name: Contentstack Content Management API\n    baseURL: https://api.contentstack.io\n    tags:\n      - Content Management\n      - CRUD\n      - Headless CMS\n      - REST\n    serviceName: Contentstack Content Management API\n    serviceCategory: API\n  - name: Contentstack GraphQL Content Delivery API\n    baseURL: https://graphql.contentstack.com\n    tags:\n      - Content Delivery\n      - GraphQL\n      - Headless CMS\n      - Query Language\n    serviceName: Contentstack GraphQL Content\
  \ Delivery API\n    serviceCategory: API\n  - name: Contentstack Image Delivery API\n    baseURL: https://images.contentstack.io\n    tags:\n      - Asset Delivery\n      - Images\n      - Media\n      - Transformation\n    serviceName: Contentstack Image Delivery API\n    serviceCategory: API\n  - name: Contentstack Personalize Management API\n    baseURL: https://personalize-api.contentstack.com\n    tags:\n      - Audiences\n      - Content Management\n      - Experiences\n      - Personalization\n    serviceName: Contentstack Personalize Management API\n    serviceCategory: API\n  - name: Contentstack Personalize Edge API\n    baseURL: https://personalize-edge.contentstack.com\n    tags:\n      - Edge Computing\n      - Events\n      - Personalization\n      - User Attributes\n    serviceName: Contentstack Personalize Edge API\n    serviceCategory: API\n  - name: Contentstack Automate Management API\n    baseURL: https://automations-api.contentstack.com\n    tags:\n      - Automation\n\
  \      - Content Management\n      - Integration\n      - Workflows\n    serviceName: Contentstack Automate Management API\n    serviceCategory: API\n  - name: Contentstack Analytics API\n    baseURL: https://api.contentstack.io\n    tags:\n      - Analytics\n      - Metrics\n      - Monitoring\n      - Reporting\n    serviceName: Contentstack Analytics API\n    serviceCategory: API\n  - name: Contentstack SCIM API\n    baseURL: https://auth-api.contentstack.com\n    tags:\n      - Identity Management\n      - SCIM\n      - Security\n      - User Provisioning\n    serviceName: Contentstack SCIM API\n    serviceCategory: API\n  - name: Contentstack Brand Kit Management API\n    baseURL: https://brand-kits-api.contentstack.com\n    tags:\n      - AI\n      - Brand Management\n      - Content Generation\n      - Voice Profiles\n    serviceName: Contentstack Brand Kit Management API\n    serviceCategory: API\n  - name: Contentstack Knowledge Vault API\n    baseURL: https://ai.contentstack.com\n\
  \    tags:\n      - AI\n      - Knowledge Management\n      - RAG\n      - Vector Database\n    serviceName: Contentstack Knowledge Vault API\n    serviceCategory: API\n  - name: Contentstack Generative AI API\n    baseURL: https://ai.contentstack.com/brand-kits\n    tags:\n      - AI\n      - Brand Kit\n      - Content Generation\n      - Generative AI\n    serviceName: Contentstack Generative AI API\n    serviceCategory: API\n  - name: Contentstack Launch API\n    baseURL: https://launch-api.contentstack.com\n    tags:\n      - CI/CD\n      - Deployment\n      - Frontend\n      - Hosting\n    serviceName: Contentstack Launch API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/contentstack/refs/heads/main/finops/contentstack-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
