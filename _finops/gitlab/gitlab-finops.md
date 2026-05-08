---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gitlab-api-v4-groups-openapi-original.yml
  format: yaml
  label: GitLab Groups API
  slug: apiv4groups
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-groups-openapi-original.yml
- filename: gitlab-api-v4-projects-openapi-original.yml
  format: yaml
  label: GitLab Projects API
  slug: apiv4projects
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-projects-openapi-original.yml
- filename: gitlab-api-v4-admin-openapi-original.yml
  format: yaml
  label: GitLab Admin API
  slug: apiv4admin
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-admin-openapi-original.yml
- filename: gitlab-api-v4-applications-openapi-original.yml
  format: yaml
  label: GitLab Applications API
  slug: apiv4applications
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-applications-openapi-original.yml
- filename: gitlab-api-v4-avatar-openapi-original.yml
  format: yaml
  label: GitLab Avatar API
  slug: apiv4avatar
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-avatar-openapi-original.yml
- filename: gitlab-api-v4-broadcast-messages-openapi-original.yml
  format: yaml
  label: GitLab Broadcast Messages API
  slug: apiv4broadcast-messages
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-broadcast-messages-openapi-original.yml
- filename: gitlab-api-v4-bulk-imports-openapi-original.yml
  format: yaml
  label: GitLab Bulk Imports API
  slug: apiv4bulk-imports
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-bulk-imports-openapi-original.yml
- filename: gitlab-api-v4-application-openapi-original.yml
  format: yaml
  label: GitLab Application Settings API
  slug: apiv4application
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-application-openapi-original.yml
- filename: gitlab-api-v4-metadata-openapi-original.yml
  format: yaml
  label: GitLab Metadata API
  slug: apiv4metadata
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-metadata-openapi-original.yml
- filename: gitlab-api-v4-version-openapi-original.yml
  format: yaml
  label: GitLab Version API
  slug: apiv4version
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-api-v4-version-openapi-original.yml
- filename: gitlab-openapi-original.yml
  format: yaml
  label: GitLab REST API
  slug: gitlab-rest-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-openapi-original.yml
- filename: gitlab-oauth2-openapi.yml
  format: yaml
  label: GitLab OAuth 2.0 API
  slug: gitlab-oauth2-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-oauth2-openapi.yml
- filename: gitlab-webhooks-openapi.yml
  format: yaml
  label: GitLab Webhooks
  slug: gitlab-webhooks
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/openapi/gitlab-webhooks-openapi.yml
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
description: FinOps framework definition for the GitLab API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: GitLab
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: GitLab
  PublisherName: GitLab
  ServiceCategory: Developer Tools / API
  ServiceName: GitLab
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
name: Gitlab Finops
provider_name: GitLab
provider_slug: gitlab
publisher_name: GitLab
service_category: API
slug: gitlab-finops
source_filename: gitlab-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: GitLab\nproviderId: gitlab\npublisherName: GitLab\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Code\n  - Platform\n  - Software Development\n  - Source Control\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the GitLab API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment,\
  \ application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      -\
  \ FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: GitLab\n  ServiceCategory: Developer Tools / API\n  ProviderName: GitLab\n  PublisherName: GitLab\n  InvoiceIssuerName: GitLab\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n     \
  \ - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: GitLab GraphQL API\n    baseURL: https://gitlab.com/api/graphql\n    tags:\n      - Data\n      - GraphQL\n      - Query Language\n    serviceName: GitLab GraphQL API\n    serviceCategory: API\n  - name: GitLab Groups API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Access Control\n      - Groups\n      - Organizations\n    serviceName: GitLab Groups API\n    serviceCategory: API\n  - name: GitLab Projects API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Projects\n      - Repositories\n      - Source Control\n    serviceName: GitLab Projects API\n    serviceCategory: API\n  - name: GitLab Admin API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Admin\n      - Administration\n      - Management\n\
  \    serviceName: GitLab Admin API\n    serviceCategory: API\n  - name: GitLab Applications API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Applications\n      - Authentication\n      - OAuth\n    serviceName: GitLab Applications API\n    serviceCategory: API\n  - name: GitLab Avatar API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Avatars\n      - Profile\n      - Users\n    serviceName: GitLab Avatar API\n    serviceCategory: API\n  - name: GitLab Broadcast Messages API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Administration\n      - Broadcast Messages\n      - Notifications\n    serviceName: GitLab Broadcast Messages API\n    serviceCategory: API\n  - name: GitLab Bulk Imports API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Bulk Imports\n      - Data Transfer\n      - Migration\n    serviceName: GitLab Bulk Imports API\n    serviceCategory: API\n  - name: GitLab Application Settings API\n    baseURL: https://gitlab.com/api/v4\n\
  \    tags:\n      - Administration\n      - Application Settings\n      - Configuration\n    serviceName: GitLab Application Settings API\n    serviceCategory: API\n  - name: GitLab Metadata API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Instance Information\n      - Metadata\n      - System\n    serviceName: GitLab Metadata API\n    serviceCategory: API\n  - name: GitLab Version API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Instance Information\n      - System\n      - Version\n    serviceName: GitLab Version API\n    serviceCategory: API\n  - name: GitLab REST API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - DevOps\n      - Integration\n      - REST\n    serviceName: GitLab REST API\n    serviceCategory: API\n  - name: GitLab OAuth 2.0 API\n    baseURL: https://gitlab.com\n    tags:\n      - Authentication\n      - Authorization\n      - OAuth\n    serviceName: GitLab OAuth 2.0 API\n    serviceCategory: API\n  - name: GitLab Webhooks\n\
  \    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Events\n      - Integrations\n      - Webhooks\n    serviceName: GitLab Webhooks\n    serviceCategory: API\n  - name: GitLab Issues API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Bug Tracking\n      - Issues\n      - Project Management\n    serviceName: GitLab Issues API\n    serviceCategory: API\n  - name: GitLab Merge Requests API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Code Review\n      - Collaboration\n      - Merge Requests\n    serviceName: GitLab Merge Requests API\n    serviceCategory: API\n  - name: GitLab Pipelines API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - CI/CD\n      - Continuous Integration\n      - Pipelines\n    serviceName: GitLab Pipelines API\n    serviceCategory: API\n  - name: GitLab Jobs API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Build\n      - CI/CD\n      - Jobs\n    serviceName: GitLab Jobs API\n    serviceCategory: API\n \
  \ - name: GitLab Runners API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - CI/CD\n      - Infrastructure\n      - Runners\n    serviceName: GitLab Runners API\n    serviceCategory: API\n  - name: GitLab Users API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Access Management\n      - Identity\n      - Users\n    serviceName: GitLab Users API\n    serviceCategory: API\n  - name: GitLab Repositories API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Git\n      - Repositories\n      - Source Control\n    serviceName: GitLab Repositories API\n    serviceCategory: API\n  - name: GitLab Commits API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Commits\n      - Git\n      - Source Control\n    serviceName: GitLab Commits API\n    serviceCategory: API\n  - name: GitLab Branches API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Branches\n      - Git\n      - Source Control\n    serviceName: GitLab Branches API\n    serviceCategory:\
  \ API\n  - name: GitLab Tags API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Git\n      - Source Control\n    serviceName: GitLab Tags API\n    serviceCategory: API\n  - name: GitLab Releases API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Distribution\n      - Releases\n      - Versioning\n    serviceName: GitLab Releases API\n    serviceCategory: API\n  - name: GitLab Environments API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - CI/CD\n      - Deployments\n      - Environments\n    serviceName: GitLab Environments API\n    serviceCategory: API\n  - name: GitLab Deployments API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - CI/CD\n      - Deployments\n      - Release Management\n    serviceName: GitLab Deployments API\n    serviceCategory: API\n  - name: GitLab Pipeline Schedules API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Automation\n      - CI/CD\n      - Pipeline Schedules\n    serviceName: GitLab Pipeline\
  \ Schedules API\n    serviceCategory: API\n  - name: GitLab Labels API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Labels\n      - Organization\n      - Project Management\n    serviceName: GitLab Labels API\n    serviceCategory: API\n  - name: GitLab Milestones API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Milestones\n      - Planning\n      - Project Management\n    serviceName: GitLab Milestones API\n    serviceCategory: API\n  - name: GitLab Notes API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Collaboration\n      - Comments\n      - Notes\n    serviceName: GitLab Notes API\n    serviceCategory: API\n  - name: GitLab Snippets API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Code Sharing\n      - Collaboration\n      - Snippets\n    serviceName: GitLab Snippets API\n    serviceCategory: API\n  - name: GitLab Packages API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Artifacts\n      - Package Registry\n\
  \      - Packages\n    serviceName: GitLab Packages API\n    serviceCategory: API\n  - name: GitLab Container Registry API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Container Registry\n      - Containers\n      - Docker\n    serviceName: GitLab Container Registry API\n    serviceCategory: API\n  - name: GitLab Vulnerabilities API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - DevSecOps\n      - Security\n      - Vulnerabilities\n    serviceName: GitLab Vulnerabilities API\n    serviceCategory: API\n  - name: GitLab Deploy Keys API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Deploy Keys\n      - Security\n      - SSH\n    serviceName: GitLab Deploy Keys API\n    serviceCategory: API\n  - name: GitLab Protected Branches API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Access Control\n      - Protected Branches\n      - Source Control\n    serviceName: GitLab Protected Branches API\n    serviceCategory: API\n  - name: GitLab Wikis\
  \ API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Documentation\n      - Knowledge Base\n      - Wikis\n    serviceName: GitLab Wikis API\n    serviceCategory: API\n  - name: GitLab Events API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Activity\n      - Audit\n      - Events\n    serviceName: GitLab Events API\n    serviceCategory: API\n  - name: GitLab Search API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Discovery\n      - Query\n      - Search\n    serviceName: GitLab Search API\n    serviceCategory: API\n  - name: GitLab Namespaces API\n    baseURL: https://gitlab.com/api/v4\n    tags:\n      - Namespaces\n      - Organization\n      - Structure\n    serviceName: GitLab Namespaces API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n\
  \  - FN: Kin Lane\n    url: http://apievangelist.com\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gitlab/refs/heads/main/finops/gitlab-finops.yml
sources: []
specification: FinOps Framework
tags:
- Code
- Platform
- Software Development
- Source Control
- FinOps
- Cost Management
- FOCUS
---
