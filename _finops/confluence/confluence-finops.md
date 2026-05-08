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
  label: Confluence Cloud REST API v1
  slug: ''
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/confluence/swagger.v3.json
- filename: openapi.yaml
  format: yaml
  label: Confluence Cloud REST API v2
  slug: ''
  spec_type: OpenAPI
  url: https://developer.atlassian.com/cloud/confluence/rest/v2/api-spec/
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
description: FinOps framework definition for the Confluence API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Confluence
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Confluence
  PublisherName: Confluence
  ServiceCategory: Developer Tools / API
  ServiceName: Confluence
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
name: Confluence Finops
provider_name: Confluence
provider_slug: confluence
publisher_name: Confluence
service_category: API
slug: confluence-finops
source_filename: confluence-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Confluence\nproviderId: confluence\npublisherName: Confluence\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Collaboration\n  - Content Management\n  - Documentation\n  - Knowledge Base\n  - Wiki\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Confluence API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Confluence\n  ServiceCategory: Developer Tools / API\n  ProviderName: Confluence\n  PublisherName: Confluence\n  InvoiceIssuerName: Confluence\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n\
  \    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Confluence Cloud REST API v1\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Cloud\n      - Content\n      - Rest\n      - Spaces\n    serviceName: Confluence Cloud REST API v1\n    serviceCategory: API\n  - name: Confluence Cloud REST API v2\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Cloud\n      - Pages\n      - Rest\n      - V2\n    serviceName: Confluence Cloud REST API v2\n    serviceCategory: API\n  - name: Confluence Content Properties API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Custom Data\n      - Metadata\n      - Properties\n    serviceName: Confluence Content\
  \ Properties API\n    serviceCategory: API\n  - name: Confluence Search API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Cql\n      - Query\n      - Search\n    serviceName: Confluence Search API\n    serviceCategory: API\n  - name: Confluence Content API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Blog Posts\n      - Content\n      - Create\n      - Pages\n      - Update\n    serviceName: Confluence Content API\n    serviceCategory: API\n  - name: Confluence Space API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Permissions\n      - Settings\n      - Spaces\n    serviceName: Confluence Space API\n    serviceCategory: API\n  - name: Confluence Content Labels API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Content Organization\n      - Labels\n    serviceName: Confluence Content Labels API\n    serviceCategory: API\n  - name: Confluence Analytics\
  \ API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Analytics\n      - Metrics\n      - Views\n    serviceName: Confluence Analytics API\n    serviceCategory: API\n  - name: Confluence Audit API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Audit\n      - Compliance\n      - Logging\n      - Security\n    serviceName: Confluence Audit API\n    serviceCategory: API\n  - name: Confluence Template API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Blueprints\n      - Content Creation\n      - Templates\n    serviceName: Confluence Template API\n    serviceCategory: API\n  - name: Confluence Group API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Groups\n      - Membership\n      - Users\n    serviceName: Confluence Group API\n    serviceCategory: API\n  - name: Confluence Users API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n   \
  \ tags:\n      - Permissions\n      - Profiles\n      - Users\n    serviceName: Confluence Users API\n    serviceCategory: API\n  - name: Confluence Content States API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Content States\n      - Status\n      - Workflow\n    serviceName: Confluence Content States API\n    serviceCategory: API\n  - name: Confluence Content Restrictions API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Access Control\n      - Permissions\n      - Restrictions\n    serviceName: Confluence Content Restrictions API\n    serviceCategory: API\n  - name: Confluence Space Permissions API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Access Control\n      - Authorization\n      - Space Permissions\n    serviceName: Confluence Space Permissions API\n    serviceCategory: API\n  - name: Confluence GraphQL API\n    baseURL: https://your-domain.atlassian.net/gateway/api/graphql\n\
  \    tags:\n      - Cloud\n      - Graphql\n      - Query\n    serviceName: Confluence GraphQL API\n    serviceCategory: API\n  - name: Confluence Data Center REST API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Data Center\n      - On-Premise\n      - Rest\n      - Server\n    serviceName: Confluence Data Center REST API\n    serviceCategory: API\n  - name: Confluence Content Attachments API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Attachments\n      - Files\n      - Uploads\n    serviceName: Confluence Content Attachments API\n    serviceCategory: API\n  - name: Confluence Content Body API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Content Body\n      - Conversion\n      - Formats\n    serviceName: Confluence Content Body API\n    serviceCategory: API\n  - name: Confluence Content Children and Descendants API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n\
  \    tags:\n      - Children\n      - Descendants\n      - Hierarchy\n    serviceName: Confluence Content Children and Descendants API\n    serviceCategory: API\n  - name: Confluence Content Macro Body API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Content Body\n      - Macros\n    serviceName: Confluence Content Macro Body API\n    serviceCategory: API\n  - name: Confluence Content Permissions API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Access Control\n      - Content\n      - Permissions\n    serviceName: Confluence Content Permissions API\n    serviceCategory: API\n  - name: Confluence Content Versions API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Content Management\n      - History\n      - Versions\n    serviceName: Confluence Content Versions API\n    serviceCategory: API\n  - name: Confluence Content Watches API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n\
  \    tags:\n      - Notifications\n      - Subscriptions\n      - Watches\n    serviceName: Confluence Content Watches API\n    serviceCategory: API\n  - name: Confluence Dynamic Modules API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Connect Apps\n      - Extensions\n      - Modules\n    serviceName: Confluence Dynamic Modules API\n    serviceCategory: API\n  - name: Confluence Experimental API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Experimental\n      - Preview\n    serviceName: Confluence Experimental API\n    serviceCategory: API\n  - name: Confluence Label Info API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Information\n      - Labels\n      - Metadata\n    serviceName: Confluence Label Info API\n    serviceCategory: API\n  - name: Confluence Long-Running Task API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Async\n      - Long-Running\n\
  \      - Tasks\n    serviceName: Confluence Long-Running Task API\n    serviceCategory: API\n  - name: Confluence Relation API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Associations\n      - Links\n      - Relations\n    serviceName: Confluence Relation API\n    serviceCategory: API\n  - name: Confluence Settings API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Configuration\n      - Settings\n      - Site\n    serviceName: Confluence Settings API\n    serviceCategory: API\n  - name: Confluence Space Settings API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Configuration\n      - Space Settings\n    serviceName: Confluence Space Settings API\n    serviceCategory: API\n  - name: Confluence Themes API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Appearance\n      - Customization\n      - Themes\n    serviceName: Confluence Themes API\n   \
  \ serviceCategory: API\n  - name: Confluence User Properties API\n    baseURL: https://your-domain.atlassian.net/wiki/rest/api\n    tags:\n      - Custom Data\n      - Metadata\n      - User Properties\n    serviceName: Confluence User Properties API\n    serviceCategory: API\n  - name: Confluence V2 Page API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Content\n      - Pages\n      - V2\n    serviceName: Confluence V2 Page API\n    serviceCategory: API\n  - name: Confluence V2 Blog Post API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Blog Posts\n      - Content\n      - V2\n    serviceName: Confluence V2 Blog Post API\n    serviceCategory: API\n  - name: Confluence V2 Space API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Spaces\n      - V2\n    serviceName: Confluence V2 Space API\n    serviceCategory: API\n  - name: Confluence V2 Comment API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n\
  \    tags:\n      - Comments\n      - Discussions\n      - V2\n    serviceName: Confluence V2 Comment API\n    serviceCategory: API\n  - name: Confluence V2 Attachment API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Attachments\n      - Files\n      - V2\n    serviceName: Confluence V2 Attachment API\n    serviceCategory: API\n  - name: Confluence V2 Label API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Labels\n      - Organization\n      - V2\n    serviceName: Confluence V2 Label API\n    serviceCategory: API\n  - name: Confluence V2 Task API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Action Items\n      - Tasks\n      - V2\n    serviceName: Confluence V2 Task API\n    serviceCategory: API\n  - name: Confluence V2 Whiteboard API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - V2\n      - Visual Collaboration\n      - Whiteboards\n    serviceName:\
  \ Confluence V2 Whiteboard API\n    serviceCategory: API\n  - name: Confluence V2 Custom Content API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Custom Content\n      - Extensions\n      - V2\n    serviceName: Confluence V2 Custom Content API\n    serviceCategory: API\n  - name: Confluence V2 Ancestors API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Ancestors\n      - Hierarchy\n      - V2\n    serviceName: Confluence V2 Ancestors API\n    serviceCategory: API\n  - name: Confluence V2 Children API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Children\n      - Hierarchy\n      - V2\n    serviceName: Confluence V2 Children API\n    serviceCategory: API\n  - name: Confluence V2 Descendants API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Descendants\n      - Hierarchy\n      - V2\n    serviceName: Confluence V2 Descendants API\n    serviceCategory:\
  \ API\n  - name: Confluence V2 Version API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - History\n      - V2\n      - Versions\n    serviceName: Confluence V2 Version API\n    serviceCategory: API\n  - name: Confluence V2 Like API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Engagement\n      - Likes\n      - V2\n    serviceName: Confluence V2 Like API\n    serviceCategory: API\n  - name: Confluence V2 Space Permissions API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Access Control\n      - Space Permissions\n      - V2\n    serviceName: Confluence V2 Space Permissions API\n    serviceCategory: API\n  - name: Confluence V2 Space Properties API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Metadata\n      - Space Properties\n      - V2\n    serviceName: Confluence V2 Space Properties API\n    serviceCategory: API\n  - name: Confluence V2 Space Roles\
  \ API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Authorization\n      - Space Roles\n      - V2\n    serviceName: Confluence V2 Space Roles API\n    serviceCategory: API\n  - name: Confluence V2 Content Properties API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Content Properties\n      - Metadata\n      - V2\n    serviceName: Confluence V2 Content Properties API\n    serviceCategory: API\n  - name: Confluence V2 Folder API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Folders\n      - Organization\n      - V2\n    serviceName: Confluence V2 Folder API\n    serviceCategory: API\n  - name: Confluence V2 Database API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Databases\n      - Structured Data\n      - V2\n    serviceName: Confluence V2 Database API\n    serviceCategory: API\n  - name: Confluence V2 Smart Link API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n\
  \    tags:\n      - Previews\n      - Smart Links\n      - V2\n    serviceName: Confluence V2 Smart Link API\n    serviceCategory: API\n  - name: Confluence V2 Operation API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Operations\n      - Permissions\n      - V2\n    serviceName: Confluence V2 Operation API\n    serviceCategory: API\n  - name: Confluence V2 User API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Profiles\n      - Users\n      - V2\n    serviceName: Confluence V2 User API\n    serviceCategory: API\n  - name: Confluence V2 App Properties API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - App Properties\n      - Extensions\n      - V2\n    serviceName: Confluence V2 App Properties API\n    serviceCategory: API\n  - name: Confluence V2 Content API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Content\n      - Management\n      - V2\n    serviceName:\
  \ Confluence V2 Content API\n    serviceCategory: API\n  - name: Confluence V2 Data Policies API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Data Policies\n      - Governance\n      - V2\n    serviceName: Confluence V2 Data Policies API\n    serviceCategory: API\n  - name: Confluence V2 Classification Level API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Classification\n      - Data Protection\n      - V2\n    serviceName: Confluence V2 Classification Level API\n    serviceCategory: API\n  - name: Confluence V2 Redactions API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Data Protection\n      - Redactions\n      - V2\n    serviceName: Confluence V2 Redactions API\n    serviceCategory: API\n  - name: Confluence V2 Admin Key API\n    baseURL: https://your-domain.atlassian.net/wiki/api/v2\n    tags:\n      - Admin\n      - Api Keys\n      - V2\n    serviceName: Confluence V2 Admin Key\
  \ API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/confluence/refs/heads/main/finops/confluence-finops.yml
sources: []
specification: FinOps Framework
tags:
- Collaboration
- Content Management
- Documentation
- Knowledge Base
- Wiki
- FinOps
- Cost Management
- FOCUS
---
