---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: hmrc-vat-mtd-openapi.yml
  format: yaml
  label: HMRC VAT (Making Tax Digital) API
  slug: hmrc-vat-mtd-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/hmrc/refs/heads/main/openapi/hmrc-vat-mtd-openapi.yml
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
description: FinOps framework definition for the HMRC UK Tax Authority API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: HMRC UK Tax Authority
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: HMRC UK Tax Authority
  PublisherName: HMRC UK Tax Authority
  ServiceCategory: Developer Tools / API
  ServiceName: HMRC UK Tax Authority
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
name: Hmrc Finops
provider_name: HMRC UK Tax Authority
provider_slug: hmrc
publisher_name: HMRC UK Tax Authority
service_category: API
slug: hmrc-finops
source_filename: hmrc-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: HMRC UK Tax Authority\nproviderId: hmrc\npublisherName: HMRC UK Tax Authority\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Government\n  - Making Tax Digital\n  - Regulatory\n  - Tax\n  - UK\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the HMRC UK Tax Authority API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: HMRC UK Tax Authority\n  ServiceCategory: Developer Tools / API\n  ProviderName: HMRC UK Tax Authority\n  PublisherName: HMRC UK Tax Authority\n  InvoiceIssuerName: HMRC UK Tax Authority\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over\
  \ the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: HMRC VAT (Making Tax Digital) API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Government\n      - Making Tax Digital\n      - REST\n      - Tax\n      - UK\n      - VAT\n    serviceName: HMRC VAT (Making Tax Digital) API\n    serviceCategory: API\n  - name: HMRC Self Assessment API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Government\n      - Income Tax\n      - REST\n      - Self Assessment\n      - Tax\n      - UK\n    serviceName: HMRC Self Assessment API\n    serviceCategory: API\n  - name: HMRC PAYE (Pay As You Earn) API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n     \
  \ - Government\n      - PAYE\n      - Payroll\n      - REST\n      - Tax\n      - UK\n    serviceName: HMRC PAYE (Pay As You Earn) API\n    serviceCategory: API\n  - name: HMRC Customs Declarations API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Customs\n      - Excise\n      - Government\n      - REST\n      - Tax\n      - UK\n      - XML\n    serviceName: HMRC Customs Declarations API\n    serviceCategory: API\n  - name: HMRC Corporation Tax API\n    baseURL: https://api.service.hmrc.gov.uk\n    tags:\n      - Business\n      - Corporation Tax\n      - Government\n      - REST\n      - Tax\n      - UK\n    serviceName: HMRC Corporation Tax API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/hmrc/refs/heads/main/finops/hmrc-finops.yml
sources: []
specification: FinOps Framework
tags:
- Government
- Making Tax Digital
- Regulatory
- Tax
- UK
- FinOps
- Cost Management
- FOCUS
---
