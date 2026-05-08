---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: Reporting.yaml
  format: yaml
  label: Workday Report as a Service (RaaS)
  slug: ''
  spec_type: OpenAPI
  url: https://community.workday.com/sites/default/files/file-hosting/productionapi/Reporting/v1/Reporting.yaml
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
description: FinOps framework definition for the Workday Reporting API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Workday Reporting
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Workday Reporting
  PublisherName: Workday Reporting
  ServiceCategory: Developer Tools / API
  ServiceName: Workday Reporting
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
name: Workday Reporting Finops
provider_name: Workday Reporting
provider_slug: workday-reporting
publisher_name: Workday Reporting
service_category: API
slug: workday-reporting-finops
source_filename: workday-reporting-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Workday Reporting\nproviderId: workday-reporting\npublisherName: Workday Reporting\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Analytics\n  - Business Intelligence\n  - Financial Reporting\n  - Hr Data\n  - Reporting\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Workday Reporting API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description:\
  \ Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n\
  \    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Workday Reporting\n  ServiceCategory: Developer Tools / API\n  ProviderName: Workday Reporting\n  PublisherName: Workday Reporting\n  InvoiceIssuerName: Workday Reporting\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Workday Report as a Service (RaaS)\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service/{tenant}/Reporting\n    tags:\n      - Data Extraction\n      - Raas\n      - Reports\n      - Rest\n    serviceName: Workday Report as a Service (RaaS)\n    serviceCategory: API\n  - name: Workday Custom Reports API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service/{tenant}\n    tags:\n      - Custom Reports\n      - Report Execution\n      - Soap\n    serviceName: Workday Custom Reports API\n    serviceCategory: API\n  - name: Workday Advanced Reports API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service/{tenant}\n\
  \    tags:\n      - Advanced Reporting\n      - Composite Reports\n      - Matrix Reports\n    serviceName: Workday Advanced Reports API\n    serviceCategory: API\n  - name: Workday Prism Analytics REST API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/prismAnalytics/v2/{tenant}\n    tags:\n      - Analytics\n      - Data Integration\n      - Datasets\n      - Prism Analytics\n    serviceName: Workday Prism Analytics REST API\n    serviceCategory: API\n  - name: Workday Prism Analytics SOAP Web Service\n    baseURL: https://wd2-impl-services1.workday.com/ccx/service/{tenant}/Prism_Analytics\n    tags:\n      - Analytic Dimensions\n      - Hierarchies\n      - Prism Analytics\n      - SOAP\n    serviceName: Workday Prism Analytics SOAP Web Service\n    serviceCategory: API\n  - name: Workday WQL API\n    baseURL: https://wd2-impl-services1.workday.com/ccx/api/wql/v1/{tenant}\n    tags:\n      - Analytics\n      - Data Access\n      - Query Language\n      - Reporting\n  \
  \  serviceName: Workday WQL API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/workday-reporting/refs/heads/main/finops/workday-reporting-finops.yml
sources: []
specification: FinOps Framework
tags:
- Analytics
- Business Intelligence
- Financial Reporting
- Hr Data
- Reporting
- FinOps
- Cost Management
- FOCUS
---
