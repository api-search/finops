---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: montran-global-payments-hub-openapi.yml
  format: yaml
  label: Montran Global Payments Hub
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-global-payments-hub-openapi.yml
- filename: montran-instant-payments-gateway-openapi.yml
  format: yaml
  label: Montran Instant Payments Gateway
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-instant-payments-gateway-openapi.yml
- filename: montran-payments-connectivity-openapi.yml
  format: yaml
  label: Montran Payments Connectivity
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-payments-connectivity-openapi.yml
- filename: montran-corporate-payments-portal-openapi.yml
  format: yaml
  label: Montran Corporate Payments Portal
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-corporate-payments-portal-openapi.yml
- filename: montran-virtual-accounts-openapi.yml
  format: yaml
  label: Montran Virtual Accounts
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-virtual-accounts-openapi.yml
- filename: montran-sanctions-screening-openapi.yml
  format: yaml
  label: Montran Sanctions Screening
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/openapi/montran-sanctions-screening-openapi.yml
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
description: FinOps framework definition for the Montran API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Montran
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Montran
  PublisherName: Montran
  ServiceCategory: Developer Tools / API
  ServiceName: Montran
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
name: Montran Finops
provider_name: Montran
provider_slug: montran
publisher_name: Montran
service_category: API
slug: montran-finops
source_filename: montran-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Montran\nproviderId: montran\npublisherName: Montran\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Central Banking\n  - Financial Services\n  - ISO 20022\n  - Market Infrastructure\n  - Messaging\n  - Payments\n  - Real-Time Payments\n  - SWIFT\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Montran API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Montran\n  ServiceCategory: Developer Tools / API\n  ProviderName: Montran\n  PublisherName: Montran\n  InvoiceIssuerName: Montran\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Montran Global Payments Hub\n    baseURL: ''\n    tags:\n      - Clearing\n      - Cross-Border\n      - Multi-Currency\n      - Payments\n      - Settlement\n    serviceName: Montran Global Payments Hub\n    serviceCategory: API\n  - name: Montran Instant Payments Gateway\n    baseURL: ''\n    tags:\n      - Instant Payments\n      - ISO 20022\n      - Open API\n      - PSD2\n      - Real-Time\n    serviceName: Montran Instant Payments Gateway\n    serviceCategory: API\n  - name: Montran Instant Payments System\n    baseURL: ''\n    tags:\n      - Central Banking\n      - Clearing\n      - Instant Payments\n      - Market Infrastructure\n\
  \      - Real-Time\n    serviceName: Montran Instant Payments System\n    serviceCategory: API\n  - name: Montran Payments Connectivity\n    baseURL: ''\n    tags:\n      - Connectivity\n      - Integration\n      - ISO 20022\n      - Messaging\n      - SWIFT\n    serviceName: Montran Payments Connectivity\n    serviceCategory: API\n  - name: Montran Real-Time Gross Settlement\n    baseURL: ''\n    tags:\n      - Central Banking\n      - High-Value Payments\n      - Market Infrastructure\n      - RTGS\n      - Settlement\n    serviceName: Montran Real-Time Gross Settlement\n    serviceCategory: API\n  - name: Montran Automated Clearing House\n    baseURL: ''\n    tags:\n      - ACH\n      - Clearing\n      - Credit Transfers\n      - Direct Debits\n      - Payments\n    serviceName: Montran Automated Clearing House\n    serviceCategory: API\n  - name: Montran Automated Transfer System\n    baseURL: ''\n    tags:\n      - Clearing\n      - High-Value\n      - Low-Value\n      - Payments\n\
  \      - Settlement\n    serviceName: Montran Automated Transfer System\n    serviceCategory: API\n  - name: Montran Central Securities Depository\n    baseURL: ''\n    tags:\n      - Corporate Actions\n      - Depository\n      - Market Infrastructure\n      - Securities\n      - Settlement\n    serviceName: Montran Central Securities Depository\n    serviceCategory: API\n  - name: Montran Trading System\n    baseURL: ''\n    tags:\n      - Capital Markets\n      - Financial Instruments\n      - Multi-Currency\n      - Securities\n      - Trading\n    serviceName: Montran Trading System\n    serviceCategory: API\n  - name: Montran Corporate Payments Portal\n    baseURL: ''\n    tags:\n      - Banking\n      - Cash Management\n      - Corporate Payments\n      - Multi-Bank\n      - Treasury\n    serviceName: Montran Corporate Payments Portal\n    serviceCategory: API\n  - name: Montran Virtual Accounts\n    baseURL: ''\n    tags:\n      - Cash Management\n      - Open Banking\n      -\
  \ POBO\n      - Treasury\n      - Virtual Accounts\n    serviceName: Montran Virtual Accounts\n    serviceCategory: API\n  - name: Montran Intraday Liquidity Management\n    baseURL: ''\n    tags:\n      - Banking\n      - Cash Management\n      - Liquidity\n      - Monitoring\n      - Real-Time\n    serviceName: Montran Intraday Liquidity Management\n    serviceCategory: API\n  - name: Montran Cash Pool Engine\n    baseURL: ''\n    tags:\n      - Cash Pooling\n      - Liquidity\n      - Multi-Currency\n      - Sweeping\n      - Treasury\n    serviceName: Montran Cash Pool Engine\n    serviceCategory: API\n  - name: Montran Sanctions Screening\n    baseURL: ''\n    tags:\n      - AML\n      - Compliance\n      - Risk Management\n      - Sanctions\n      - Screening\n    serviceName: Montran Sanctions Screening\n    serviceCategory: API\n  - name: Montran Payments and Collections Factory\n    baseURL: ''\n    tags:\n      - COBO\n      - Collections\n      - Corporate Payments\n      -\
  \ Multi-Bank\n      - POBO\n    serviceName: Montran Payments and Collections Factory\n    serviceCategory: API\n  - name: Montran In-House Bank\n    baseURL: ''\n    tags:\n      - Centralization\n      - Corporate\n      - In-House Banking\n      - Liquidity\n      - Treasury\n    serviceName: Montran In-House Bank\n    serviceCategory: API\n  - name: Montran Mandate Management\n    baseURL: ''\n    tags:\n      - Compliance\n      - Direct Debits\n      - Mandates\n      - Payments\n      - Risk Management\n    serviceName: Montran Mandate Management\n    serviceCategory: API\n  - name: Montran Case Management\n    baseURL: ''\n    tags:\n      - Case Management\n      - Compensation\n      - Disputes\n      - Investigation\n      - Payments\n    serviceName: Montran Case Management\n    serviceCategory: API\n  - name: Montran Dispute Management\n    baseURL: ''\n    tags:\n      - Banking\n      - Case Management\n      - Disputes\n      - Payments\n      - Resolution\n    serviceName:\
  \ Montran Dispute Management\n    serviceCategory: API\n  - name: Montran Backup RTGS\n    baseURL: ''\n    tags:\n      - Backup\n      - Business Continuity\n      - Market Infrastructure\n      - RTGS\n      - Settlement\n    serviceName: Montran Backup RTGS\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://www.montran.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/montran/refs/heads/main/finops/montran-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Central Banking
- Financial Services
- ISO 20022
- Market Infrastructure
- Messaging
- Payments
- Real-Time Payments
- SWIFT
- FinOps
- Cost Management
- FOCUS
---
