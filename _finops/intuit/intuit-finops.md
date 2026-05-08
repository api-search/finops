---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: quickbooks-accounting.yml
  format: yaml
  label: QuickBooks Online Accounting API
  slug: quickbooks-accounting
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/intuit/refs/heads/main/openapi/quickbooks-accounting.yml
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
description: FinOps framework definition for the Intuit API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Intuit
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Intuit
  PublisherName: Intuit
  ServiceCategory: Developer Tools / API
  ServiceName: Intuit
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
name: Intuit Finops
provider_name: Intuit
provider_slug: intuit
publisher_name: Intuit
service_category: API
slug: intuit-finops
source_filename: intuit-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Intuit\nproviderId: intuit\npublisherName: Intuit\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Accounting\n  - Custom Fields\n  - Financial\n  - Financial Services\n  - Invoicing\n  - Payments\n  - Payroll\n  - Project Management\n  - Sales Tax\n  - Small Business\n  - Tax\n  - Tax Preparation\n  - Taxes\n  - Time Tracking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Intuit API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to\
  \ engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload\
  \ Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Intuit\n  ServiceCategory: Developer Tools / API\n  ProviderName: Intuit\n  PublisherName: Intuit\n  InvoiceIssuerName: Intuit\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      -\
  \ consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Intuit APIs\n    baseURL: ''\n    tags:\n      - Accounting\n      - Financial\n      - Tax Preparation\n      - Taxes\n    serviceName: Intuit APIs\n    serviceCategory: API\n  - name: QuickBooks Online Accounting API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Bookkeeping\n      - Financial\n      - Invoicing\n      - Small Business\n    serviceName: QuickBooks Online Accounting API\n    serviceCategory: API\n  - name: QuickBooks Payments API\n    baseURL: ''\n    tags:\n      - Credit Cards\n      - eCommerce\n      - Financial\n      - Payments\n  \
  \  serviceName: QuickBooks Payments API\n    serviceCategory: API\n  - name: QuickBooks Payroll and Time API\n    baseURL: ''\n    tags:\n      - HR\n      - Payroll\n      - Small Business\n      - Time Tracking\n    serviceName: QuickBooks Payroll and Time API\n    serviceCategory: API\n  - name: QuickBooks Desktop API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Desktop\n      - Financial\n      - Small Business\n    serviceName: QuickBooks Desktop API\n    serviceCategory: API\n  - name: QuickBooks Projects API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Financial\n      - Project Management\n      - Projects\n      - Small Business\n    serviceName: QuickBooks Projects API\n    serviceCategory: API\n  - name: QuickBooks Custom Fields API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Custom Fields\n      - Financial\n      - Metadata\n      - Small Business\n    serviceName: QuickBooks Custom Fields API\n    serviceCategory: API\n  - name: QuickBooks\
  \ Sales Tax API\n    baseURL: ''\n    tags:\n      - Accounting\n      - Financial\n      - Sales Tax\n      - Small Business\n      - Tax\n    serviceName: QuickBooks Sales Tax API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - name: Intuit Developer\n    email: developer-support@intuit.com\n    url: https://help.developer.intuit.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/intuit/refs/heads/main/finops/intuit-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting
- Custom Fields
- Financial
- Financial Services
- Invoicing
- Payments
- Payroll
- Project Management
- Sales Tax
- Small Business
- Tax
- Tax Preparation
- Taxes
- Time Tracking
- FinOps
- Cost Management
- FOCUS
---
