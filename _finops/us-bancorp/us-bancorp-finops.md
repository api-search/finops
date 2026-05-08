---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: us-bank-corporate-account-information-openapi.yml
  format: yaml
  label: US Bank Corporate Account Information API
  slug: us-bank-corporate-account-information
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-bancorp/refs/heads/main/openapi/us-bank-corporate-account-information-openapi.yml
- filename: us-bank-rtp-openapi.yml
  format: yaml
  label: US Bank RTP Real-Time Payments API
  slug: us-bank-rtp
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-bancorp/refs/heads/main/openapi/us-bank-rtp-openapi.yml
- filename: us-bank-ach-originations-openapi.yml
  format: yaml
  label: US Bank ACH Originations API
  slug: us-bank-ach-originations
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-bancorp/refs/heads/main/openapi/us-bank-ach-originations-openapi.yml
- filename: us-bank-positive-pay-openapi.yml
  format: yaml
  label: US Bank Positive Pay API
  slug: us-bank-positive-pay
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-bancorp/refs/heads/main/openapi/us-bank-positive-pay-openapi.yml
- filename: us-bank-push-to-card-openapi.yml
  format: yaml
  label: US Bank Push to Card API
  slug: us-bank-push-to-card
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/us-bancorp/refs/heads/main/openapi/us-bank-push-to-card-openapi.yml
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
description: FinOps framework definition for the US Bancorp API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: US Bancorp
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: US Bancorp
  PublisherName: US Bancorp
  ServiceCategory: Developer Tools / API
  ServiceName: US Bancorp
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
name: Us Bancorp Finops
provider_name: US Bancorp
provider_slug: us-bancorp
publisher_name: US Bancorp
service_category: API
slug: us-bancorp-finops
source_filename: us-bancorp-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: US Bancorp\nproviderId: us-bancorp\npublisherName: US Bancorp\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Finance\n  - Fortune 500\n  - Corporate Banking\n  - Payments\n  - Open Banking\n  - Treasury Management\n  - Consumer Banking\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the US Bancorp API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name:\
  \ Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  -\
  \ name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: US Bancorp\n  ServiceCategory: Developer Tools / API\n  ProviderName: US Bancorp\n  PublisherName: US Bancorp\n  InvoiceIssuerName: US Bancorp\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: US Bank Corporate Account Information API\n    baseURL: https://api.usbank.com\n    tags:\n      - Banking\n      - Corporate Banking\n      - Account Information\n      - Treasury Management\n      - Finance\n      - Fortune 500\n    serviceName: US Bank Corporate Account Information API\n    serviceCategory: API\n  - name: US Bank RTP Real-Time Payments API\n    baseURL: ''\n    tags:\n      - Payments\n      - Real-Time Payments\n      - RTP\n      - Banking\n      - Treasury Management\n      - Finance\n    serviceName: US Bank RTP Real-Time Payments API\n    serviceCategory: API\n  - name: US Bank ACH Originations API\n    baseURL:\
  \ ''\n    tags:\n      - Payments\n      - ACH\n      - Banking\n      - Corporate Payments\n      - Finance\n    serviceName: US Bank ACH Originations API\n    serviceCategory: API\n  - name: US Bank Positive Pay API\n    baseURL: ''\n    tags:\n      - Payments\n      - Fraud Prevention\n      - Check Management\n      - Treasury Management\n      - Banking\n    serviceName: US Bank Positive Pay API\n    serviceCategory: API\n  - name: US Bank Push to Card API\n    baseURL: ''\n    tags:\n      - Payments\n      - Disbursements\n      - Debit Card\n      - Banking\n      - Finance\n    serviceName: US Bank Push to Card API\n    serviceCategory: API\n  - name: US Bank Wire Transfers API\n    baseURL: ''\n    tags:\n      - Payments\n      - Wire Transfers\n      - Banking\n      - Treasury Management\n      - Finance\n    serviceName: US Bank Wire Transfers API\n    serviceCategory: API\n  - name: US Bank Data Toolbox API\n    baseURL: ''\n    tags:\n      - Banking\n      - Account Data\n\
  \      - Retail Banking\n      - Finance\n      - Open Banking\n    serviceName: US Bank Data Toolbox API\n    serviceCategory: API\n  - name: US Bank Voyager Fleet API\n    baseURL: ''\n    tags:\n      - Fleet Management\n      - Transportation\n      - Banking\n      - Finance\n      - Corporate Payments\n    serviceName: US Bank Voyager Fleet API\n    serviceCategory: API\n  - name: US Bank Freight Payment API\n    baseURL: ''\n    tags:\n      - Freight Payment\n      - Transportation\n      - Banking\n      - Finance\n      - Supply Chain\n    serviceName: US Bank Freight Payment API\n    serviceCategory: API\n  - name: US Bank Instant Payments API\n    baseURL: ''\n    tags:\n      - Payments\n      - Instant Payments\n      - Banking\n      - Finance\n    serviceName: US Bank Instant Payments API\n    serviceCategory: API\n  - name: US Bank Holidays API\n    baseURL: ''\n    tags:\n      - Banking\n      - Holidays\n      - Reference Data\n      - Finance\n    serviceName: US Bank\
  \ Holidays API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/us-bancorp/refs/heads/main/finops/us-bancorp-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Finance
- Fortune 500
- Corporate Banking
- Payments
- Open Banking
- Treasury Management
- Consumer Banking
- FinOps
- Cost Management
- FOCUS
---
