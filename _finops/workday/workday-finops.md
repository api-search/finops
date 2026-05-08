---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hcm.yml
  format: yaml
  label: Workday HCM API
  slug: hcm-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/hcm.yml
- filename: financialManagement.yml
  format: yaml
  label: Workday Financial Management API
  slug: financial-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/financialManagement.yml
- filename: recruiting.yml
  format: yaml
  label: Workday Recruiting API
  slug: recruiting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/recruiting.yml
- filename: timeTracking.yml
  format: yaml
  label: Workday Time Tracking API
  slug: time-tracking-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/timeTracking.yml
- filename: benefits.yml
  format: yaml
  label: Workday Benefits API
  slug: benefits-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/benefits.yml
- filename: absenceManagement.yml
  format: yaml
  label: Workday Absence Management API
  slug: absence-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/absenceManagement.yml
- filename: compensation.yml
  format: yaml
  label: Workday Compensation API
  slug: compensation-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/compensation.yml
- filename: payroll.yml
  format: yaml
  label: Workday Payroll API
  slug: payroll-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/payroll.yml
- filename: person.yml
  format: yaml
  label: Workday Person API
  slug: person-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/person.yml
- filename: performanceManagement.yml
  format: yaml
  label: Workday Performance Management API
  slug: performance-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/performanceManagement.yml
- filename: talent.yml
  format: yaml
  label: Workday Talent Management API
  slug: talent-management-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/talent.yml
- filename: common.yml
  format: yaml
  label: Workday Common API
  slug: common-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/common.yml
- filename: staffing.yml
  format: yaml
  label: Workday Staffing API
  slug: staffing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/staffing.yml
- filename: prismAnalytics.yml
  format: yaml
  label: Workday Prism Analytics API
  slug: prism-analytics-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/prismAnalytics.yml
- filename: raas.yml
  format: yaml
  label: Workday Report-as-a-Service API
  slug: raas-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/raas.yml
- filename: wql.yml
  format: yaml
  label: Workday WQL API
  slug: wql-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/openapi/wql.yml
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
description: FinOps framework definition for the Workday API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Workday
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Workday
  PublisherName: Workday
  ServiceCategory: Developer Tools / API
  ServiceName: Workday
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
name: Workday Finops
provider_name: Workday
provider_slug: workday
publisher_name: Workday
service_category: API
slug: workday-finops
source_filename: workday-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Workday\nproviderId: workday\npublisherName: Workday\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Cloud Computing\n  - Enterprise Software\n  - Financial Management\n  - HCM\n  - SaaS\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Workday API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Workday\n  ServiceCategory: Developer Tools / API\n  ProviderName: Workday\n  PublisherName: Workday\n  InvoiceIssuerName: Workday\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Workday HCM API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/\n    tags:\n      - Human Capital Management\n      - Human Resources\n      - Payroll\n      - Talent Management\n      - Workforce\n    serviceName: Workday HCM API\n    serviceCategory: API\n  - name: Workday Financial Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/financialManagement/\n    tags:\n      - Accounting\n      - Expenses\n      - Financial Management\n      - Procurement\n      - Revenue\n    serviceName: Workday Financial Management API\n    serviceCategory: API\n  - name: Workday Recruiting API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/recruiting/\n    tags:\n\
  \      - Applications\n      - Candidates\n      - Hiring\n      - Job Postings\n      - Recruiting\n    serviceName: Workday Recruiting API\n    serviceCategory: API\n  - name: Workday Time Tracking API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/timeTracking/\n    tags:\n      - Absence\n      - Leave Management\n      - Time Tracking\n      - Timesheets\n    serviceName: Workday Time Tracking API\n    serviceCategory: API\n  - name: Workday Benefits API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/benefits/\n    tags:\n      - Benefits\n      - Coverage\n      - Enrollments\n      - Health Insurance\n    serviceName: Workday Benefits API\n    serviceCategory: API\n  - name: Workday Absence Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/absenceManagement/\n    tags:\n      - Absence Management\n      - Leave Balances\n      - Leave of Absence\n      - Time Off\n    serviceName: Workday Absence Management API\n    serviceCategory:\
  \ API\n  - name: Workday Compensation API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/compensation/\n    tags:\n      - Compensation\n      - One-Time Payments\n      - Pay Plans\n      - Scorecards\n    serviceName: Workday Compensation API\n    serviceCategory: API\n  - name: Workday Payroll API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/payroll/\n    tags:\n      - Pay Components\n      - Pay Groups\n      - Payroll\n      - Tax Rates\n    serviceName: Workday Payroll API\n    serviceCategory: API\n  - name: Workday Person API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/person/\n    tags:\n      - Contact Information\n      - Employee Data\n      - Person\n      - Workers\n    serviceName: Workday Person API\n    serviceCategory: API\n  - name: Workday Performance Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/performanceManagement/\n    tags:\n      - Feedback\n      - Goals\n      - Performance Management\n\
  \      - Reviews\n    serviceName: Workday Performance Management API\n    serviceCategory: API\n  - name: Workday Talent Management API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/talent/\n    tags:\n      - Career Development\n      - Mentorships\n      - Succession Planning\n      - Talent Management\n    serviceName: Workday Talent Management API\n    serviceCategory: API\n  - name: Workday Common API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/common/\n    tags:\n      - Common\n      - Lookup Values\n      - Reference Data\n      - Shared Services\n    serviceName: Workday Common API\n    serviceCategory: API\n  - name: Workday Staffing API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/staffing/\n    tags:\n      - Job Profiles\n      - Organizations\n      - Positions\n      - Staffing\n    serviceName: Workday Staffing API\n    serviceCategory: API\n  - name: Workday Strategic Sourcing API\n    baseURL: https://api.workdayspend.com/services/\n\
  \    tags:\n      - Awards\n      - Contracts\n      - Procurement\n      - Strategic Sourcing\n      - Suppliers\n    serviceName: Workday Strategic Sourcing API\n    serviceCategory: API\n  - name: Workday SOAP Web Services API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service/\n    tags:\n      - Enterprise Integration\n      - SOAP API\n      - Web Services\n      - WSDL\n    serviceName: Workday SOAP Web Services API\n    serviceCategory: API\n  - name: Workday Prism Analytics API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/prismAnalytics/\n    tags:\n      - Analytics\n      - Business Intelligence\n      - Datasets\n      - Prism Analytics\n    serviceName: Workday Prism Analytics API\n    serviceCategory: API\n  - name: Workday Extend API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/\n    tags:\n      - App Development\n      - Custom Applications\n      - Low Code\n      - Platform Extensibility\n    serviceName: Workday Extend API\n\
  \    serviceCategory: API\n  - name: Workday Report-as-a-Service API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service/\n    tags:\n      - Custom Reports\n      - Data Export\n      - Report as a Service\n      - Reporting\n    serviceName: Workday Report-as-a-Service API\n    serviceCategory: API\n  - name: Workday Adaptive Planning API\n    baseURL: https://api.adaptiveinsights.com/api/\n    tags:\n      - Adaptive Planning\n      - Budgeting\n      - Financial Planning\n      - Forecasting\n    serviceName: Workday Adaptive Planning API\n    serviceCategory: API\n  - name: Workday WQL API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/wql/\n    tags:\n      - Analytics\n      - Data Access\n      - Query Language\n      - Reporting\n    serviceName: Workday WQL API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost\
  \ / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday/refs/heads/main/finops/workday-finops.yml
sources: []
specification: FinOps Framework
tags:
- Cloud Computing
- Enterprise Software
- Financial Management
- HCM
- SaaS
- FinOps
- Cost Management
- FOCUS
---
