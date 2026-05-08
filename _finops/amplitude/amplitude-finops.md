---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: amplitude-http-v2-api-openapi.yml
  format: yaml
  label: Amplitude HTTP V2 API
  slug: http-v2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-http-v2-api-openapi.yml
- filename: amplitude-identify-api-openapi.yml
  format: yaml
  label: Amplitude Identify API
  slug: identify-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-identify-api-openapi.yml
- filename: amplitude-dashboard-rest-api-openapi.yml
  format: yaml
  label: Amplitude Dashboard REST API
  slug: dashboard-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-dashboard-rest-api-openapi.yml
- filename: amplitude-export-api-openapi.yml
  format: yaml
  label: Amplitude Export API
  slug: export-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-export-api-openapi.yml
- filename: amplitude-behavioral-cohorts-api-openapi.yml
  format: yaml
  label: Amplitude Behavioral Cohorts API
  slug: behavioral-cohorts-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-behavioral-cohorts-api-openapi.yml
- filename: amplitude-taxonomy-api-openapi.yml
  format: yaml
  label: Amplitude Taxonomy API
  slug: taxonomy-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-taxonomy-api-openapi.yml
- filename: amplitude-attribution-api-openapi.yml
  format: yaml
  label: Amplitude Attribution API
  slug: attribution-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-attribution-api-openapi.yml
- filename: amplitude-chart-annotations-api-openapi.yml
  format: yaml
  label: Amplitude Chart Annotations API
  slug: chart-annotations-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-chart-annotations-api-openapi.yml
- filename: amplitude-user-profile-api-openapi.yml
  format: yaml
  label: Amplitude User Profile API
  slug: user-profile-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-user-profile-api-openapi.yml
- filename: amplitude-user-mapping-api-openapi.yml
  format: yaml
  label: Amplitude User Mapping API
  slug: user-mapping-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-user-mapping-api-openapi.yml
- filename: amplitude-scim-api-openapi.yml
  format: yaml
  label: Amplitude SCIM API
  slug: scim-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-scim-api-openapi.yml
- filename: amplitude-dsar-api-openapi.yml
  format: yaml
  label: Amplitude Data Subject Access Request API
  slug: dsar-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-dsar-api-openapi.yml
- filename: amplitude-experiment-evaluation-api-openapi.yml
  format: yaml
  label: Amplitude Experiment Evaluation API
  slug: experiment-evaluation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-experiment-evaluation-api-openapi.yml
- filename: amplitude-experiment-management-api-openapi.yml
  format: yaml
  label: Amplitude Experiment Management API
  slug: experiment-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/openapi/amplitude-experiment-management-api-openapi.yml
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
description: FinOps framework definition for the Amplitude API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Amplitude
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Amplitude
  PublisherName: Amplitude
  ServiceCategory: Developer Tools / API
  ServiceName: Amplitude
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
name: Amplitude Finops
provider_name: Amplitude
provider_slug: amplitude
publisher_name: Amplitude
service_category: API
slug: amplitude-finops
source_filename: amplitude-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Amplitude\nproviderId: amplitude\npublisherName: Amplitude\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - A/B Testing\n  - Analytics\n  - Experimentation\n  - Feature Flags\n  - Product Analytics\n  - User Behavior\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Amplitude API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag\
  \ every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Amplitude\n  ServiceCategory: Developer Tools / API\n  ProviderName: Amplitude\n  PublisherName: Amplitude\n  InvoiceIssuerName: Amplitude\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Amplitude HTTP V2 API\n    baseURL: https://api2.amplitude.com\n    tags:\n      - Analytics\n      - Events\n      - Ingestion\n      - Tracking\n    serviceName: Amplitude HTTP V2 API\n    serviceCategory: API\n  - name: Amplitude Batch Event Upload API\n    baseURL: https://api2.amplitude.com\n    tags:\n      - Analytics\n      - Batch\n      - Events\n      - Ingestion\n    serviceName: Amplitude Batch Event Upload API\n    serviceCategory: API\n  - name: Amplitude Identify API\n    baseURL: https://api2.amplitude.com\n    tags:\n      - Analytics\n      - Identity\n      - Properties\n      - Users\n    serviceName: Amplitude Identify API\n    serviceCategory:\
  \ API\n  - name: Amplitude Group Identify API\n    baseURL: https://api2.amplitude.com\n    tags:\n      - Analytics\n      - Groups\n      - Identity\n      - Properties\n    serviceName: Amplitude Group Identify API\n    serviceCategory: API\n  - name: Amplitude Dashboard REST API\n    baseURL: https://amplitude.com\n    tags:\n      - Analytics\n      - Dashboards\n      - Metrics\n      - Reporting\n    serviceName: Amplitude Dashboard REST API\n    serviceCategory: API\n  - name: Amplitude Export API\n    baseURL: https://amplitude.com\n    tags:\n      - Analytics\n      - Data\n      - Events\n      - Export\n    serviceName: Amplitude Export API\n    serviceCategory: API\n  - name: Amplitude Behavioral Cohorts API\n    baseURL: https://amplitude.com\n    tags:\n      - Analytics\n      - Cohorts\n      - Segmentation\n      - Users\n    serviceName: Amplitude Behavioral Cohorts API\n    serviceCategory: API\n  - name: Amplitude Taxonomy API\n    baseURL: https://amplitude.com\n\
  \    tags:\n      - Analytics\n      - Data Governance\n      - Events\n      - Taxonomy\n    serviceName: Amplitude Taxonomy API\n    serviceCategory: API\n  - name: Amplitude Attribution API\n    baseURL: https://api2.amplitude.com\n    tags:\n      - Analytics\n      - Attribution\n      - Campaigns\n      - Marketing\n    serviceName: Amplitude Attribution API\n    serviceCategory: API\n  - name: Amplitude Chart Annotations API\n    baseURL: https://amplitude.com\n    tags:\n      - Analytics\n      - Annotations\n      - Charts\n      - Reporting\n    serviceName: Amplitude Chart Annotations API\n    serviceCategory: API\n  - name: Amplitude Releases API\n    baseURL: https://amplitude.com\n    tags:\n      - Analytics\n      - Deployments\n      - Releases\n      - Tracking\n    serviceName: Amplitude Releases API\n    serviceCategory: API\n  - name: Amplitude Session Replay API\n    baseURL: https://amplitude.com\n    tags:\n      - Analytics\n      - Replay\n      - Sessions\n\
  \      - User Experience\n    serviceName: Amplitude Session Replay API\n    serviceCategory: API\n  - name: Amplitude User Profile API\n    baseURL: https://profile-api.amplitude.com\n    tags:\n      - Analytics\n      - Profiles\n      - Recommendations\n      - Users\n    serviceName: Amplitude User Profile API\n    serviceCategory: API\n  - name: Amplitude User Mapping API\n    baseURL: https://api2.amplitude.com\n    tags:\n      - Aliasing\n      - Analytics\n      - Identity\n      - Users\n    serviceName: Amplitude User Mapping API\n    serviceCategory: API\n  - name: Amplitude User Privacy API\n    baseURL: https://amplitude.com\n    tags:\n      - Compliance\n      - GDPR\n      - Privacy\n      - Users\n    serviceName: Amplitude User Privacy API\n    serviceCategory: API\n  - name: Amplitude SCIM API\n    baseURL: https://analytics.amplitude.com\n    tags:\n      - Access Management\n      - Identity\n      - Provisioning\n      - Users\n    serviceName: Amplitude SCIM API\n\
  \    serviceCategory: API\n  - name: Amplitude Data Subject Access Request API\n    baseURL: https://amplitude.com\n    tags:\n      - CCPA\n      - Compliance\n      - GDPR\n      - Privacy\n    serviceName: Amplitude Data Subject Access Request API\n    serviceCategory: API\n  - name: Amplitude Experiment Evaluation API\n    baseURL: https://api.lab.amplitude.com\n    tags:\n      - A/B Testing\n      - Experimentation\n      - Feature Flags\n      - Variants\n    serviceName: Amplitude Experiment Evaluation API\n    serviceCategory: API\n  - name: Amplitude Experiment Management API\n    baseURL: https://experiment.amplitude.com\n    tags:\n      - A/B Testing\n      - Experimentation\n      - Feature Flags\n      - Management\n    serviceName: Amplitude Experiment Management API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n\
  \    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/amplitude/refs/heads/main/finops/amplitude-finops.yml
sources: []
specification: FinOps Framework
tags:
- A/B Testing
- Analytics
- Experimentation
- Feature Flags
- Product Analytics
- User Behavior
- FinOps
- Cost Management
- FOCUS
---
