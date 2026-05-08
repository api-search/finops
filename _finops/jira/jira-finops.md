---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: swagger-v3.v3.json
  format: json
  label: Jira Cloud Platform REST API
  slug: ''
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/platform/swagger-v3.v3.json
- filename: swagger.v3.json
  format: json
  label: Jira Software Cloud REST API
  slug: ''
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/software/swagger.v3.json
- filename: swagger.v3.json
  format: json
  label: Jira Service Management REST API
  slug: ''
  spec_type: OpenAPI
  url: https://dac-static.atlassian.com/cloud/jira/service-desk/swagger.v3.json
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
description: FinOps framework definition for the Jira API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Jira
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Jira
  PublisherName: Jira
  ServiceCategory: Developer Tools / API
  ServiceName: Jira
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
name: Jira Finops
provider_name: Jira
provider_slug: jira
publisher_name: Jira
service_category: API
slug: jira-finops
source_filename: jira-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Jira\nproviderId: jira\npublisherName: Jira\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Agile\n  - Issue Tracking\n  - ITSM\n  - Project Management\n  - Service Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Jira API surface. Provides a FOCUS-aligned mapping for\n  cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming\
  \ team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice\
  \ Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Jira\n  ServiceCategory: Developer Tools / API\n  ProviderName: Jira\n  PublisherName: Jira\n  InvoiceIssuerName: Jira\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      -\
  \ api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Jira Cloud Platform REST API\n    baseURL: https://your-domain.atlassian.net/rest/api/3\n    tags:\n      - Agile\n      - Issues\n      - Project Management\n      - Projects\n      - Workflows\n    serviceName: Jira Cloud Platform REST API\n    serviceCategory: API\n  - name: Jira Cloud Platform REST API v2\n    baseURL: https://your-domain.atlassian.net/rest/api/2\n    tags:\n      - Issues\n      - Legacy\n      - Project Management\n      - Projects\n      - Workflows\n    serviceName: Jira Cloud Platform REST API v2\n    serviceCategory: API\n  - name: Jira Software Cloud REST API\n    baseURL: https://your-domain.atlassian.net/rest/agile/1.0\n    tags:\n      - Agile\n      - Boards\n      - Kanban\n      - Scrum\n \
  \     - Sprints\n    serviceName: Jira Software Cloud REST API\n    serviceCategory: API\n  - name: Jira Service Management REST API\n    baseURL: https://your-domain.atlassian.net/rest/servicedeskapi\n    tags:\n      - Customers\n      - ITSM\n      - Requests\n      - Service Desk\n      - SLA\n    serviceName: Jira Service Management REST API\n    serviceCategory: API\n  - name: Jira Service Management Operations REST API\n    baseURL: https://api.atlassian.com/jsm/ops/api/{cloudId}\n    tags:\n      - Alerts\n      - Escalations\n      - Incidents\n      - On-Call\n      - Operations\n      - Schedules\n    serviceName: Jira Service Management Operations REST API\n    serviceCategory: API\n  - name: Jira Align REST API\n    baseURL: https://your-domain.jiraalign.com/rest/align/api/2\n    tags:\n      - Enterprise Agile\n      - Planning\n      - Portfolios\n      - Program Management\n      - SAFe\n    serviceName: Jira Align REST API\n    serviceCategory: API\n  - name: Jira Customer\
  \ Service Management REST API\n    baseURL: https://your-domain.atlassian.net\n    tags:\n      - Customer Service\n      - Customers\n      - Entitlements\n      - Organizations\n    serviceName: Jira Customer Service Management REST API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Atlassian\n    email: ecosystem@atlassian.com\n    url: https://www.atlassian.com\n  - name: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/jira/refs/heads/main/finops/jira-finops.yml
sources: []
specification: FinOps Framework
tags:
- Agile
- Issue Tracking
- ITSM
- Project Management
- Service Management
- FinOps
- Cost Management
- FOCUS
---
