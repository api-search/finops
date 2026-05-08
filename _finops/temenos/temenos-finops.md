---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: openapi.json
  format: json
  label: Temenos Transact API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/transact/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Infinity API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/infinity/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Payments API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/payments/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Fund Administration API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/funds/openapi.json
- filename: openapi.json
  format: json
  label: Temenos Financial Crime Mitigation API
  slug: ''
  spec_type: OpenAPI
  url: https://developer.temenos.com/fcm/openapi.json
- filename: temenos-data-hub-openapi.yml
  format: yaml
  label: Temenos Transact Data Hub API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-data-hub-openapi.yml
- filename: temenos-wealth-openapi.yml
  format: yaml
  label: Temenos Wealth API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-wealth-openapi.yml
- filename: temenos-enterprise-product-pricing-openapi.yml
  format: yaml
  label: Temenos Enterprise Product and Pricing API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-enterprise-product-pricing-openapi.yml
- filename: temenos-cloud-banking-openapi.yml
  format: yaml
  label: Temenos Cloud Banking (CMB) API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-cloud-banking-openapi.yml
- filename: temenos-journey-manager-openapi.yml
  format: yaml
  label: Temenos Journey Manager API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-journey-manager-openapi.yml
- filename: temenos-microservices-openapi.yml
  format: yaml
  label: Temenos Transact Microservices API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-microservices-openapi.yml
- filename: temenos-bnpl-openapi.yml
  format: yaml
  label: Temenos Buy Now Pay Later API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/openapi/temenos-bnpl-openapi.yml
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
description: FinOps framework definition for the Temenos API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Temenos
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Temenos
  PublisherName: Temenos
  ServiceCategory: Developer Tools / API
  ServiceName: Temenos
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
name: Temenos Finops
provider_name: Temenos
provider_slug: temenos
publisher_name: Temenos
service_category: API
slug: temenos-finops
source_filename: temenos-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Temenos\nproviderId: temenos\npublisherName: Temenos\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Banking\n  - Cloud Banking\n  - Core Banking\n  - Digital Banking\n  - Financial Services\n  - Fintech\n  - Open Banking\n  - Payments\n  - Wealth Management\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Temenos API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n\
  \  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and\
  \ SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Temenos\n  ServiceCategory: Developer Tools / API\n  ProviderName: Temenos\n  PublisherName: Temenos\n  InvoiceIssuerName: Temenos\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned\
  \ over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Temenos Transact API\n    baseURL: https://api.temenos.com/transact\n    tags:\n      - Accounts\n      - Banking\n      - Core Banking\n      - Deposits\n      - Loans\n      - Transactions\n      - Treasury\n    serviceName: Temenos Transact API\n    serviceCategory: API\n  - name: Temenos Infinity API\n    baseURL: https://api.temenos.com/infinity\n    tags:\n      - Business Banking\n      - Customer Experience\n      - Digital Banking\n      - Mobile Banking\n      - Omnichannel\n      - Retail Banking\n    serviceName: Temenos Infinity API\n    serviceCategory: API\n  - name: Temenos Payments API\n    baseURL: https://api.temenos.com/payments\n\
  \    tags:\n      - Bulk Payments\n      - Direct Debit\n      - Open Banking\n      - Payment Processing\n      - Payments\n      - PSD2\n      - Real-Time Payments\n      - SEPA\n      - SWIFT\n    serviceName: Temenos Payments API\n    serviceCategory: API\n  - name: Temenos Fund Administration API\n    baseURL: https://api.temenos.com/funds\n    tags:\n      - Asset Management\n      - Fund Accounting\n      - Fund Management\n      - Investment\n      - Wealth Management\n    serviceName: Temenos Fund Administration API\n    serviceCategory: API\n  - name: Temenos Financial Crime Mitigation API\n    baseURL: https://api.temenos.com/fcm\n    tags:\n      - AML\n      - Compliance\n      - Fraud Detection\n      - KYC\n      - Risk Management\n      - Sanctions Screening\n    serviceName: Temenos Financial Crime Mitigation API\n    serviceCategory: API\n  - name: Temenos Transact Data Hub API\n    baseURL: https://api.temenos.com/transact-data-hub\n    tags:\n      - Analytics\n   \
  \   - Business Intelligence\n      - Data Hub\n      - Operational Data\n      - Reporting\n    serviceName: Temenos Transact Data Hub API\n    serviceCategory: API\n  - name: Temenos Wealth API\n    baseURL: https://api.temenos.com/wealth\n    tags:\n      - Investment Management\n      - Portfolio Management\n      - Private Banking\n      - Securities Trading\n      - Wealth Management\n    serviceName: Temenos Wealth API\n    serviceCategory: API\n  - name: Temenos Enterprise Product and Pricing API\n    baseURL: https://api.temenos.com/enterprise-pricing\n    tags:\n      - Banking Products\n      - Package Management\n      - Product Pricing\n      - Promotions\n      - Quotation\n    serviceName: Temenos Enterprise Product and Pricing API\n    serviceCategory: API\n  - name: Temenos Cloud Banking (CMB) API\n    baseURL: https://api.temenos.com/cmb\n    tags:\n      - Cloud Banking\n      - Commercial Banking\n      - Deposits\n      - Lending\n      - Regional Banking\n      - Regulatory\
  \ Compliance\n      - Trade Finance\n    serviceName: Temenos Cloud Banking (CMB) API\n    serviceCategory: API\n  - name: Temenos Lifecycle Management Suite API\n    baseURL: https://api.temenos.com/lms\n    tags:\n      - Account Origination\n      - Collections\n      - Decisioning\n      - Lifecycle Management\n      - Loan Origination\n    serviceName: Temenos Lifecycle Management Suite API\n    serviceCategory: API\n  - name: Temenos Journey Manager API\n    baseURL: https://journey.temenos.com/api\n    tags:\n      - Customer Journeys\n      - Digital Forms\n      - Onboarding\n      - Orchestration\n      - Workflow\n    serviceName: Temenos Journey Manager API\n    serviceCategory: API\n  - name: Temenos Transact Microservices API\n    baseURL: https://api.temenos.com/transact/microservices\n    tags:\n      - Configuration\n      - Entitlements\n      - Event Store\n      - Microservices\n      - Service Orchestration\n    serviceName: Temenos Transact Microservices API\n   \
  \ serviceCategory: API\n  - name: Temenos Ecosystem API\n    baseURL: https://api.temenos.com/ecosystem\n    tags:\n      - Cards\n      - Digital Assets\n      - Document Management\n      - Ecosystem\n      - Integrations\n    serviceName: Temenos Ecosystem API\n    serviceCategory: API\n  - name: Temenos Buy Now Pay Later API\n    baseURL: https://api.temenos.com/bnpl\n    tags:\n      - Buy Now Pay Later\n      - Consumer Lending\n      - Decisioning\n      - Point of Sale\n    serviceName: Temenos Buy Now Pay Later API\n    serviceCategory: API\n  - name: Temenos Explorer API\n    baseURL: https://api.temenos.com/explorer\n    tags:\n      - API Gateway\n      - Developer Tools\n      - Explorer\n      - Plugins\n    serviceName: Temenos Explorer API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\n\
  maintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/temenos/refs/heads/main/finops/temenos-finops.yml
sources: []
specification: FinOps Framework
tags:
- Banking
- Cloud Banking
- Core Banking
- Digital Banking
- Financial Services
- Fintech
- Open Banking
- Payments
- Wealth Management
- FinOps
- Cost Management
- FOCUS
---
