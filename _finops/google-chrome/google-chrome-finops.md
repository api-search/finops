---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: google-chrome-management-api-openapi.json
  format: json
  label: Chrome Management API
  slug: ''
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/google-chrome/refs/heads/main/openapi/google-chrome-management-api-openapi.json
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
description: FinOps framework definition for the Google Chrome API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Chrome
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Chrome
  PublisherName: Google Chrome
  ServiceCategory: Developer Tools / API
  ServiceName: Google Chrome
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
name: Google Chrome Finops
provider_name: Google Chrome
provider_slug: google-chrome
publisher_name: Google Chrome
service_category: API
slug: google-chrome-finops
source_filename: google-chrome-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Chrome\nproviderId: google-chrome\npublisherName: Google Chrome\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Browser\n  - Chrome Extensions\n  - Developer Tools\n  - Web Platform\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Chrome API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API\
  \ call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n\
  \      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Chrome\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Chrome\n  PublisherName: Google Chrome\n  InvoiceIssuerName: Google Chrome\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n\
  \    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Chrome Extensions API\n    baseURL: ''\n    tags:\n      - Add-Ons\n      - Browser\n      - Extensions\n    serviceName: Chrome Extensions API\n    serviceCategory: API\n  - name: Chrome DevTools Protocol\n    baseURL: ''\n    tags:\n      - Automation\n      - Debugging\n      - DevTools\n      - Testing\n    serviceName: Chrome DevTools Protocol\n    serviceCategory: API\n  - name: Chrome Web Store API\n    baseURL: ''\n    tags:\n      - Distribution\n      - Publishing\n      - Web Store\n    serviceName: Chrome Web Store API\n    serviceCategory: API\n  - name: Chrome Management API\n    baseURL: ''\n    tags:\n      - Administration\n      - Device Management\n\
  \      - Enterprise\n    serviceName: Chrome Management API\n    serviceCategory: API\n  - name: Chrome User Experience Report API\n    baseURL: ''\n    tags:\n      - Analytics\n      - Metrics\n      - Performance\n      - User Experience\n    serviceName: Chrome User Experience Report API\n    serviceCategory: API\n  - name: Chrome Policy API\n    baseURL: ''\n    tags:\n      - Administration\n      - Chrome OS\n      - Enterprise\n      - Policies\n    serviceName: Chrome Policy API\n    serviceCategory: API\n  - name: Chrome Verified Access API\n    baseURL: ''\n    tags:\n      - Chrome OS\n      - Enterprise\n      - Security\n      - Verification\n    serviceName: Chrome Verified Access API\n    serviceCategory: API\n  - name: Google Safe Browsing API\n    baseURL: ''\n    tags:\n      - Malware\n      - Phishing\n      - Security\n      - URL Checking\n    serviceName: Google Safe Browsing API\n    serviceCategory: API\n  - name: PageSpeed Insights API\n    baseURL: ''\n    tags:\n\
  \      - Analytics\n      - Lighthouse\n      - Optimization\n      - Performance\n    serviceName: PageSpeed Insights API\n    serviceCategory: API\n  - name: Chrome Built-in AI APIs\n    baseURL: ''\n    tags:\n      - AI\n      - Gemini Nano\n      - Machine Learning\n      - On-Device AI\n    serviceName: Chrome Built-in AI APIs\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n    url: https://apievangelist.com/\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-chrome/refs/heads/main/finops/google-chrome-finops.yml
sources: []
specification: FinOps Framework
tags:
- Browser
- Chrome Extensions
- Developer Tools
- Web Platform
- FinOps
- Cost Management
- FOCUS
---
