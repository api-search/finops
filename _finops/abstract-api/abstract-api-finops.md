---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: abstract-api-email-reputation.yaml
  format: yaml
  label: Email Reputation API
  slug: email-reputation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-email-reputation.yaml
- filename: abstract-api-phone-intelligence.yaml
  format: yaml
  label: Phone Intelligence API
  slug: phone-intelligence
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-phone-intelligence.yaml
- filename: abstract-api-ip-geolocation.yaml
  format: yaml
  label: IP Geolocation API
  slug: ip-geolocation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-ip-geolocation.yaml
- filename: abstract-api-ip-intelligence.yaml
  format: yaml
  label: IP Intelligence API
  slug: ip-intelligence
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-ip-intelligence.yaml
- filename: abstract-api-company-enrichment.yaml
  format: yaml
  label: Company Enrichment API
  slug: company-enrichment
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-company-enrichment.yaml
- filename: abstract-api-exchange-rates.yaml
  format: yaml
  label: Exchange Rates API
  slug: exchange-rates
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-exchange-rates.yaml
- filename: abstract-api-public-holidays.yaml
  format: yaml
  label: Public Holidays API
  slug: public-holidays
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-public-holidays.yaml
- filename: abstract-api-timezones.yaml
  format: yaml
  label: Timezone API
  slug: timezones
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-timezones.yaml
- filename: abstract-api-vat-validation.yaml
  format: yaml
  label: VAT Validation API
  slug: vat-validation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-vat-validation.yaml
- filename: abstract-api-iban-validation.yaml
  format: yaml
  label: IBAN Validation API
  slug: iban-validation
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-iban-validation.yaml
- filename: abstract-api-website-screenshot.yaml
  format: yaml
  label: Website Screenshot API
  slug: website-screenshot
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-website-screenshot.yaml
- filename: abstract-api-image-processing.yaml
  format: yaml
  label: Image Processing API
  slug: image-processing
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-image-processing.yaml
- filename: abstract-api-web-scraping.yaml
  format: yaml
  label: Web Scraping API
  slug: web-scraping
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-web-scraping.yaml
- filename: abstract-api-avatars.yaml
  format: yaml
  label: Avatars API
  slug: avatars
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/openapi/abstract-api-avatars.yaml
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
description: FinOps framework definition for the Abstract API API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Abstract API
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Abstract API
  PublisherName: Abstract API
  ServiceCategory: Developer Tools / API
  ServiceName: Abstract API
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
name: Abstract Api Finops
provider_name: Abstract API
provider_slug: abstract-api
publisher_name: Abstract API
service_category: API
slug: abstract-api-finops
source_filename: abstract-api-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Abstract API\nproviderId: abstract-api\npublisherName: Abstract API\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Avatars\n  - Company Enrichment\n  - Contacts\n  - Currencies\n  - Email Validation\n  - Exchange Rates\n  - IBAN Validation\n  - Image Processing\n  - IP Geolocation\n  - IP Intelligence\n  - Phone Validation\n  - Public Holidays\n  - Screenshots\n  - Timezones\n  - VAT Validation\n  - Web Scraping\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Abstract API API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's\
  \ APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n\
  \    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Abstract API\n  ServiceCategory: Developer Tools / API\n  ProviderName: Abstract API\n  PublisherName: Abstract API\n  InvoiceIssuerName: Abstract API\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit:\
  \ request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Email Reputation API\n    baseURL: https://emailreputation.abstractapi.com/v1/\n    tags:\n      - Email Validation\n      - Email Reputation\n      - Fraud Detection\n    serviceName: Email Reputation API\n    serviceCategory: API\n  - name: Phone Intelligence API\n    baseURL: https://phoneintelligence.abstractapi.com/v1/\n    tags:\n      - Phone Validation\n      - Phone Intelligence\n      - Fraud Detection\n    serviceName: Phone Intelligence API\n\
  \    serviceCategory: API\n  - name: IP Geolocation API\n    baseURL: https://ipgeolocation.abstractapi.com/v1/\n    tags:\n      - IP Geolocation\n      - IP Addresses\n      - Geolocation\n    serviceName: IP Geolocation API\n    serviceCategory: API\n  - name: IP Intelligence API\n    baseURL: https://ip-intelligence.abstractapi.com/v1/\n    tags:\n      - IP Intelligence\n      - IP Addresses\n      - Security\n      - Fraud Detection\n    serviceName: IP Intelligence API\n    serviceCategory: API\n  - name: Company Enrichment API\n    baseURL: https://companyenrichment.abstractapi.com/v1/\n    tags:\n      - Company Enrichment\n      - Business Data\n      - Data Enrichment\n    serviceName: Company Enrichment API\n    serviceCategory: API\n  - name: Exchange Rates API\n    baseURL: https://exchange-rates.abstractapi.com/v1/\n    tags:\n      - Currencies\n      - Exchange Rates\n      - Finance\n    serviceName: Exchange Rates API\n    serviceCategory: API\n  - name: Public Holidays\
  \ API\n    baseURL: https://holidays.abstractapi.com/v1/\n    tags:\n      - Public Holidays\n      - Calendar\n      - Global Data\n    serviceName: Public Holidays API\n    serviceCategory: API\n  - name: Timezone API\n    baseURL: https://timezone.abstractapi.com/v1/\n    tags:\n      - Timezones\n      - Time\n      - Date\n      - Calendar\n    serviceName: Timezone API\n    serviceCategory: API\n  - name: VAT Validation API\n    baseURL: https://vat.abstractapi.com/v1/\n    tags:\n      - VAT Validation\n      - Finance\n      - Compliance\n      - Tax\n    serviceName: VAT Validation API\n    serviceCategory: API\n  - name: IBAN Validation API\n    baseURL: https://ibanvalidation.abstractapi.com/v1/\n    tags:\n      - IBAN Validation\n      - Finance\n      - Banking\n    serviceName: IBAN Validation API\n    serviceCategory: API\n  - name: Website Screenshot API\n    baseURL: https://screenshot.abstractapi.com/v1/\n    tags:\n      - Screenshots\n      - Web Capture\n      - Images\n\
  \    serviceName: Website Screenshot API\n    serviceCategory: API\n  - name: Image Processing API\n    baseURL: https://images.abstractapi.com/v1/\n    tags:\n      - Image Processing\n      - Images\n      - Optimization\n    serviceName: Image Processing API\n    serviceCategory: API\n  - name: Web Scraping API\n    baseURL: https://scrape.abstractapi.com/v1/\n    tags:\n      - Web Scraping\n      - Data Extraction\n      - HTML\n    serviceName: Web Scraping API\n    serviceCategory: API\n  - name: Avatars API\n    baseURL: https://avatars.abstractapi.com/v1/\n    tags:\n      - Avatars\n      - Images\n      - User Interface\n    serviceName: Avatars API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/abstract-api/refs/heads/main/finops/abstract-api-finops.yml
sources: []
specification: FinOps Framework
tags:
- Avatars
- Company Enrichment
- Contacts
- Currencies
- Email Validation
- Exchange Rates
- IBAN Validation
- Image Processing
- IP Geolocation
- IP Intelligence
- Phone Validation
- Public Holidays
- Screenshots
- Timezones
- VAT Validation
- Web Scraping
- FinOps
- Cost Management
- FOCUS
---
