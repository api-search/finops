---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: salesforce-experience-cloud-sites-openapi.yml
  format: yaml
  label: Experience Cloud Sites API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-sites-openapi.yml
- filename: salesforce-experience-cloud-connect-communities-openapi.yml
  format: yaml
  label: Connect REST API (Communities)
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-connect-communities-openapi.yml
- filename: salesforce-experience-cloud-cms-connect-openapi.yml
  format: yaml
  label: CMS Connect API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-cms-connect-openapi.yml
- filename: salesforce-experience-cloud-rest-api-openapi.yml
  format: yaml
  label: Salesforce REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-rest-api-openapi.yml
- filename: salesforce-experience-cloud-templates-openapi.yml
  format: yaml
  label: Experience Cloud Templates API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-templates-openapi.yml
- filename: salesforce-experience-cloud-graphql-openapi.yml
  format: yaml
  label: GraphQL API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-graphql-openapi.yml
- filename: salesforce-experience-cloud-cms-managed-content-openapi.yml
  format: yaml
  label: CMS Managed Content API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-cms-managed-content-openapi.yml
- filename: salesforce-experience-cloud-cms-delivery-openapi.yml
  format: yaml
  label: CMS Delivery API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-cms-delivery-openapi.yml
- filename: salesforce-experience-cloud-user-interface-openapi.yml
  format: yaml
  label: User Interface API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/openapi/salesforce-experience-cloud-user-interface-openapi.yml
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
description: FinOps framework definition for the Salesforce Experience Cloud API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Salesforce Experience Cloud
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Salesforce Experience Cloud
  PublisherName: Salesforce Experience Cloud
  ServiceCategory: Developer Tools / API
  ServiceName: Salesforce Experience Cloud
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
name: Salesforce Experience Cloud Finops
provider_name: Salesforce Experience Cloud
provider_slug: salesforce-experience-cloud
publisher_name: Salesforce Experience Cloud
service_category: API
slug: salesforce-experience-cloud-finops
source_filename: salesforce-experience-cloud-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Salesforce Experience Cloud\nproviderId: salesforce-experience-cloud\npublisherName: Salesforce Experience Cloud\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - CMS\n  - Communities\n  - CRM\n  - Customer Portal\n  - Digital Experience\n  - Experience Cloud\n  - Partner Portal\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Salesforce Experience Cloud API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance\
  \ teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n\
  \      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Salesforce Experience Cloud\n  ServiceCategory: Developer Tools / API\n  ProviderName: Salesforce Experience Cloud\n  PublisherName: Salesforce Experience Cloud\n  InvoiceIssuerName: Salesforce Experience Cloud\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n\
  \      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Experience Cloud Sites API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0\n    tags:\n      - CMS\n      - Communities\n      - Configuration\n      - Digital Experiences\n      - Sites\n    serviceName: Experience Cloud Sites API\n    serviceCategory: API\n  - name: Connect REST API (Communities)\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/connect\n    tags:\n      - Chatter\n      - Communities\n      - Feeds\n      - Social\n      - Topics\n    serviceName: Connect REST API (Communities)\n\
  \    serviceCategory: API\n  - name: CMS Connect API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/connect/cms\n    tags:\n      - Channels\n      - CMS\n      - Content\n      - Media\n      - Publishing\n    serviceName: CMS Connect API\n    serviceCategory: API\n  - name: Salesforce REST API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0\n    tags:\n      - CRUD\n      - Data\n      - Objects\n      - Platform\n      - REST\n    serviceName: Salesforce REST API\n    serviceCategory: API\n  - name: Experience Cloud Templates API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0\n    tags:\n      - Branding\n      - Design\n      - LWR\n      - Templates\n      - Themes\n    serviceName: Experience Cloud Templates API\n    serviceCategory: API\n  - name: GraphQL API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/graphql\n    tags:\n      - Data\n      - GraphQL\n      - Performance\n      - Query\n\
  \    serviceName: GraphQL API\n    serviceCategory: API\n  - name: CMS Managed Content API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/connect/cms/delivery\n    tags:\n      - Channels\n      - Content Management\n      - Delivery\n      - Headless CMS\n      - Managed Content\n    serviceName: CMS Managed Content API\n    serviceCategory: API\n  - name: CMS Delivery API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/connect/cms/delivery\n    tags:\n      - Channels\n      - CMS\n      - Content Delivery\n      - Headless\n    serviceName: CMS Delivery API\n    serviceCategory: API\n  - name: User Interface API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0/ui-api\n    tags:\n      - Layouts\n      - Lightning\n      - Navigation\n      - Records\n      - User Interface\n    serviceName: User Interface API\n    serviceCategory: API\n  - name: Metadata API (Experience Cloud)\n    baseURL: https://yourInstance.salesforce.com/services/Soap/m/59.0\n\
  \    tags:\n      - CI/CD\n      - Configuration\n      - Deployment\n      - DevOps\n      - Metadata\n    serviceName: Metadata API (Experience Cloud)\n    serviceCategory: API\n  - name: LWR Sites API\n    baseURL: https://yourInstance.salesforce.com/services/data/v59.0\n    tags:\n      - Components\n      - Lightning Web Runtime\n      - LWR\n      - Performance\n      - Sites\n    serviceName: LWR Sites API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/salesforce-experience-cloud/refs/heads/main/finops/salesforce-experience-cloud-finops.yml
sources: []
specification: FinOps Framework
tags:
- CMS
- Communities
- CRM
- Customer Portal
- Digital Experience
- Experience Cloud
- Partner Portal
- FinOps
- Cost Management
- FOCUS
---
