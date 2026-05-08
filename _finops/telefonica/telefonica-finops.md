---
aligned_with:
  dataSpec: FOCUS
  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/
  dataSpecVersion: '1.3'
  framework: FinOps Foundation Framework
  frameworkUrl: https://www.finops.org/framework/
api_specs:
- filename: telefonica-number-verification-openapi.yml
  format: yaml
  label: Telefónica Number Verification API
  slug: number-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-number-verification-openapi.yml
- filename: telefonica-sim-swap-openapi.yml
  format: yaml
  label: Telefónica SIM Swap API
  slug: sim-swap-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-sim-swap-openapi.yml
- filename: telefonica-kyc-match-openapi.yml
  format: yaml
  label: Telefónica Know Your Customer Match API
  slug: kyc-match-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-kyc-match-openapi.yml
- filename: telefonica-location-verification-openapi.yml
  format: yaml
  label: Telefónica Location Verification API
  slug: location-verification-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-location-verification-openapi.yml
- filename: telefonica-quality-on-demand-openapi.yml
  format: yaml
  label: Telefónica Quality on Demand API
  slug: quality-on-demand-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-quality-on-demand-openapi.yml
- filename: telefonica-device-roaming-openapi.yml
  format: yaml
  label: Telefónica Device Roaming Status API
  slug: device-roaming-status-api
  spec_type: OpenAPI
  url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/openapi/telefonica-device-roaming-openapi.yml
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
description: FinOps framework definition for the Telefónica API surface. Provides a FOCUS-aligned mapping for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.
focus_columns:
  BillingCurrency: USD
  ChargeCategory: Usage
  InvoiceIssuerName: Telefónica
  PricingCategory: Usage-Based
  PricingUnit: request
  ProviderName: Telefónica
  PublisherName: Telefónica
  ServiceCategory: Developer Tools / API
  ServiceName: Telefónica
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
name: Telefonica Finops
provider_name: Telefónica
provider_slug: telefonica
publisher_name: Telefónica
service_category: API
slug: telefonica-finops
source_filename: telefonica-finops.yml
source_heading: FinOps Profile
source_url: ''
source_yaml: "specification: FinOps Framework\nspecificationVersion: '1.0'\nalignedWith:\n  framework: FinOps Foundation Framework\n  frameworkUrl: https://www.finops.org/framework/\n  dataSpec: FOCUS\n  dataSpecVersion: '1.3'\n  dataSpecUrl: https://focus.finops.org/focus-specification/v1-3/\nprovider: Telefónica\nproviderId: telefonica\npublisherName: Telefónica\nserviceCategory: API\ncreated: '2026-05-08'\nmodified: '2026-05-08'\ntags:\n  - Telecommunications\n  - Mobile Network\n  - CAMARA\n  - Open Gateway\n  - Authentication\n  - Fraud Prevention\n  - Location Services\n  - FinOps\n  - Cost Management\n  - FOCUS\ndescription: FinOps framework definition for the Telefónica API surface. Provides a FOCUS-aligned mapping\n  for cost allocation, usage measurement, and unit-economics reporting across the provider's APIs.\nprinciples:\n  - name: Visibility\n    description: Make API consumption costs visible to engineering, product, and finance teams in near\n      real-time.\n  - name: Allocation\n\
  \    description: Tag every chargeable API call with the consuming team, environment, application, and\n      feature so cost can be allocated.\n  - name: Optimization\n    description: Continuously evaluate request patterns, caching, batching, and tier selection to reduce\n      cost per useful unit of work.\n  - name: Accountability\n    description: Establish budget owners and chargeback or showback flows for each consuming team.\ndomains:\n  - name: Understand Usage and Cost\n    capabilities:\n      - Data Ingestion\n      - Allocation\n      - Reporting and Analytics\n      - Anomaly Management\n  - name: Quantify Business Value\n    capabilities:\n      - Planning and Estimating\n      - Forecasting\n      - Budgeting\n      - Benchmarking\n      - Unit Economics\n  - name: Optimize Usage and Cost\n    capabilities:\n      - Architecting for Cloud\n      - Rate Optimization\n      - Workload Optimization\n      - Cloud Sustainability\n      - Licensing and SaaS\n  - name: Manage\
  \ the FinOps Practice\n    capabilities:\n      - FinOps Practice Operations\n      - FinOps Education and Enablement\n      - Invoicing and Chargeback\n      - Onboarding Workloads\n      - Intersecting Disciplines\nbillingModel:\n  pricingCategory: Usage-Based\n  billingFrequency: Monthly\n  billingCurrency: USD\n  chargeCategories:\n    - Usage\n    - Purchase\n    - Tax\n    - Credit\n    - Adjustment\n  chargeFrequency: Recurring\nfocusColumns:\n  ServiceName: Telefónica\n  ServiceCategory: Developer Tools / API\n  ProviderName: Telefónica\n  PublisherName: Telefónica\n  InvoiceIssuerName: Telefónica\n  PricingCategory: Usage-Based\n  PricingUnit: request\n  BillingCurrency: USD\n  ChargeCategory: Usage\nmeters:\n  - name: api_requests\n    description: Count of billable API requests\n    unit: request\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\n      - region\n      - consumer\n  - name: data_egress\n    description: Bytes returned over the\
  \ network in API responses\n    unit: GB\n    aggregation: sum\n    dimensions:\n      - api\n      - region\n      - consumer\n  - name: compute_seconds\n    description: Server-side compute consumed by the request, where applicable\n    unit: second\n    aggregation: sum\n    dimensions:\n      - api\n      - endpoint\n      - tier\napis:\n  - name: Telefónica Number Verification API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Authentication\n      - Number Verification\n      - Fraud Prevention\n      - Mobile Identity\n      - SIM\n    serviceName: Telefónica Number Verification API\n    serviceCategory: API\n  - name: Telefónica SIM Swap API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Authentication\n      - Fraud Prevention\n      - SIM Swap\n      - Mobile Security\n    serviceName: Telefónica SIM Swap API\n    serviceCategory: API\n  - name: Telefónica Know Your Customer Match API\n    baseURL: https://opengateway.telefonica.com\n\
  \    tags:\n      - Authentication\n      - Fraud Prevention\n      - KYC\n      - Identity Verification\n      - Financial Services\n    serviceName: Telefónica Know Your Customer Match API\n    serviceCategory: API\n  - name: Telefónica Location Verification API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Location Services\n      - Device Location\n      - Fraud Prevention\n      - Mobile Network\n    serviceName: Telefónica Location Verification API\n    serviceCategory: API\n  - name: Telefónica Quality on Demand API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Quality of Service\n      - Mobile Network\n      - IoT\n      - Network Slicing\n      - Communication Quality\n    serviceName: Telefónica Quality on Demand API\n    serviceCategory: API\n  - name: Telefónica Device Roaming Status API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Roaming\n      - Device Status\n      - Fraud Prevention\n      - Mobile\
  \ Network\n    serviceName: Telefónica Device Roaming Status API\n    serviceCategory: API\n  - name: Telefónica Scam Signal API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Fraud Prevention\n      - Scam Detection\n      - Phishing\n      - Voice Fraud\n      - Security\n    serviceName: Telefónica Scam Signal API\n    serviceCategory: API\n  - name: Telefónica Age Verification API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Age Verification\n      - Compliance\n      - E-Commerce\n      - Media\n      - Privacy\n    serviceName: Telefónica Age Verification API\n    serviceCategory: API\n  - name: Telefónica Line Tenure API\n    baseURL: https://opengateway.telefonica.com\n    tags:\n      - Fraud Prevention\n      - Identity Verification\n      - Financial Services\n      - Mobile Security\n    serviceName: Telefónica Line Tenure API\n    serviceCategory: API\n  - name: Telefónica Population Density Data API\n    baseURL: https://opengateway.telefonica.com\n\
  \    tags:\n      - Location Services\n      - Population Data\n      - Analytics\n      - Transport\n      - Smart City\n    serviceName: Telefónica Population Density Data API\n    serviceCategory: API\nunitEconomics:\n  - name: Cost per 1K Requests\n    metric: billed_cost / (api_requests / 1000)\n    target: TBD\n  - name: Cost per Active Consumer\n    metric: billed_cost / active_consumers\n    target: TBD\nmaintainers:\n  - FN: Kin Lane\n    email: kin@apievangelist.com\n"
source_yaml_url: https://raw.githubusercontent.com/api-evangelist/telefonica/refs/heads/main/finops/telefonica-finops.yml
sources: []
specification: FinOps Framework
tags:
- Telecommunications
- Mobile Network
- CAMARA
- Open Gateway
- Authentication
- Fraud Prevention
- Location Services
- FinOps
- Cost Management
- FOCUS
---
