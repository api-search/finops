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
description: FinOps framework definition for the Tax Reporting Templates API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Tax Reporting Templates
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Tax Reporting Templates
  PublisherName: Tax Reporting Templates
  ServiceCategory: Developer Tools / API
  ServiceName: Tax Reporting Templates
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
name: Tax Reporting Templates Finops
provider_name: Tax Reporting Templates
provider_slug: tax-reporting-templates
publisher_name: Tax Reporting Templates
service_category: API
slug: tax-reporting-templates-finops
source_filename: tax-reporting-templates-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Tax Reporting Templates\nproviderId: tax-reporting-templates\npublisherName: Tax Reporting Templates\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Compliance\n  - Documentation\n  - Finance\n  - Reporting\n  - Tax\n  - Templates\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Tax Reporting Templates API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Tax Reporting Templates\n  ServiceCategory: Developer Tools / API\n  ProviderName: Tax Reporting Templates\n  PublisherName: Tax Reporting Templates\n  InvoiceIssuerName: Tax Reporting Templates\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name:\
  \ data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: IRS Modernized e-File (MeF) API\n    baseURL: https://la1.www4.irs.gov/mef\n    tags:\n      - Compliance\n      - E-File\n      - Federal Tax\n      - IRS\n      - Tax\n    serviceName: IRS Modernized e-File (MeF) API\n    serviceCategory: API\n  - name: TaxJar API\n    baseURL: https://api.taxjar.com/v2\n    tags:\n      - Compliance\n      - Sales Tax\n      - Tax\n    serviceName: TaxJar API\n    serviceCategory: API\n  - name: Avalara AvaTax API\n    baseURL: https://rest.avatax.com/api/v2\n    tags:\n      - Compliance\n      - Global Tax\n      - Sales Tax\n      - Tax\n    serviceName:\
  \ Avalara AvaTax API\n    serviceCategory: API\n  - name: W-2 and 1099 Reporting Templates\n    baseURL: ''\n    tags:\n      - 1099\n      - Compliance\n      - Payroll\n      - Tax\n      - W-2\n    serviceName: W-2 and 1099 Reporting Templates\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers: []\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/tax-reporting-templates/refs/heads/main/finops/tax-reporting-templates-finops.yml
sources: []
specification: FinOps Framework
tags:
- Compliance
- Documentation
- Finance
- Reporting
- Tax
- Templates
- FinOps
- Cost Management
- FOCUS
---
