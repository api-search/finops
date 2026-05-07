---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: rest
  format: yaml
  label: Google Pay API
  slug: ''
  spec_type: OpenAPI
  url: https://developers.google.com/pay/api/web/reference/rest
- filename: v1
  format: yaml
  label: Google Wallet API
  slug: ''
  spec_type: OpenAPI
  url: https://developers.google.com/wallet/generic/rest/v1
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
description: FinOps framework definition for the Google Pay API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Google Pay
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Google Pay
  PublisherName: Google Pay
  ServiceCategory: Developer Tools / API
  ServiceName: Google Pay
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
name: Google Pay Finops
provider_name: Google Pay
provider_slug: google-pay
publisher_name: Google Pay
service_category: API
slug: google-pay-finops
source_filename: google-pay-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Google Pay\nproviderId: google-pay\npublisherName: Google Pay\nserviceCategory: API\ncreated: '2026-05-04'\nmodified: '2026-05-04'\ntags:\n  - Contactless Payments\n  - Digital Wallet\n  - Mobile Payments\n  - Payments\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Google Pay API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n    description: Tag every chargeable API call\
  \ with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage the FinOps Practice\n    capabilities:\n    \
  \  - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Google Pay\n  ServiceCategory: Developer Tools / API\n  ProviderName: Google Pay\n  PublisherName: Google Pay\n  InvoiceIssuerName: Google Pay\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the network in API responses\n    unit: GB\n  \
  \  aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Google Pay API\n    baseURL: https://pay.google.com/gp/v/\n    tags:\n      - Checkout\n      - Payments\n      - Web\n    serviceName: Google Pay API\n    serviceCategory: API\n  - name: Google Pay API for Android\n    baseURL: https://pay.google.com/gp/v/\n    tags:\n      - Android\n      - Checkout\n      - Mobile\n      - Payments\n    serviceName: Google Pay API for Android\n    serviceCategory: API\n  - name: Google Wallet API\n    baseURL: https://walletobjects.googleapis.com/\n    tags:\n      - Loyalty\n      - Passes\n      - Tickets\n      - Wallet\n    serviceName: Google Wallet API\n    serviceCategory: API\n  - name: Google Pay Facilitated Transaction Event API\n  \
  \  baseURL: https://pay.google.com/\n    tags:\n      - Payment Integrators\n      - Payments\n      - Transactions\n    serviceName: Google Pay Facilitated Transaction Event API\n    serviceCategory: API\n  - name: Google Pay Virtual Cards API\n    baseURL: https://pay.google.com/\n    tags:\n      - Card Issuance\n      - Payments\n      - Virtual Cards\n    serviceName: Google Pay Virtual Cards API\n    serviceCategory: API\n  - name: Google Pay Push Provisioning API\n    baseURL: https://pay.google.com/\n    tags:\n      - Card Provisioning\n      - Issuers\n      - Payments\n      - Tokenization\n    serviceName: Google Pay Push Provisioning API\n    serviceCategory: API\n  - name: Google Pay Payment Card Recognition API\n    baseURL: https://pay.google.com/\n    tags:\n      - Android\n      - Card Recognition\n      - OCR\n      - Payments\n    serviceName: Google Pay Payment Card Recognition API\n    serviceCategory: API\n  - name: Google Pay India Merchant SDK\n    baseURL: https://pay.google.com/\n\
  \    tags:\n      - India\n      - Merchant SDK\n      - Payments\n      - UPI\n    serviceName: Google Pay India Merchant SDK\n    serviceCategory: API\n  - name: Google Universal Commerce Protocol\n    baseURL: https://pay.google.com/\n    tags:\n      - Agentic Commerce\n      - Checkout\n      - Commerce\n      - Merchants\n    serviceName: Google Universal Commerce Protocol\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/google-pay/refs/heads/main/finops/google-pay-finops.yml
sources: []
specification: FinOps Framework
tags:
- Contactless Payments
- Digital Wallet
- Mobile Payments
- Payments
- FinOps
- Cost Management
- FOCUS
---
