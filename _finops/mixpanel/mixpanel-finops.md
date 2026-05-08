---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi
  format: yaml
  label: Mixpanel Ingestion API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.mixpanel.com/reference/openapi
- filename: openapi
  format: yaml
  label: Mixpanel Query API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.mixpanel.com/reference/openapi
- filename: openapi
  format: yaml
  label: Mixpanel Data Pipelines API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.mixpanel.com/reference/openapi
- filename: mixpanel-identity-openapi.yml
  format: yaml
  label: Mixpanel Identity API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-identity-openapi.yml
- filename: mixpanel-event-export-openapi.yml
  format: yaml
  label: Mixpanel Event Export API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-event-export-openapi.yml
- filename: mixpanel-lexicon-schemas-openapi.yml
  format: yaml
  label: Mixpanel Lexicon Schemas API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-lexicon-schemas-openapi.yml
- filename: mixpanel-service-accounts-openapi.yml
  format: yaml
  label: Mixpanel Service Accounts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-service-accounts-openapi.yml
- filename: mixpanel-annotations-openapi.yml
  format: yaml
  label: Mixpanel Annotations API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-annotations-openapi.yml
- filename: mixpanel-gdpr-ccpa-openapi.yml
  format: yaml
  label: Mixpanel GDPR and CCPA API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-gdpr-ccpa-openapi.yml
- filename: mixpanel-warehouse-connectors-openapi.yml
  format: yaml
  label: Mixpanel Warehouse Connectors API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/openapi/mixpanel-warehouse-connectors-openapi.yml
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
description: FinOps framework definition for the Mixpanel API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Mixpanel
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Mixpanel
  PublisherName: Mixpanel
  ServiceCategory: Developer Tools / API
  ServiceName: Mixpanel
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
name: Mixpanel Finops
provider_name: Mixpanel
provider_slug: mixpanel
publisher_name: Mixpanel
service_category: API
slug: mixpanel-finops
source_filename: mixpanel-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Mixpanel\nproviderId: mixpanel\npublisherName: Mixpanel\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Data Analysis\n  - Event Tracking\n  - Product Analytics\n  - User Behavior\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Mixpanel API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Mixpanel\n  ServiceCategory: Developer Tools / API\n  ProviderName: Mixpanel\n  PublisherName: Mixpanel\n  InvoiceIssuerName: Mixpanel\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Mixpanel Ingestion API\n    baseURL: https://api.mixpanel.com\n    tags:\n      - Analytics\n      - Events\n      - Group Profiles\n      - Ingestion\n      - Tracking\n      - User Profiles\n    serviceName: Mixpanel Ingestion API\n    serviceCategory: API\n  - name: Mixpanel Query API\n    baseURL: https://mixpanel.com/api\n    tags:\n      - Analytics\n      - Cohorts\n      - Data Export\n      - Funnels\n      - Query\n      - Retention\n      - Segmentation\n    serviceName: Mixpanel Query API\n    serviceCategory: API\n  - name: Mixpanel Data Pipelines API\n    baseURL: https://data.mixpanel.com\n    tags:\n      - Data Pipeline\n      - Export\n      - Import\n    serviceName: Mixpanel\
  \ Data Pipelines API\n    serviceCategory: API\n  - name: Mixpanel Identity API\n    baseURL: https://api.mixpanel.com\n    tags:\n      - ID Merge\n      - Identity\n      - User Management\n    serviceName: Mixpanel Identity API\n    serviceCategory: API\n  - name: Mixpanel Event Export API\n    baseURL: https://data.mixpanel.com/api/2.0\n    tags:\n      - Data Export\n      - Events\n      - Raw Data\n    serviceName: Mixpanel Event Export API\n    serviceCategory: API\n  - name: Mixpanel Lexicon Schemas API\n    baseURL: https://mixpanel.com/api/app\n    tags:\n      - Data Dictionary\n      - Data Governance\n      - Lexicon\n      - Schemas\n    serviceName: Mixpanel Lexicon Schemas API\n    serviceCategory: API\n  - name: Mixpanel Service Accounts API\n    baseURL: https://mixpanel.com/api/app\n    tags:\n      - Administration\n      - Authentication\n      - Service Accounts\n    serviceName: Mixpanel Service Accounts API\n    serviceCategory: API\n  - name: Mixpanel Annotations\
  \ API\n    baseURL: https://mixpanel.com/api/app\n    tags:\n      - Annotations\n      - Charts\n      - Reports\n    serviceName: Mixpanel Annotations API\n    serviceCategory: API\n  - name: Mixpanel GDPR and CCPA API\n    baseURL: https://mixpanel.com/api/app\n    tags:\n      - CCPA\n      - Compliance\n      - Data Deletion\n      - Data Retrieval\n      - GDPR\n      - Privacy\n    serviceName: Mixpanel GDPR and CCPA API\n    serviceCategory: API\n  - name: Mixpanel Warehouse Connectors API\n    baseURL: https://mixpanel.com/api/app\n    tags:\n      - Connectors\n      - Data Import\n      - Integrations\n      - Warehouse\n    serviceName: Mixpanel Warehouse Connectors API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url:\
  \ https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/mixpanel/refs/heads/main/finops/mixpanel-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Data Analysis
- Event Tracking
- Product Analytics
- User Behavior
- FinOps
- Cost Management
- FOCUS
---
