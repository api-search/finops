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
description: FinOps framework definition for the Thomson Reuters API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Thomson Reuters
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Thomson Reuters
  PublisherName: Thomson Reuters
  ServiceCategory: Developer Tools / API
  ServiceName: Thomson Reuters
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
name: Thomson Reuters Finops
provider_name: Thomson Reuters
provider_slug: thomson-reuters
publisher_name: Thomson Reuters
service_category: API
slug: thomson-reuters-finops
source_filename: thomson-reuters-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Thomson Reuters\nproviderId: thomson-reuters\npublisherName: Thomson Reuters\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Legal\n  - Tax\n  - Finance\n  - Risk\n  - Fraud\n  - Compliance\n  - Data\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Thomson Reuters API surface. Provides a FOCUS-aligned\n  mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable\
  \ API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Thomson Reuters\n  ServiceCategory: Developer Tools / API\n  ProviderName: Thomson Reuters\n  PublisherName: Thomson Reuters\n  InvoiceIssuerName: Thomson Reuters\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Thomson Reuters Westlaw API\n    baseURL: ''\n    tags:\n      - Legal\n      - Research\n      - Case Law\n      - Litigation\n      - Westlaw\n    serviceName: Thomson Reuters Westlaw API\n    serviceCategory: API\n  - name: Thomson Reuters Checkpoint API\n    baseURL: ''\n    tags:\n      - Tax\n      - Accounting\n      - Checkpoint\n      - Research\n    serviceName: Thomson Reuters Checkpoint API\n    serviceCategory: API\n  - name: Thomson Reuters ONESOURCE API\n    baseURL: ''\n    tags:\n      - Tax\n      - Compliance\n      - ONESOURCE\n      - Workflow\n    serviceName: Thomson Reuters ONESOURCE API\n    serviceCategory: API\n  - name: Thomson Reuters HighQ\
  \ API\n    baseURL: ''\n    tags:\n      - Legal\n      - Document Management\n      - HighQ\n      - Collaboration\n    serviceName: Thomson Reuters HighQ API\n    serviceCategory: API\n  - name: Thomson Reuters Legal Tracker API\n    baseURL: ''\n    tags:\n      - Legal\n      - Matter Management\n      - E-billing\n      - Legal Tracker\n    serviceName: Thomson Reuters Legal Tracker API\n    serviceCategory: API\n  - name: Thomson Reuters Risk and Fraud API\n    baseURL: ''\n    tags:\n      - Risk\n      - Fraud\n      - KYC\n      - AML\n      - Identity Verification\n      - Compliance\n    serviceName: Thomson Reuters Risk and Fraud API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/thomson-reuters/refs/heads/main/finops/thomson-reuters-finops.yml
sources: []
specification: FinOps Framework
tags:
- Legal
- Tax
- Finance
- Risk
- Fraud
- Compliance
- Data
- FinOps
- Cost Management
- FOCUS
---
