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
description: FinOps framework definition for the Accounting Standards API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Accounting Standards
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Accounting Standards
  PublisherName: Accounting Standards
  ServiceCategory: Developer Tools / API
  ServiceName: Accounting Standards
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
name: Accounting Standards Finops
provider_name: Accounting Standards
provider_slug: accounting-standards
publisher_name: Accounting Standards
service_category: API
slug: accounting-standards-finops
source_filename: accounting-standards-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Accounting Standards\nproviderId: accounting-standards\npublisherName: Accounting Standards\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Accounting Standards\n  - Finance\n  - GAAP\n  - IFRS\n  - XBRL\n  - Financial Reporting\n  - SEC\n  - FASB\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Accounting Standards API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Accounting Standards\n  ServiceCategory: Developer Tools / API\n  ProviderName: Accounting Standards\n  PublisherName: Accounting Standards\n  InvoiceIssuerName: Accounting Standards\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n\
  \  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: US GAAP Financial Reporting Taxonomy 2026\n    baseURL: https://xbrl.fasb.org/us-gaap/2026/\n    tags:\n      - GAAP\n      - XBRL\n      - FASB\n      - SEC\n      - Financial Reporting\n    serviceName: US GAAP Financial Reporting Taxonomy 2026\n    serviceCategory: API\n  - name: SEC EDGAR XBRL API\n    baseURL: https://data.sec.gov/\n    tags:\n      - SEC\n      - EDGAR\n      - XBRL\n      - Financial Data\n      - Open Data\n      - REST API\n    serviceName: SEC EDGAR XBRL API\n    serviceCategory: API\n  - name: IFRS Accounting Standards\n    baseURL: https://www.ifrs.org/\n\
  \    tags:\n      - IFRS\n      - IASB\n      - International\n      - Financial Reporting\n      - XBRL\n    serviceName: IFRS Accounting Standards\n    serviceCategory: API\n  - name: FASB Accounting Standards Codification\n    baseURL: https://asc.fasb.org/\n    tags:\n      - GAAP\n      - FASB\n      - Codification\n      - US Accounting\n    serviceName: FASB Accounting Standards Codification\n    serviceCategory: API\n  - name: XBRL International Specification\n    baseURL: https://www.xbrl.org/\n    tags:\n      - XBRL\n      - Digital Reporting\n      - Financial Data\n      - Open Standard\n    serviceName: XBRL International Specification\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/accounting-standards/refs/heads/main/finops/accounting-standards-finops.yml
sources: []
specification: FinOps Framework
tags:
- Accounting Standards
- Finance
- GAAP
- IFRS
- XBRL
- Financial Reporting
- SEC
- FASB
- FinOps
- Cost Management
- FOCUS
---
