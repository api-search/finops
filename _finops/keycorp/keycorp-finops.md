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
description: FinOps framework definition for the KeyCorp API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: KeyCorp
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: KeyCorp
  PublisherName: KeyCorp
  ServiceCategory: Developer Tools / API
  ServiceName: KeyCorp
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
name: Keycorp Finops
provider_name: KeyCorp
provider_slug: keycorp
publisher_name: KeyCorp
service_category: API
slug: keycorp-finops
source_filename: keycorp-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: KeyCorp\nproviderId: keycorp\npublisherName: KeyCorp\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Commercial Banking\n  - Financial Services\n  - Fortune 500\n  - Payments\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the KeyCorp API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with\
  \ the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps\
  \ Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: KeyCorp\n  ServiceCategory: Developer Tools / API\n  ProviderName: KeyCorp\n  PublisherName: KeyCorp\n  InvoiceIssuerName: KeyCorp\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n  \
  \  dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: KeyBank Account Information API\n    baseURL: ''\n    tags:\n      - Account Information\n      - Commercial Banking\n    serviceName: KeyBank Account Information API\n    serviceCategory: API\n  - name: KeyBank ACH Origination API\n    baseURL: ''\n    tags:\n      - ACH\n      - Payments\n    serviceName: KeyBank ACH Origination API\n    serviceCategory: API\n  - name: KeyBank Wire Transfer API\n    baseURL: ''\n    tags:\n      - Payments\n      - Wire Transfer\n    serviceName: KeyBank Wire Transfer API\n    serviceCategory: API\n  - name: KeyBank RTP Send Payment API\n    baseURL: ''\n    tags:\n      - Payments\n      - Real-Time Payments\n    serviceName: KeyBank RTP Send Payment API\n    serviceCategory:\
  \ API\n  - name: KeyBank Account Validation API\n    baseURL: ''\n    tags:\n      - Account Validation\n      - Payments\n    serviceName: KeyBank Account Validation API\n    serviceCategory: API\n  - name: KeyBank ACH Inquiry API\n    baseURL: ''\n    tags:\n      - ACH\n      - Inquiry\n    serviceName: KeyBank ACH Inquiry API\n    serviceCategory: API\n  - name: KeyBank Wire Inquiry API\n    baseURL: ''\n    tags:\n      - Inquiry\n      - Wire Transfer\n    serviceName: KeyBank Wire Inquiry API\n    serviceCategory: API\n  - name: KeyBank RTP Inquiry API\n    baseURL: ''\n    tags:\n      - Inquiry\n      - Real-Time Payments\n    serviceName: KeyBank RTP Inquiry API\n    serviceCategory: API\n  - name: KeyBank Previous Day API\n    baseURL: ''\n    tags:\n      - Account Information\n      - Reporting\n    serviceName: KeyBank Previous Day API\n    serviceCategory: API\n  - name: KeyBank Intraday API\n    baseURL: ''\n    tags:\n      - Account Information\n      - Reporting\n  \
  \  serviceName: KeyBank Intraday API\n    serviceCategory: API\n  - name: KeyBank Check Services API\n    baseURL: ''\n    tags:\n      - Check Services\n      - Commercial Banking\n    serviceName: KeyBank Check Services API\n    serviceCategory: API\n  - name: KeyBank Webhooks\n    baseURL: ''\n    tags:\n      - Events\n      - Webhooks\n    serviceName: KeyBank Webhooks\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/keycorp/refs/heads/main/finops/keycorp-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Commercial Banking
- Financial Services
- Fortune 500
- Payments
- FinOps
- Cost Management
- FOCUS
---
