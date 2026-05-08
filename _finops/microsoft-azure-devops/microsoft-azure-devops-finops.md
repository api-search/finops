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
  label: Azure DevOps Services REST API
  slug: ''
  spec_type: OpenAPI
  url: https://learn.microsoft.com/en-us/rest/api/azure/devops/
- filename: azure-devops-work-items-api-openapi.yml
  format: yaml
  label: Azure DevOps Boards API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-work-items-api-openapi.yml
- filename: azure-devops-git-api-openapi.yml
  format: yaml
  label: Azure DevOps Repos API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-git-api-openapi.yml
- filename: azure-devops-pipelines-api-openapi.yml
  format: yaml
  label: Azure DevOps Pipelines API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-pipelines-api-openapi.yml
- filename: azure-devops-builds-api-openapi.yml
  format: yaml
  label: Azure DevOps Build API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-builds-api-openapi.yml
- filename: azure-devops-releases-api-openapi.yml
  format: yaml
  label: Azure DevOps Release API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-releases-api-openapi.yml
- filename: azure-devops-test-plans-api-openapi.yml
  format: yaml
  label: Azure DevOps Test Plans API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-test-plans-api-openapi.yml
- filename: azure-devops-artifacts-api-openapi.yml
  format: yaml
  label: Azure DevOps Artifacts API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-artifacts-api-openapi.yml
- filename: azure-devops-service-hooks-api-openapi.yml
  format: yaml
  label: Azure DevOps Service Hooks API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-service-hooks-api-openapi.yml
- filename: azure-devops-wiki-api-openapi.yml
  format: yaml
  label: Azure DevOps Wiki API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/openapi/azure-devops-wiki-api-openapi.yml
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
description: FinOps framework definition for the Azure DevOps API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Azure DevOps
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Azure DevOps
  PublisherName: Azure DevOps
  ServiceCategory: Developer Tools / API
  ServiceName: Azure DevOps
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
name: Microsoft Azure Devops Finops
provider_name: Azure DevOps
provider_slug: microsoft-azure-devops
publisher_name: Azure DevOps
service_category: API
slug: microsoft-azure-devops-finops
source_filename: microsoft-azure-devops-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Azure DevOps\nproviderId: microsoft-azure-devops\npublisherName: Azure DevOps\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agile\n  - CI/CD\n  - DevOps\n  - Project Management\n  - Version Control\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Azure DevOps API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Azure DevOps\n  ServiceCategory: Developer Tools / API\n  ProviderName: Azure DevOps\n  PublisherName: Azure DevOps\n  InvoiceIssuerName: Azure DevOps\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit:\
  \ GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Azure DevOps Services REST API\n    baseURL: https://dev.azure.com/{organization}\n    tags:\n      - DevOps\n      - REST\n    serviceName: Azure DevOps Services REST API\n    serviceCategory: API\n  - name: Azure DevOps Boards API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/wit\n    tags:\n      - Agile\n      - Boards\n      - Work Items\n    serviceName: Azure DevOps Boards API\n    serviceCategory: API\n  - name: Azure DevOps Repos API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/git\n    tags:\n      - Git\n      - Repositories\n      - Source Control\n    serviceName: Azure DevOps Repos API\n    serviceCategory: API\n  - name:\
  \ Azure DevOps Pipelines API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/pipelines\n    tags:\n      - Builds\n      - CI/CD\n      - Releases\n    serviceName: Azure DevOps Pipelines API\n    serviceCategory: API\n  - name: Azure DevOps Build API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/build\n    tags:\n      - Automation\n      - Build\n      - CI\n    serviceName: Azure DevOps Build API\n    serviceCategory: API\n  - name: Azure DevOps Release API\n    baseURL: https://vsrm.dev.azure.com/{organization}/{project}/_apis/release\n    tags:\n      - CD\n      - Deployment\n      - Release\n    serviceName: Azure DevOps Release API\n    serviceCategory: API\n  - name: Azure DevOps Test Plans API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/test\n    tags:\n      - QA\n      - Test Plans\n      - Testing\n    serviceName: Azure DevOps Test Plans API\n    serviceCategory: API\n  - name: Azure DevOps Artifacts API\n   \
  \ baseURL: https://feeds.dev.azure.com/{organization}/_apis/packaging\n    tags:\n      - Artifacts\n      - Dependencies\n      - Packages\n    serviceName: Azure DevOps Artifacts API\n    serviceCategory: API\n  - name: Azure DevOps Graph API\n    baseURL: https://vssps.dev.azure.com/{organization}/_apis/graph\n    tags:\n      - Groups\n      - Permissions\n      - Users\n    serviceName: Azure DevOps Graph API\n    serviceCategory: API\n  - name: Azure DevOps Core API\n    baseURL: https://dev.azure.com/{organization}/_apis\n    tags:\n      - Organization\n      - Projects\n      - Teams\n    serviceName: Azure DevOps Core API\n    serviceCategory: API\n  - name: Azure DevOps Security API\n    baseURL: https://dev.azure.com/{organization}/_apis/accesscontrollists\n    tags:\n      - Access Control\n      - Permissions\n      - Security\n    serviceName: Azure DevOps Security API\n    serviceCategory: API\n  - name: Azure DevOps Service Hooks API\n    baseURL: https://dev.azure.com/{organization}/_apis/hooks\n\
  \    tags:\n      - Events\n      - Integrations\n      - Webhooks\n    serviceName: Azure DevOps Service Hooks API\n    serviceCategory: API\n  - name: Azure DevOps Notifications API\n    baseURL: https://dev.azure.com/{organization}/_apis/notification\n    tags:\n      - Alerts\n      - Notifications\n      - Subscriptions\n    serviceName: Azure DevOps Notifications API\n    serviceCategory: API\n  - name: Azure DevOps Audit API\n    baseURL: https://auditservice.dev.azure.com/{organization}/_apis/audit\n    tags:\n      - Audit\n      - Compliance\n      - Security\n    serviceName: Azure DevOps Audit API\n    serviceCategory: API\n  - name: Azure DevOps Search API\n    baseURL: https://almsearch.dev.azure.com/{organization}/_apis/search\n    tags:\n      - Code\n      - Search\n      - Work Items\n    serviceName: Azure DevOps Search API\n    serviceCategory: API\n  - name: Azure DevOps Policy API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/policy\n    tags:\n\
  \      - Branch Protection\n      - Code Review\n      - Policy\n    serviceName: Azure DevOps Policy API\n    serviceCategory: API\n  - name: Azure DevOps Distributed Task API\n    baseURL: https://dev.azure.com/{organization}/_apis/distributedtask\n    tags:\n      - Agents\n      - Pipelines\n      - Pools\n    serviceName: Azure DevOps Distributed Task API\n    serviceCategory: API\n  - name: Azure DevOps Analytics OData API\n    baseURL: https://analytics.dev.azure.com/{organization}/{project}/_odata\n    tags:\n      - Analytics\n      - OData\n      - Reporting\n    serviceName: Azure DevOps Analytics OData API\n    serviceCategory: API\n  - name: Azure DevOps Wiki API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/wiki\n    tags:\n      - Documentation\n      - Pages\n      - Wiki\n    serviceName: Azure DevOps Wiki API\n    serviceCategory: API\n  - name: Azure DevOps Extension Management API\n    baseURL: https://extmgmt.dev.azure.com/{organization}/_apis/extensionmanagement\n\
  \    tags:\n      - Extensions\n      - Marketplace\n      - Plugins\n    serviceName: Azure DevOps Extension Management API\n    serviceCategory: API\n  - name: Azure DevOps Service Endpoint API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/serviceendpoint\n    tags:\n      - Integrations\n      - Pipelines\n      - Service Connections\n    serviceName: Azure DevOps Service Endpoint API\n    serviceCategory: API\n  - name: Azure DevOps TFVC API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/tfvc\n    tags:\n      - Source Control\n      - TFVC\n      - Version Control\n    serviceName: Azure DevOps TFVC API\n    serviceCategory: API\n  - name: Azure DevOps Token Administration API\n    baseURL: https://vssps.dev.azure.com/{organization}/_apis/tokenadmin\n    tags:\n      - Access Control\n      - Security\n      - Token Administration\n    serviceName: Azure DevOps Token Administration API\n    serviceCategory: API\n  - name: Azure DevOps Accounts\
  \ API\n    baseURL: https://app.vssps.visualstudio.com/_apis/accounts\n    tags:\n      - Accounts\n      - Administration\n      - Organizations\n    serviceName: Azure DevOps Accounts API\n    serviceCategory: API\n  - name: Azure DevOps Approvals and Checks API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/pipelines/checks\n    tags:\n      - Approvals\n      - Checks\n      - Pipelines\n    serviceName: Azure DevOps Approvals and Checks API\n    serviceCategory: API\n  - name: Azure DevOps Artifacts Package Types API\n    baseURL: https://pkgs.dev.azure.com/{organization}/_apis/packaging\n    tags:\n      - Maven\n      - Npm\n      - NuGet\n      - Packages\n    serviceName: Azure DevOps Artifacts Package Types API\n    serviceCategory: API\n  - name: Azure DevOps Dashboard API\n    baseURL: https://dev.azure.com/{organization}/{project}/{team}/_apis/dashboard\n    tags:\n      - Dashboards\n      - Reporting\n      - Widgets\n    serviceName: Azure DevOps Dashboard\
  \ API\n    serviceCategory: API\n  - name: Azure DevOps Favorites API\n    baseURL: https://dev.azure.com/{organization}/_apis/favorite\n    tags:\n      - Bookmarks\n      - Favorites\n      - User Preferences\n    serviceName: Azure DevOps Favorites API\n    serviceCategory: API\n  - name: Azure DevOps Identities API\n    baseURL: https://vssps.dev.azure.com/{organization}/_apis/identities\n    tags:\n      - Groups\n      - Identities\n      - Users\n    serviceName: Azure DevOps Identities API\n    serviceCategory: API\n  - name: Azure DevOps Member Entitlement Management API\n    baseURL: https://vsaex.dev.azure.com/{organization}/_apis/userentitlements\n    tags:\n      - Entitlements\n      - Licensing\n      - User Management\n    serviceName: Azure DevOps Member Entitlement Management API\n    serviceCategory: API\n  - name: Azure DevOps Permissions Report API\n    baseURL: https://dev.azure.com/{organization}/_apis/permissionsreport\n    tags:\n      - Compliance\n      - Permissions\n\
  \      - Reports\n    serviceName: Azure DevOps Permissions Report API\n    serviceCategory: API\n  - name: Azure DevOps Profile API\n    baseURL: https://app.vssps.visualstudio.com/_apis/profile/profiles\n    tags:\n      - Identity\n      - Profile\n      - Users\n    serviceName: Azure DevOps Profile API\n    serviceCategory: API\n  - name: Azure DevOps Security Roles API\n    baseURL: https://dev.azure.com/{organization}/_apis/securityroles\n    tags:\n      - Access Control\n      - Role Assignments\n      - Security Roles\n    serviceName: Azure DevOps Security Roles API\n    serviceCategory: API\n  - name: Azure DevOps Status API\n    baseURL: https://status.dev.azure.com/_apis/status\n    tags:\n      - Health\n      - Monitoring\n      - Status\n    serviceName: Azure DevOps Status API\n    serviceCategory: API\n  - name: Azure DevOps Symbol API\n    baseURL: https://artifacts.dev.azure.com/{organization}/_apis/symbol\n    tags:\n      - Artifacts\n      - Debugging\n      - Symbols\n\
  \    serviceName: Azure DevOps Symbol API\n    serviceCategory: API\n  - name: Azure DevOps Test Plan API\n    baseURL: https://dev.azure.com/{organization}/{project}/_apis/testplan\n    tags:\n      - Test Cases\n      - Test Plans\n      - Test Suites\n    serviceName: Azure DevOps Test Plan API\n    serviceCategory: API\n  - name: Azure DevOps Test Results API\n    baseURL: https://vstmr.dev.azure.com/{organization}/{project}/_apis/testresults\n    tags:\n      - Code Coverage\n      - Test Results\n      - Test Runs\n    serviceName: Azure DevOps Test Results API\n    serviceCategory: API\n  - name: Azure DevOps Token Lifecycle Management API\n    baseURL: https://vssps.dev.azure.com/{organization}/_apis/tokens\n    tags:\n      - Authentication\n      - Personal Access Tokens\n      - Tokens\n    serviceName: Azure DevOps Token Lifecycle Management API\n    serviceCategory: API\n  - name: Azure DevOps Work API\n    baseURL: https://dev.azure.com/{organization}/{project}/{team}/_apis/work\n\
  \    tags:\n      - Boards\n      - Capacity\n      - Sprints\n    serviceName: Azure DevOps Work API\n    serviceCategory: API\n  - name: Azure DevOps Work Item Tracking Process API\n    baseURL: https://dev.azure.com/{organization}/_apis/work/processes\n    tags:\n      - Customization\n      - Processes\n      - Work Item Types\n    serviceName: Azure DevOps Work Item Tracking Process API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/microsoft-azure-devops/refs/heads/main/finops/microsoft-azure-devops-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agile
- CI/CD
- DevOps
- Project Management
- Version Control
- FinOps
- Cost Management
- FOCUS
---
