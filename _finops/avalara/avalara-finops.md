---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: avalara-avatax-rest-openapi.yml
  format: yaml
  label: AvaTax APIs
  slug: avatax-apis
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-avatax-rest-openapi.yml
- filename: avalara-communications-openapi.yml
  format: yaml
  label: Communications Tax API
  slug: communications-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-communications-openapi.yml
- filename: avalara-excise-openapi.yml
  format: yaml
  label: Excise Platform API
  slug: excise-tax-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-excise-openapi.yml
- filename: avalara-item-classification-openapi.yml
  format: yaml
  label: Item Classification API
  slug: item-classification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-item-classification-openapi.yml
- filename: avalara-avatax-brazil-openapi.yml
  format: yaml
  label: AvaTax Brazil API
  slug: avatax-brazil-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-avatax-brazil-openapi.yml
- filename: avalara-vat-reporting-openapi.yml
  format: yaml
  label: VAT Reporting API
  slug: vat-reporting-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-vat-reporting-openapi.yml
- filename: avalara-mylodgetax-openapi.yml
  format: yaml
  label: MyLodgeTax API
  slug: mylodgetax-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-mylodgetax-openapi.yml
- filename: avalara-certcapture-openapi.yml
  format: yaml
  label: CertCapture API
  slug: certcapture-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-certcapture-openapi.yml
- filename: avalara-e-invoicing-openapi.yml
  format: yaml
  label: E-Invoicing REST API
  slug: e-invoicing-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-e-invoicing-openapi.yml
- filename: avalara-activation-service-openapi.yml
  format: yaml
  label: Activation Service API
  slug: activation-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-activation-service-openapi.yml
- filename: avalara-business-openapi.yml
  format: yaml
  label: Avalara Business API
  slug: business-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-business-openapi.yml
- filename: avalara-portal-oauth-openapi.yml
  format: yaml
  label: Portal OAuth API
  slug: portal-oauth-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-portal-oauth-openapi.yml
- filename: avalara-shared-company-service-openapi.yml
  format: yaml
  label: Shared Company Service API
  slug: shared-company-service-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-shared-company-service-openapi.yml
- filename: avalara-hs-code-classification-openapi.yml
  format: yaml
  label: Automated Tariff Code Classification API
  slug: hs-code-classification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-hs-code-classification-openapi.yml
- filename: avalara-1099-w9-openapi.yml
  format: yaml
  label: 1099 & W-9 API
  slug: 1099-w9-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/openapi/avalara-1099-w9-openapi.yml
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
description: FinOps framework definition for the Avalara API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Avalara
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Avalara
  PublisherName: Avalara
  ServiceCategory: Developer Tools / API
  ServiceName: Avalara
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
name: Avalara Finops
provider_name: Avalara
provider_slug: avalara
publisher_name: Avalara
service_category: API
slug: avalara-finops
source_filename: avalara-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Avalara\nproviderId: avalara\npublisherName: Avalara\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Taxes\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Avalara API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can\
  \ be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing\
  \ and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Avalara\n  ServiceCategory: Developer Tools / API\n  ProviderName: Avalara\n  PublisherName: Avalara\n  InvoiceIssuerName: Avalara\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n\
  \    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Avalara\n    baseURL: ''\n    tags:\n      - Taxes\n    serviceName: Avalara\n    serviceCategory: API\n  - name: AvaTax APIs\n    baseURL: ''\n    tags:\n      - Sales Tax\n      - Taxes\n      - VAT\n    serviceName: AvaTax APIs\n    serviceCategory: API\n  - name: AvaTax SOAP API\n    baseURL: ''\n    tags:\n      - SOAP\n      - Taxes\n    serviceName: AvaTax SOAP API\n    serviceCategory: API\n  - name: Communications Tax API\n    baseURL: ''\n    tags:\n      - Communications\n      - Taxes\n      - Telecom\n    serviceName: Communications Tax API\n    serviceCategory: API\n  - name: Excise Platform API\n    baseURL: ''\n    tags:\n      - Excise\n      - Taxes\n    serviceName: Excise Platform API\n    serviceCategory: API\n  - name: Item Classification API\n    baseURL: ''\n    tags:\n\
  \      - Classification\n      - HS Codes\n      - Taxes\n    serviceName: Item Classification API\n    serviceCategory: API\n  - name: Avalara Tax Content for Retail Configuration API\n    baseURL: ''\n    tags:\n      - Point of Sale\n      - Retail\n      - Taxes\n    serviceName: Avalara Tax Content for Retail Configuration API\n    serviceCategory: API\n  - name: AvaTax Brazil API\n    baseURL: ''\n    tags:\n      - Brazil\n      - Taxes\n    serviceName: AvaTax Brazil API\n    serviceCategory: API\n  - name: VAT Reporting API\n    baseURL: ''\n    tags:\n      - Reporting\n      - Taxes\n      - VAT\n    serviceName: VAT Reporting API\n    serviceCategory: API\n  - name: MyLodgeTax API\n    baseURL: ''\n    tags:\n      - Lodging\n      - Short-Term Rental\n      - Taxes\n    serviceName: MyLodgeTax API\n    serviceCategory: API\n  - name: CertCapture API\n    baseURL: ''\n    tags:\n      - Certificates\n      - Exemptions\n      - Taxes\n    serviceName: CertCapture API\n    serviceCategory:\
  \ API\n  - name: E-Invoicing REST API\n    baseURL: ''\n    tags:\n      - Compliance\n      - E-Invoicing\n      - Taxes\n    serviceName: E-Invoicing REST API\n    serviceCategory: API\n  - name: Activation Service API\n    baseURL: ''\n    tags:\n      - Registration\n      - Taxes\n    serviceName: Activation Service API\n    serviceCategory: API\n  - name: Avalara Business API\n    baseURL: ''\n    tags:\n      - Business\n      - Orders\n      - Taxes\n    serviceName: Avalara Business API\n    serviceCategory: API\n  - name: Portal OAuth API\n    baseURL: ''\n    tags:\n      - Authentication\n      - OAuth\n      - Taxes\n    serviceName: Portal OAuth API\n    serviceCategory: API\n  - name: Shared Company Service API\n    baseURL: ''\n    tags:\n      - Company Management\n      - Taxes\n    serviceName: Shared Company Service API\n    serviceCategory: API\n  - name: Automated Tariff Code Classification API\n    baseURL: ''\n    tags:\n      - Classification\n      - HS Codes\n\
  \      - Tariff\n      - Taxes\n    serviceName: Automated Tariff Code Classification API\n    serviceCategory: API\n  - name: Self-Serve Tariff Classification API\n    baseURL: ''\n    tags:\n      - Cross-Border\n      - Tariff\n      - Taxes\n    serviceName: Self-Serve Tariff Classification API\n    serviceCategory: API\n  - name: 1099 & W-9 API\n    baseURL: ''\n    tags:\n      - Tax Forms\n      - Taxes\n      - W-9\n    serviceName: 1099 & W-9 API\n    serviceCategory: API\n  - name: License Guidance Order API\n    baseURL: ''\n    tags:\n      - Licensing\n      - Registration\n      - Taxes\n    serviceName: License Guidance Order API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n  - FN: Avalara Developer Relations\n    email:\
  \ developer.relations@avalara.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/avalara/refs/heads/main/finops/avalara-finops.yml
sources: []
specification: FinOps Framework
tags:
- Taxes
- FinOps
- Cost Management
- FOCUS
---
