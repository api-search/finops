---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: gainsight-rest-api-openapi.yml
  format: yaml
  label: Gainsight REST API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-rest-api-openapi.yml
- filename: gainsight-px-api-openapi.yml
  format: yaml
  label: Gainsight PX API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-px-api-openapi.yml
- filename: gainsight-cs-company-api-openapi.yml
  format: yaml
  label: Gainsight CS Company API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-company-api-openapi.yml
- filename: gainsight-cs-person-api-openapi.yml
  format: yaml
  label: Gainsight CS Person API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-person-api-openapi.yml
- filename: gainsight-cs-custom-object-api-openapi.yml
  format: yaml
  label: Gainsight CS Custom Object API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-custom-object-api-openapi.yml
- filename: gainsight-cs-cta-api-openapi.yml
  format: yaml
  label: Gainsight CS CTA API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-cta-api-openapi.yml
- filename: gainsight-cs-timeline-api-openapi.yml
  format: yaml
  label: Gainsight CS Timeline API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-timeline-api-openapi.yml
- filename: gainsight-cs-success-plan-api-openapi.yml
  format: yaml
  label: Gainsight CS Success Plan API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-success-plan-api-openapi.yml
- filename: gainsight-cs-data-management-api-openapi.yml
  format: yaml
  label: Gainsight CS Data Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-data-management-api-openapi.yml
- filename: gainsight-cs-bulk-api-openapi.yml
  format: yaml
  label: Gainsight CS Bulk API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-bulk-api-openapi.yml
- filename: gainsight-cs-events-api-openapi.yml
  format: yaml
  label: Gainsight CS Events API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-events-api-openapi.yml
- filename: gainsight-cs-user-management-api-openapi.yml
  format: yaml
  label: Gainsight CS User Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-user-management-api-openapi.yml
- filename: gainsight-cs-customer-goals-api-openapi.yml
  format: yaml
  label: Gainsight CS Customer Goals API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-customer-goals-api-openapi.yml
- filename: gainsight-cs-renewal-center-api-openapi.yml
  format: yaml
  label: Gainsight CS Renewal Center API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-renewal-center-api-openapi.yml
- filename: gainsight-cs-task-and-playbook-api-openapi.yml
  format: yaml
  label: Gainsight CS Task and Playbook API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/openapi/gainsight-cs-task-and-playbook-api-openapi.yml
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
description: FinOps framework definition for the Gainsight API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Gainsight
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Gainsight
  PublisherName: Gainsight
  ServiceCategory: Developer Tools / API
  ServiceName: Gainsight
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
name: Gainsight Finops
provider_name: Gainsight
provider_slug: gainsight
publisher_name: Gainsight
service_category: API
slug: gainsight-finops
source_filename: gainsight-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Gainsight\nproviderId: gainsight\npublisherName: Gainsight\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Gainsight API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be\
  \ allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Gainsight\n  ServiceCategory: Developer Tools / API\n  ProviderName: Gainsight\n  PublisherName: Gainsight\n  InvoiceIssuerName: Gainsight\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n\
  \    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Gainsight REST API\n    baseURL: https://api.gainsight.com\n    tags:\n      - Analytics\n      - CRM\n      - Customer Success\n      - SaaS\n    serviceName: Gainsight REST API\n    serviceCategory: API\n  - name: Gainsight PX API\n    baseURL: https://api.aptrinsic.com/v1\n    tags:\n      - Product Analytics\n      - Product Experience\n      - User Engagement\n    serviceName: Gainsight PX API\n    serviceCategory: API\n  - name: Gainsight CS Company API\n    baseURL: https://companyapi.gainsightcloud.com\n    tags:\n      - Accounts\n      - Companies\n      - Customer Success\n    serviceName: Gainsight CS Company API\n    serviceCategory: API\n  - name: Gainsight CS Person API\n    baseURL: https://personapi.gainsightcloud.com\n    tags:\n      - Contacts\n      - Customer Success\n\
  \      - People\n    serviceName: Gainsight CS Person API\n    serviceCategory: API\n  - name: Gainsight CS Custom Object API\n    baseURL: https://customobjectapi.gainsightcloud.com\n    tags:\n      - Custom Objects\n      - Customer Success\n      - Data Management\n    serviceName: Gainsight CS Custom Object API\n    serviceCategory: API\n  - name: Gainsight CS CTA API\n    baseURL: https://cta.gainsightcloud.com\n    tags:\n      - Calls to Action\n      - Cockpit\n      - Customer Success\n    serviceName: Gainsight CS CTA API\n    serviceCategory: API\n  - name: Gainsight CS Timeline API\n    baseURL: https://timeline.gainsightcloud.com\n    tags:\n      - Activities\n      - Customer Success\n      - Timeline\n    serviceName: Gainsight CS Timeline API\n    serviceCategory: API\n  - name: Gainsight CS Success Plan API\n    baseURL: https://successplan.gainsightcloud.com\n    tags:\n      - Customer Success\n      - Goal Tracking\n      - Success Plans\n    serviceName: Gainsight\
  \ CS Success Plan API\n    serviceCategory: API\n  - name: Gainsight CS Data Management API\n    baseURL: https://data.gainsightcloud.com\n    tags:\n      - Customer Success\n      - Data Management\n      - Metadata\n    serviceName: Gainsight CS Data Management API\n    serviceCategory: API\n  - name: Gainsight CS Bulk API\n    baseURL: https://bulk.gainsightcloud.com\n    tags:\n      - Bulk Data\n      - Customer Success\n      - Data Import\n    serviceName: Gainsight CS Bulk API\n    serviceCategory: API\n  - name: Gainsight CS Events API\n    baseURL: https://events.gainsightcloud.com\n    tags:\n      - Customer Success\n      - Events\n      - Webhooks\n    serviceName: Gainsight CS Events API\n    serviceCategory: API\n  - name: Gainsight CS User Management API\n    baseURL: https://usermanagement.gainsightcloud.com\n    tags:\n      - Customer Success\n      - Provisioning\n      - SCIM\n      - User Management\n    serviceName: Gainsight CS User Management API\n    serviceCategory:\
  \ API\n  - name: Gainsight CS Customer Goals API\n    baseURL: https://goals.gainsightcloud.com\n    tags:\n      - Customer Success\n      - Goals\n      - Outcomes\n    serviceName: Gainsight CS Customer Goals API\n    serviceCategory: API\n  - name: Gainsight CS Renewal Center API\n    baseURL: https://renewals.gainsightcloud.com\n    tags:\n      - Customer Success\n      - Opportunities\n      - Renewals\n    serviceName: Gainsight CS Renewal Center API\n    serviceCategory: API\n  - name: Gainsight CS Task and Playbook API\n    baseURL: https://task.gainsightcloud.com\n    tags:\n      - Cockpit\n      - Customer Success\n      - Playbooks\n      - Tasks\n    serviceName: Gainsight CS Task and Playbook API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - name: Kin Lane\n    email:\
  \ kin@apievangelist.com\n    url: https://www.gainsight.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/gainsight/refs/heads/main/finops/gainsight-finops.yml
sources: []
specification: FinOps Framework
tags:
- FinOps
- Cost Management
- FOCUS
---
