---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
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
description: FinOps framework definition for the Automatic Data Processing (ADP) API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Automatic Data Processing (ADP)
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Automatic Data Processing (ADP)
  PublisherName: Automatic Data Processing (ADP)
  ServiceCategory: Developer Tools / API
  ServiceName: Automatic Data Processing (ADP)
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
name: Automatic Data Processing Finops
provider_name: Automatic Data Processing (ADP)
provider_slug: automatic-data-processing
publisher_name: Automatic Data Processing (ADP)
service_category: API
slug: automatic-data-processing-finops
source_filename: automatic-data-processing-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Automatic Data Processing (ADP)\nproviderId: automatic-data-processing\npublisherName: Automatic Data Processing (ADP)\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - HCM\n  - Human Capital Management\n  - HR\n  - Payroll\n  - Benefits\n  - Workforce Management\n  - Tax Compliance\n  - Enterprise\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Automatic Data Processing (ADP) API surface. Provides\n  a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across\n  the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to\
  \ engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Automatic Data Processing (ADP)\n  ServiceCategory: Developer Tools / API\n  ProviderName: Automatic Data Processing (ADP)\n  PublisherName: Automatic Data Processing (ADP)\n  InvoiceIssuerName: Automatic Data Processing (ADP)\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation:\
  \ sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: ADP Payroll API\n    baseURL: https://api.adp.com\n    tags:\n      - Payroll\n      - Earnings\n      - Deductions\n      - Pay Statements\n      - Tax\n    serviceName: ADP Payroll API\n    serviceCategory: API\n  - name: ADP Worker Demographics API\n    baseURL: https://api.adp.com\n    tags:\n      - Worker Demographics\n      - Employee Data\n      - HR\n      - Workforce\n    serviceName: ADP Worker Demographics API\n    serviceCategory: API\n  - name: ADP Time and Labor\
  \ API\n    baseURL: https://api.adp.com\n    tags:\n      - Time and Attendance\n      - Scheduling\n      - Timekeeping\n      - Labor Management\n    serviceName: ADP Time and Labor API\n    serviceCategory: API\n  - name: ADP Benefits API\n    baseURL: https://api.adp.com\n    tags:\n      - Benefits\n      - Enrollment\n      - Healthcare\n      - Insurance\n    serviceName: ADP Benefits API\n    serviceCategory: API\n  - name: ADP Talent Management API\n    baseURL: https://api.adp.com\n    tags:\n      - Talent Management\n      - Performance Reviews\n      - Learning\n      - Succession Planning\n    serviceName: ADP Talent Management API\n    serviceCategory: API\n  - name: ADP Recruiting API\n    baseURL: https://api.adp.com\n    tags:\n      - Recruiting\n      - Applicant Tracking\n      - Onboarding\n      - HR\n    serviceName: ADP Recruiting API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n   \
  \ target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/automatic-data-processing/refs/heads/main/finops/automatic-data-processing-finops.yml
sources: []
specification: FinOps Framework
tags:
- HCM
- Human Capital Management
- HR
- Payroll
- Benefits
- Workforce Management
- Tax Compliance
- Enterprise
- FinOps
- Cost Management
- FOCUS
---
