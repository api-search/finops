---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: figma-api-openapi.yml
  format: yaml
  label: Figma API
  slug: figma-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma REST API
  slug: figma-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-files-api-openapi.yml
  format: yaml
  label: Figma Files API
  slug: figma-files-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-files-api-openapi.yml
- filename: figma-images-api-openapi.yml
  format: yaml
  label: Figma Images API
  slug: figma-images-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-images-api-openapi.yml
- filename: figma-teams-api-openapi.yml
  format: yaml
  label: Figma Teams API
  slug: figma-teams-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-teams-api-openapi.yml
- filename: figma-projects-api-openapi.yml
  format: yaml
  label: Figma Projects API
  slug: figma-projects-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-projects-api-openapi.yml
- filename: figma-me-api-openapi.yml
  format: yaml
  label: Figma Me API
  slug: figma-me-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-me-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Components API
  slug: figma-components-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-component-sets-api-openapi.yml
  format: yaml
  label: Figma Component Sets API
  slug: figma-component-sets-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-component-sets-api-openapi.yml
- filename: figma-styles-api-openapi.yml
  format: yaml
  label: Figma Styles API
  slug: figma-styles-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-styles-api-openapi.yml
- filename: figma-activity-logs-api-openapi.yml
  format: yaml
  label: Figma Activity Logs API
  slug: figma-activity-logs-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-activity-logs-api-openapi.yml
- filename: figma-payments-api-openapi.yml
  format: yaml
  label: Figma Payments API
  slug: figma-payments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-payments-api-openapi.yml
- filename: figma-dev-resources-api-openapi.yml
  format: yaml
  label: Figma Dev Resources API
  slug: figma-dev-resources-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-dev-resources-api-openapi.yml
- filename: figma-analytics-api-openapi.yml
  format: yaml
  label: Figma Analytics API
  slug: figma-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-analytics-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Comments API
  slug: figma-comments-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Version History API
  slug: figma-version-history-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Variables API
  slug: figma-variables-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
- filename: figma-rest-api-openapi.yml
  format: yaml
  label: Figma Library Analytics API
  slug: figma-library-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/openapi/figma-rest-api-openapi.yml
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
description: FinOps framework definition for the Figma API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Figma
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Figma
  PublisherName: Figma
  ServiceCategory: Developer Tools / API
  ServiceName: Figma
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
name: Figma Finops
provider_name: Figma
provider_slug: figma
publisher_name: Figma
service_category: API
slug: figma-finops
source_filename: figma-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Figma\nproviderId: figma\npublisherName: Figma\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Collaboration\n  - Design\n  - Graphics\n  - Interfaces\n  - Prototypes\n  - Prototyping\n  - UI/UX\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Figma API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Figma\n  ServiceCategory: Developer Tools / API\n  ProviderName: Figma\n  PublisherName: Figma\n  InvoiceIssuerName: Figma\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n\
  \    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Figma API\n    baseURL: https://api.figma.com\n    tags:\n      - Design\n      - Users\n    serviceName: Figma API\n    serviceCategory: API\n  - name: Figma REST API\n    baseURL: https://api.figma.com\n    tags:\n      - Comments\n      - Components\n      - Files\n      - Projects\n      - Users\n    serviceName: Figma REST API\n    serviceCategory: API\n  - name: Figma Files API\n    baseURL: https://api.figma.com\n    tags:\n      - Dev Resources\n      - Files\n    serviceName: Figma Files API\n    serviceCategory: API\n  - name: Figma Images API\n    baseURL: https://api.figma.com\n    tags:\n      - Export\n      - Images\n      - Rendering\n    serviceName: Figma Images API\n    serviceCategory:\
  \ API\n  - name: Figma Teams API\n    baseURL: https://api.figma.com\n    tags:\n      - Teams\n      - Webhooks\n    serviceName: Figma Teams API\n    serviceCategory: API\n  - name: Figma Projects API\n    baseURL: https://api.figma.com\n    tags:\n      - Files\n      - Projects\n    serviceName: Figma Projects API\n    serviceCategory: API\n  - name: Figma Me API\n    baseURL: https://api.figma.com\n    tags:\n      - Authentication\n      - Users\n    serviceName: Figma Me API\n    serviceCategory: API\n  - name: Figma Components API\n    baseURL: https://api.figma.com\n    tags:\n      - Components\n      - Design Systems\n      - Libraries\n    serviceName: Figma Components API\n    serviceCategory: API\n  - name: Figma Component Sets API\n    baseURL: https://api.figma.com\n    tags:\n      - Component Sets\n      - Design Systems\n    serviceName: Figma Component Sets API\n    serviceCategory: API\n  - name: Figma Styles API\n    baseURL: https://api.figma.com\n    tags:\n   \
  \   - Design Systems\n      - Styles\n    serviceName: Figma Styles API\n    serviceCategory: API\n  - name: Figma Activity Logs API\n    baseURL: https://api.figma.com\n    tags:\n      - Activity Logs\n      - Audit\n      - Compliance\n    serviceName: Figma Activity Logs API\n    serviceCategory: API\n  - name: Figma Payments API\n    baseURL: https://api.figma.com\n    tags:\n      - Monetization\n      - Payments\n      - Plugins\n    serviceName: Figma Payments API\n    serviceCategory: API\n  - name: Figma Dev Resources API\n    baseURL: https://api.figma.com\n    tags:\n      - Design to Code\n      - Dev Resources\n      - Development\n    serviceName: Figma Dev Resources API\n    serviceCategory: API\n  - name: Figma Analytics API\n    baseURL: https://api.figma.com\n    tags:\n      - Analytics\n      - Design Systems\n      - Libraries\n    serviceName: Figma Analytics API\n    serviceCategory: API\n  - name: Figma Comments API\n    baseURL: https://api.figma.com\n    tags:\n\
  \      - Annotations\n      - Collaboration\n      - Comments\n      - Reactions\n    serviceName: Figma Comments API\n    serviceCategory: API\n  - name: Figma Version History API\n    baseURL: https://api.figma.com\n    tags:\n      - Files\n      - History\n      - Versions\n    serviceName: Figma Version History API\n    serviceCategory: API\n  - name: Figma Variables API\n    baseURL: https://api.figma.com\n    tags:\n      - Collections\n      - Design Tokens\n      - Variables\n    serviceName: Figma Variables API\n    serviceCategory: API\n  - name: Figma Library Analytics API\n    baseURL: https://api.figma.com\n    tags:\n      - Analytics\n      - Components\n      - Libraries\n      - Styles\n      - Usages\n      - Variables\n    serviceName: Figma Library Analytics API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n  - name: Figma\n    email: support@figma.com\n    url: https://www.figma.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/figma/refs/heads/main/finops/figma-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Design
- Graphics
- Interfaces
- Prototypes
- Prototyping
- UI/UX
- FinOps
- Cost Management
- FOCUS
---
